# How Classification Works

This page explains what happens when Sieve classifies your images — from the moment you press classify to the moment your files are sorted into folders.

---

## The basic idea

Sieve shows each of your images to an AI vision model and asks it to pick the best matching label from your list. The AI looks at the image, considers your labels, and responds with its best guess along with a confidence score — a number between 0 and 1 that indicates how certain it is.

Sieve then renames the file, sorts it into a folder, and moves on to the next image.

---

## Step by step

### 1. You select images and a label set

On the main screen, you choose:
- A single image or a folder of images
- Which label set to use (your list of categories)

> **Screenshot placeholder — main classify screen**

---

### 2. Each image is sent to the AI

For each image, Sieve sends the image and a prompt to your chosen AI provider. The prompt looks like this:

```
Classify this image using exactly one of the following labels: 
[your labels here]. 
Respond with only the label and a confidence score between 0 and 1.
Format: label|confidence
```

The AI looks at the image and responds with something like:
```
Gel|0.92
```

This means the AI is 92% confident the image is a gel.

---

### 3. The result is evaluated

Sieve reads the response and checks the confidence score:

- **0.6 or above** — classified normally, sorted into the matching folder
- **Below 0.6** — classified but flagged as uncertain with a warning indicator in the gallery

Uncertain images are still sorted — they don't get skipped — but the warning tells you to double check that result manually.

---

### 4. The file is renamed

Before sorting, Sieve renames the file using this format:

```
YYYYMMDD_HHMMSS_[label].[original extension]
```

For example, an image originally called `IMG_4823.jpg` taken on March 15 2026 at 2:23pm and classified as a Gel would become:

```
20260315_142301_Gel.jpg
```

The date and time come from the file's original timestamp, not the time of classification.

If two files have the same timestamp, Sieve adds a number to avoid collisions:
```
20260315_142301_Gel_1.jpg
20260315_142301_Gel_2.jpg
```

---

### 5. The file is sorted into a folder

Inside your chosen storage folder, Sieve creates subfolders named after each label and copies the renamed file into the right one:

```
/sieve-storage/
  /Gel/
    20260315_142301_Gel.jpg
  /Microscopy/
    20260314_091522_Microscopy.jpg
  /Drosophila/
    20260314_103401_Drosophila.jpg
```

The original file is not deleted unless you explicitly choose to delete it.

---

### 6. A CSV is generated

When classification is complete, Sieve exports a CSV file summarising every result:

```
filename, label, confidence, flagged
20260315_142301_Gel.jpg, Gel, 0.92, No
20260314_091522_Microscopy.jpg, Microscopy, 0.87, No
20260314_103401_Drosophila.jpg, Drosophila, 0.54, Yes
```

This CSV is useful for record keeping, sharing results with colleagues, or importing into analysis tools.

---

## How accurate is it?

Accuracy depends on several factors:

**Image clarity** — well-lit, in-focus images classify much more accurately than blurry or poorly cropped ones.

**How distinct your labels are** — labels that look very different from each other (a gel versus a petri plate) will classify accurately. Labels that overlap visually (microorganisms versus microscopy) may occasionally be confused.

**Which provider you use** — larger, more capable models like GPT-4o or Qwen 2.5 VL 72B perform better than smaller or lighter models.

In general, for clearly distinct biological image categories, you can expect accuracy in the range of 80–90% on clean images. Images flagged as uncertain (below 0.6 confidence) are the ones most likely to be misclassified and worth reviewing manually.

---

## What about images that don't match any label?

If an image genuinely doesn't fit any of your labels, the AI will still pick the closest match — it always chooses from your list. The confidence score will usually be low, so it will be flagged as uncertain. This is a good signal to review those images and either reclassify them manually or add a new label to your label set.

---

## Processing speed

Speed depends on your provider and connection:

| Provider | Approximate speed |
|----------|------------------|
| OpenRouter (cloud) | 2–5 seconds per image |
| OpenAI / Anthropic / Gemini | 2–5 seconds per image |
| Ollama (local, modern hardware) | 5–15 seconds per image |
| Ollama (local, older hardware) | 15–30 seconds per image |

For a batch of 100 images on a cloud provider, expect around 5–10 minutes total.

Next: [Label Set Management](label-sets.md)
