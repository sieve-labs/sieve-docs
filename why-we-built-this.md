# Why We Built This

Sieve exists because a frustrating but solvable problem kept coming up: sorting large numbers of images into categories — and no existing tool was addressing it in a way that actually worked for most people.

---

## The problem

People generate a lot of images. A single photo session can produce hundreds of files. Over weeks and months, this becomes thousands of images sitting in folders with names like `IMG_4823.jpg`, `scan_002_final_v3.tif`, or `untitled_export.png`.

At some point, someone has to go through all of them and figure out what they are. This is slow, tedious, and error-prone — especially when the person doing it wasn't the one who took the images, or when returning to a project after months away.

The manual tagging and organisation of images is a task that can take hours. Multiply that across a year, and it represents a significant amount of time that could be spent on more important work.

---

## Why existing tools didn't work

There are image classification tools out there, but most of them have problems:

**Cloud platforms require accounts and subscriptions.** Users are not always in a position to sign up for yet another service, get approval, or pay a monthly fee for a tool they use occasionally.

**General purpose tools are not designed for your categories.** Most image classification services have their own taxonomies. Users have their own vocabulary — and that vocabulary is what matters for organising their data.

**Privacy is a real concern.** In many contexts, images cannot be sent to cloud services without approval. Unpublished results, sensitive data, and proprietary materials are all reasons a user might not want their images leaving their own machine.

---

## What we wanted to build

A tool that:
- Runs on your own device with no required backend
- Uses your own categories, not ours
- Works with any AI provider you already have access to, or none at all if you use Ollama locally
- Is fast to set up, easy to use, and doesn't require technical expertise
- Is completely free and open source so anyone, anywhere can use it without barriers

Sieve is that tool. It is not trying to be a platform. It is not trying to build a business around your data. It is a focused, local-first utility that does one thing well.

---

## Why open source

Tools should be open. Users should be able to inspect what a tool does with their data, modify it for their specific needs, and share improvements with the community.

Open sourcing Sieve also means that if the original developer stops maintaining it, the community can keep it going. A useful tool should not disappear because one person moved on.

---

## A note on scope

Sieve intentionally does not do everything. It classifies and organises images. It does not analyse them, quantify them, or produce measurements. There are excellent specialised tools for image analysis (Fiji/ImageJ, CellProfiler, QuPath) and Sieve is not trying to replace them.

The goal is to solve the organisation problem so that when you sit down with your analysis tools, your images are already where they should be.

---

If Sieve has saved you time, consider [supporting the project](https://buymeacoffee.com/sameermann). And if you have ideas for how it could work better for your workflow, open an issue on [GitHub](https://github.com/sieve-sort/sieve-app/issues) — feedback from actual users is what shapes where the project goes next.

Next: [Contributing](contributing.md)
