# Label Set Management

A label set is a named list of categories that you want Sieve to sort your images into. This is the core of how Sieve works — you define the categories, Sieve does the sorting.

---

## What is a label set?

Think of a label set like a set of folders you want to end up with. If you want your images sorted into folders named Gel, Microscopy, Drosophila, and Petriplate, your label set contains exactly those four labels.

You can have as many label sets as you want, saved and ready to use. A research lab might have one label set for cell culture work, another for mouse experiments, and another for imaging sessions. Each is saved separately and can be selected at classification time.

---

## The default label set

Sieve comes with one built-in label set for biological research:

**Biology (default)**
- Drosophila
- Mice
- Insects
- Celegans
- Microorganisms
- Microscopy
- Gel
- Petriplate
- Biochemistry

You can use this as-is, edit it to fit your workflow, or create entirely new label sets.

---

## Creating a label set

1. Open Sieve and go to **Label Sets** from the main menu
2. Tap or click **New Label Set**
3. Give it a name — something descriptive like "Mouse Histology" or "PCR Gels"
4. Add your labels one by one using the **Add Label** button
5. Tap **Save**

Your new label set is now available to select when classifying images.

> **Screenshot placeholder — label set creation screen**

---

## Tips for writing good labels

The quality of your labels directly affects classification accuracy. A few things to keep in mind:

**Be specific but not too narrow.** A label like `Confocal Microscopy Z-Stack` is so specific that the AI may rarely match it confidently. A label like `Confocal` or `Microscopy` works better.

**Avoid overlapping labels.** If two labels describe things that look visually similar, the AI will struggle to choose between them. For example, `Microorganisms` and `Bacteria` might cause confusion. Pick one or combine them.

**Use plain, recognisable names.** The AI understands standard scientific and common terminology. Abbreviations or highly internal naming conventions may reduce accuracy.

**Keep the list focused.** A label set with 5–10 labels generally performs better than one with 30. If you have many categories, consider splitting them into multiple label sets for different sessions.

---

## Editing a label set

1. Go to **Label Sets**
2. Tap the label set you want to edit
3. Add, remove, or rename labels as needed
4. Tap **Save**

Changes take effect immediately for any future classification sessions.

---

## Deleting a label set

1. Go to **Label Sets**
2. Long press the label set (mobile) or use the options menu (desktop)
3. Tap **Delete** and confirm

Deleting a label set does not affect any images already sorted using it.

---

## Selecting a label set for classification

When you start a new classification session, Sieve will ask which label set to use. Tap the one you want and proceed.

You can also set a default label set in **Settings** if you mostly use the same one.

---

## Example label sets for different research domains

**Cell biology**
- HeLa Cells
- Neuron
- Fibroblast
- Stem Cell
- Tissue Section
- Fluorescence

**Mouse experiments**
- Brain Section
- Liver
- Kidney
- Tumor
- Whole Animal
- Behaviour

**PCR and gel work**
- Agarose Gel
- Western Blot
- SDS PAGE
- PCR Product
- Ladder

**Microscopy techniques**
- Brightfield
- Confocal
- Electron Microscopy
- Phase Contrast
- Fluorescence

Feel free to adapt any of these or build your own from scratch. See [Using Sieve for Anything](beyond-the-lab.md) for label set ideas outside of research.

Next: [The Gallery](gallery.md)
