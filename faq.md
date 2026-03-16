# FAQ

Answers to the most common questions about Sieve.

---

## Privacy and data

**Is my data private?**  
Your images are only sent to the AI provider you choose, using your own API key. Sieve has no servers, no accounts, and no telemetry. Nothing goes to the Sieve project.

If you use Ollama, your images never leave your device at all.

**Does Sieve store my images in the cloud?**  
No. Sieve stores everything on your device in the folder you chose during setup. No cloud storage is involved unless you deliberately move files there yourself.

**Is my API key secure?**  
Your API key is stored using your device's encrypted secure storage and is never transmitted anywhere except directly to your chosen provider when making a classification request.

**Can I use Sieve with patient or confidential research images?**  
If you use Ollama, yes — your images never leave your device. If you use a cloud provider, your images are sent to that provider and subject to their data policies. Check your institution's data policies before using a cloud provider with sensitive data.

---

## Installation

**Why does Android warn me about the APK?**  
Android shows this warning for any app installed outside the Play Store. Sieve is distributed directly to avoid marketplace fees. The warning is expected and normal — you can safely allow the installation.

**Why does macOS block the app?**  
macOS shows this warning for apps not distributed through the App Store. Go to **System Settings → Privacy & Security** and click **Open Anyway** to allow it.

**Why does Windows show a SmartScreen warning?**  
Same reason as macOS — the app is not from the Microsoft Store. Click **More info** then **Run anyway**.

---

## Classification

**How accurate is Sieve?**  
For clearly distinct image categories with good quality images, accuracy is typically in the 80–90% range. Blurry, ambiguous, or visually similar categories will produce lower accuracy. Images flagged as uncertain (confidence below 0.6) are most likely to be misclassified and should be reviewed manually.

**Why is my image flagged as uncertain?**  
The AI's confidence score for that image was below 0.6. This usually means the image is ambiguous, low quality, doesn't clearly fit any of your labels, or sits visually between two of your categories. Review the image manually and reclassify it if needed.

**Can Sieve assign multiple labels to one image?**  
Not in v0.1.5. Each image receives exactly one label — the best match from your label set. Multi-label support may come in a future version.

**What image formats are supported?**  
Sieve works with standard image formats: JPG, JPEG, PNG, TIFF, BMP, and WEBP. If your images are in a proprietary format from lab equipment, you may need to export or convert them first.

**What happens if an image doesn't match any of my labels?**  
The AI will still pick the closest match from your label list — it always chooses from what you provide. The confidence score will typically be low, so the image will be flagged as uncertain. Consider adding an `Other` or `Unknown` label to your label set as a catch-all.

**Does image resolution affect accuracy?**  
Yes. Very small or heavily compressed images may reduce accuracy. Sieve does not require high resolution — most images at their normal export size work well.

---

## Providers and API keys

**Which provider is best?**  
For most users, OpenRouter's free tier is the best starting point. For sensitive data, use Ollama. For the highest accuracy on difficult images, OpenAI or Anthropic.

**Does Sieve work offline?**  
Yes, if you use Ollama. All other providers require an internet connection to process images.

**I hit the rate limit on OpenRouter. What do I do?**  
Wait until the next day for the free daily limit to reset, add credits to your OpenRouter account to remove the limit, or switch to Ollama for unlimited local classification.

**Can I use Sieve without any API key?**  
No. Sieve needs an AI provider to classify images. Ollama is the only option that does not require a paid or registered account — it just needs to be installed on your machine.

---

## Files and storage

**Where are my sorted images saved?**  
In the folder you chose during first-time setup. You can see the exact path for any image by opening **File Info** from the gallery.

**Can I change my storage folder?**  
Yes, go to **Settings → Storage** and choose a new folder. Images already sorted will stay in the old location — Sieve does not automatically move them.

**Does Sieve delete my original images?**  
No. Sieve copies images into the sorted folder structure. Your originals are not touched unless you explicitly delete them.

**The gallery is empty even though I have sorted images. Why?**  
The gallery reads from your current storage folder. If you changed the storage folder in settings, point it back to the folder containing your sorted images. Also check that Sieve has storage permission on Android.

---

## Appearance

**How do I switch between dark and light mode?**  
Go to **Settings → Appearance** and toggle the theme. Sieve v0.1.5 supports both dark and light modes.

---

## The project

**Is Sieve free?**  
Yes, completely free. No trial period, no premium tier, no in-app purchases.

**Is the code open source?**  
Yes. The full source code is available at [github.com/sieve-sort/sieve-app](https://github.com/sieve-sort/sieve-app) under the MIT license.

**Can I use Sieve commercially?**  
Yes. The MIT license allows use for any purpose including commercial use.

**How do I report a bug or request a feature?**  
Open an issue on the [GitHub repository](https://github.com/sieve-sort/sieve-app/issues).

**How do I support the project?**  
[Buy the developer a coffee](https://buymeacoffee.com/sameermann). It helps keep the project going.

Next: [Why We Built This](why-we-built-this.md)
