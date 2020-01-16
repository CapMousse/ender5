---
layout: default
title: Mods and improvements
nav_order: 8
---

# Mods and improvements
{: .no_toc}

## Table of content
{: .no_toc .text-delta}

1. TOC
{:toc}

---

## Printable mods

Many parts from the Ender 3 or the CR 10 can be used on the Ender 5. Don't be surprised if the listing include anything from theses printers

### Electronics

- [Main board cable protection](https://www.thingiverse.com/thing:3354725)
- [Control panel back cover](https://www.thingiverse.com/thing:3353394)
- [Control panel with raspberry back cover](https://www.thingiverse.com/thing:3628970)

### Extruder

- [Extruder Arm](https://www.thingiverse.com/thing:3595328)
- [Stepper motor mount](https://www.thingiverse.com/thing:3747071)

### Fan duct

- [CR-10 duct fan mod](https://www.thingiverse.com/thing:2221647)
- [CR-10 Fan Mod - Airflow optimisation](https://www.thingiverse.com/thing:2814127)
- [Petsfang Duct](https://www.thingiverse.com/thing:2759439) with [Ender-5 Base](https://www.thingiverse.com/thing:3343314)

### Bed

- [Heated bed cable strain relief](https://www.thingiverse.com/thing:3443100)
- [Bed supports](https://www.thingiverse.com/thing:3479330)

### Other

- [Silent auto home](https://www.thingiverse.com/thing:3349425)
- [Spool clamp](https://www.thingiverse.com/thing:3478552)

---

## Improvements

### Use 100% of the printable area

By default, Ender 3 and Ender 5 (Pro) have a X length and Y length of 220mm but it can go to 235mm for each axis.

To change those maximums, you will need to edit your firmware.

- *Marlin 1.1.X/2*: in the `Configuration.h` file, update the lines 878 to 879
- *TH3D*: in the `Configuration_backend.h` file, update the lines 2050 and 2051


```
#define X_BED_SIZE 235
#define Y_BED_SIZE 235
```