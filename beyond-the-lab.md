# Using Sieve for Anything

Sieve works well for research, but the core idea — give it images, give it labels, it sorts them — works for almost anything. If you can write a list of categories, Sieve can sort images into them.

This page shows a few examples outside the lab to help you think about what's possible.

---

## The underlying idea

Sieve does not know anything about biology specifically. It does not have a built-in understanding of gels or microscopy. All it does is show your image to an AI vision model and ask it to pick the best match from your label list.

This means your label list defines what the app does. Change the labels, and you change what the app is for.

---

## Example: Vehicles

**Use case:** You have a large collection of vehicle photos — maybe from a fleet, an auction, or a photography project — and want to sort them by type.

**Label set: Vehicles**
- Car
- Motorcycle
- Truck
- Bus
- Bicycle
- Van
- Scooter

Point Sieve at a folder of vehicle images, select this label set, and you will end up with a sorted folder structure:

```
/sorted/
  /Car/
  /Motorcycle/
  /Truck/
  /Bus/
```

> **Screenshot placeholder — vehicle classification example**

---

## Example: Food photography

**Use case:** A food blogger or researcher has thousands of food photos and wants them organised by dish or category.

**Label set: Food**
- Pasta
- Salad
- Dessert
- Soup
- Grilled
- Breakfast
- Beverage

---

## Example: Wildlife field photography

**Use case:** A field researcher returns from an expedition with thousands of camera trap images and needs to sort them by species.

**Label set: Wildlife**
- Deer
- Fox
- Badger
- Bird
- Rabbit
- Empty (no animal present)
- Unknown

The `Empty` and `Unknown` labels are worth adding for any wildlife use case — many camera trap images capture nothing, and having an explicit label for them means they get sorted cleanly rather than being misclassified.

---

## Example: Quality control

**Use case:** A small manufacturer needs to sort product photos into pass and fail categories for quality review.

**Label set: QC**
- Pass
- Defect Surface
- Defect Shape
- Defect Colour
- Incomplete

This is a simple binary-plus workflow where most images go to Pass and the flagged ones go into specific defect categories for review.

---

## Example: Document and paperwork scanning

**Use case:** Sorting scanned documents into categories before archiving.

**Label set: Documents**
- Invoice
- Receipt
- Contract
- Letter
- Form
- ID Document
- Other

---

## Example: Plant health monitoring

**Use case:** A horticulturist or agronomist photographs plants regularly and wants images sorted by health status.

**Label set: Plant Health**
- Healthy
- Wilting
- Pest Damage
- Fungal
- Nutrient Deficiency
- Flowering

---

## How to set up a non-lab workflow

The process is identical to any other Sieve workflow:

1. Open Sieve and go to **Label Sets**
2. Create a new label set with your categories
3. Go to the main classify screen
4. Select your images or folder
5. Select your new label set
6. Tap **Classify**

That is it. Sieve does not need to be told what kind of images you have. The AI figures it out from the image itself combined with your label list.

---

## Tips for non-lab use cases

**Add an "Other" or "Unsure" label.** For any real-world dataset, some images won't fit neatly into your categories. Adding an explicit catch-all label gives the AI somewhere to put those images rather than forcing a bad match.

**Test with a small batch first.** Before running 2,000 images, run 20 and review the results. If accuracy looks off, adjust your label names and try again.

**Confidence scores matter here too.** Images flagged as uncertain (below 0.6) are worth reviewing regardless of use case. In a QC workflow a false pass is a much bigger problem than in a research workflow.

**Your labels don't have to be categories.** They could also be attributes. For example: `Daytime`, `Nighttime`, `Indoors`, `Outdoors` — this would sort images by context rather than subject.

---

Sieve is essentially a general purpose image sorting tool that works well for research. The more clearly you define your label set, the better it works.

Next: [FAQ](faq.md)
