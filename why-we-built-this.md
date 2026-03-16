# Why We Built This

lab-i exists because a frustrating but solvable problem kept coming up in research workflows — and no existing tool was addressing it in a way that actually worked for researchers.

---

## The problem

Researchers generate a lot of images. A single imaging session can produce hundreds of files. Over weeks and months, this becomes thousands of images sitting in folders with names like `IMG_4823.jpg`, `scan_002_final_v3.tif`, or `untitled_export.png`.

At some point, someone has to go through all of them and figure out what they are. This is slow, tedious, and error-prone — especially when the person doing it wasn't the one who took the images, or when returning to a project after months away.

The manual tagging and organisation of images is a task that can take hours per experiment. Multiply that across a whole lab and across a year, and it represents a significant amount of time that could be spent on actual research.

---

## Why existing tools didn't work

There are image classification tools out there, but most of them have problems for research use:

**Cloud platforms require accounts and subscriptions.** Researchers are not always in a position to sign up for yet another service, get institutional approval, or pay a monthly fee for a tool they use occasionally.

**General purpose tools are not designed for research images.** Classifying a confocal microscopy image or a western blot is not the same as classifying a photo of a cat. Tools built for consumer images often struggle with the visual characteristics of research imagery.

**Existing tools assume you want their categories, not yours.** Most image classification services have their own taxonomies. Research labs have their own experimental vocabulary — and that vocabulary is what matters for organising their data.

**Privacy is a real concern.** In many research contexts, images cannot be sent to cloud services without institutional approval. Unpublished results, patient-adjacent imaging data, and proprietary experimental protocols are all reasons a researcher might not want their images leaving their own machine.

---

## What we wanted to build

A tool that:
- Runs on the researcher's own device with no required backend
- Uses the researcher's own categories, not ours
- Works with any AI provider the researcher already has access to, or none at all if they use Ollama locally
- Is fast to set up, easy to use, and doesn't require technical expertise
- Is completely free and open source so any researcher, at any institution, in any country can use it without barriers

lab-i is that tool. It is not trying to be a platform. It is not trying to build a business around researchers' data. It is a focused, local-first utility that does one thing well.

---

## Why open source

Research tools should be open. Researchers should be able to inspect what a tool does with their data, modify it for their specific needs, and share improvements with the community.

Open sourcing lab-i also means that if the original developer stops maintaining it, the community can keep it going. A useful research tool should not disappear because one person moved on.

---

## A note on scope

lab-i intentionally does not do everything. It classifies and organises images. It does not analyse them, quantify them, or produce measurements. There are excellent specialised tools for image analysis (Fiji/ImageJ, CellProfiler, QuPath) and lab-i is not trying to replace them.

The goal is to solve the organisation problem so that when researchers sit down with their analysis tools, their images are already where they should be.

---

If lab-i has saved you time in the lab, consider [supporting the project](https://buymeacoffee.com/sameermann). And if you have ideas for how it could work better for your workflow, open an issue on [GitHub](https://github.com/lab-intelligence/lab-i-app/issues) — feedback from actual researchers is what shapes where the project goes next.

Next: [Contributing](contributing.md)
