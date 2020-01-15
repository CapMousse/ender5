---
layout: default
title: Troubleshooting
nav_order: 6
---

# Troubleshooting
{: .no_toc }

## Table of content
{: .no_toc .text-delta}

1. TOC
{:toc}

---

## Maintenance flow chart

![Maintenance flow chart](/files/troubleshooting/maintenance-flow-chart.jpg)

---

## Bad adhesion

- Check if the bed is correctly leveled. Get some help [here](%{link pages/maintenanec.md%}#bed-leveling)
- Check if the surface if clean. Use Isopropol alcohol to clean the bed.
- Check if the frame is correctly aligned. Some Ender 5 can have the top frame slightly skwed.
- Check you z-offset.

---

## Warped bed

It is common for printers of this price range to get a slightly warped bed. But it can be mitigated with some solutions, from easy and free to more complexe and expensive :

- [Manual Bed Mesh Leveling](https://www.youtube.com/watch?v=vcxM7-VK44k) with an upgraded firmware can help you map the bed and prevent bad first layer.
- A glass bed can completely flatten the bed and add a beautifull first layer to any prints.
- [Installing a BL Touch](https://www.youtube.com/watch?v=Cp3D_1vJpvM) to automatically map the bed before printing.


---

## Squashed print

Some Ender 5 come with a new Z Axis lead screw with a step per milimeters of 800 instead of 400. If your firmware still use 400 step/mm, all print will look squased and with half the z height.

### GCode only
{: .no_toc }

You can easily update the printed settings by sending gocde : `M92 Z800`

### Marlin 2.0.X and Marlin 1.1.X
{: .no_toc }

In the `Configuration.h` file, edit the `DEFAULT_AXIS_STEPS_PER_UNIT` instruction:

```
#define DEFAULT_AXIS_STEPS_PER_UNIT   { 80, 80, 800, 93 }
```

### TH3D
{: .no_toc }

In the `Configuration.h` file, uncomment the line 422:

```
#define ENDER5_NEW_LEADSCREW
```

---

## Bad origin

If after a firmware upgrade (Marlin, TH3D, ...) your new origin position is the oposite of the endstop and you want to fix this issue, you will need to edit the configuration file and reflash the printer.

### Marlin 1.1.X and 2.0.X
{: .no_toc }

In the file `Configuration.h`, lines 506 to 508, change the endstop position to use `XMIN` and `YMIN`:

```c
#define USE_XMIN_PLUG
#define USE_YMIN_PLUG
#define USE_ZMIN_PLUG
```

You will need to disable steppers invert from lines 847 to 849:

```c
#define INVERT_X_DIR false
#define INVERT_Y_DIR false
#define INVERT_Z_DIR true
```

And finally you need to edit the correct home direction from lines 873 to 871:

```c
#define X_HOME_DIR -1
#define Y_HOME_DIR -1
#define Z_HOME_DIR -1
```

### TH3D
{: .no_toc }

In the file `Configuration_backend.h` change the lines 2983 to 2985 to use `XMIN` and `YMIN`:

```c
#define USE_XMIN_PLUG
#define USE_YMIN_PLUG
#define USE_ZMIN_PLUG
```

In the same file, lines 2000 and 2001, change steppers invertion to false:

```c
#define INVERT_X_DIR false
#define INVERT_Y_DIR false
```

You will also need to setup the home correct home directions from lines 3017 to 3019

```c
#define X_HOME_DIR -1
#define Y_HOME_DIR -1
#define Z_HOME_DIR -1
```