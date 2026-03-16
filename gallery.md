# The Gallery

The gallery is where you browse and manage your sorted images after classification. It reads directly from your storage folder, so it works even if you close and reopen the app.

---

## Opening the gallery

Tap or click **Gallery** in the bottom navigation bar. Sieve will scan your storage folder and display all sorted images grouped by label.

> **Screenshot placeholder — gallery main view**

---

## How images are displayed

Images are arranged in a grid, grouped by their assigned label. Each group has a section header showing the label name.

Each image thumbnail shows:
- The filename
- The confidence score
- A warning icon if the confidence was below 0.6 (uncertain classification)

Tap any thumbnail to open the image full screen.

> **Screenshot placeholder — thumbnail with confidence score and warning indicator**

---

## Per-image options

Long press an image (mobile) or click the three-dot menu (desktop) to open the options panel for that image. The options are:

**Share**
Opens your device's share sheet so you can send the image via email, messaging apps, or other apps on your device.

**Delete**
Permanently deletes the image from your device storage. lab-i will ask you to confirm before deleting. This cannot be undone.

**File Info**
Shows a summary of everything lab-i knows about that image:
- Full file path on your device
- File size
- Image dimensions
- Assigned label
- Confidence score
- Date and time of classification

> **Screenshot placeholder — file info dialog**

---

## Uncertain images

Images flagged as uncertain (confidence below 0.6) are still sorted and visible in the gallery but they have a small warning indicator on their thumbnail. These are the images most worth reviewing manually.

If you find a misclassified image, you can delete it from its current folder and re-run classification on it with a different or more specific label set.

---

## Dark and light theme

Sieve v0.1.5 includes both a dark and light theme. You can switch between them in **Settings → Appearance**. The gallery respects your chosen theme.

> **Screenshot placeholder — gallery in dark mode**

---

## The gallery and your storage folder

The gallery is just a view into your storage folder. It does not maintain its own database of images. This means:

- If you manually move or delete files outside of Sieve, the gallery will reflect those changes on the next refresh
- If you switch devices or reinstall the app, pointing Sieve at the same storage folder will restore your gallery
- The gallery works offline — no internet needed to browse your sorted images

Next: [Supported Providers](providers.md)
