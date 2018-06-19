# Introduction to light synthesis

Guillaume.Bouchard@tweag.io

20 june, 2018

# Valeo lighting systems

- Virtual prototyping of (car) lamp

Challenges:

- Physically based rendering
- Finale images must look like photography
- Complex light paths (it was my PhD topic)

- Quality at all cost:

  - Polarisation
  - Wave interferences

---

![](output/images-6.png.png)

(One week of rendering on a 2010 high end workstation)

---

# Mercenaries engineering

- Animation movies, you may have seen some

Challenges:

- Complex scenes (lot of geometry, details, materials, textures, lampes)
- Artistic freedom

---

- Watch the trailer with me

https://www.youtube.com/watch?v=fEPqgSNLfK8

---

TODO: vampire example

---

# Image Synthesis

---

## Modelisation

![](output/images-2.png.png)

---

## Simulation

![](output/images-3.png.png)

---

## Examples

![](output/images-4.png.png)

---

## What is an image

![](output/images-17.png.png)

---

## Rendering Equation

![](output/images-18.png.png)
---

## Rendering Equation
![](output/images-19.png.png)
---

## Rendering Equation
![](output/images-20.png.png)
---

## Rendering Equation
![](output/images-21.png.png)
---

## Rendering Equation
![](output/images-22.png.png)
---

## Rendering Equation
![](output/images-23.png.png)
---

## Rendering Equation
![](output/images-24.png.png)
---

## Rendering Equation
![](output/images-25.png.png)
---

## Quantites

![](output/images-26.png.png)

---

Can we solve this equation ?

Too complex:

- Difficult to model in close form
- Lot of discontinuities

--> Monte Carlo

---

## Monte Carlo in 5 minutes

![](output/images-27.png.png)

---


## Monte Carlo

![](output/images-28.png.png)

---

## Lever of quality: Number of samples

![](output/images-29.png.png)

---

## Lever of quality: Sampling strategy

![](output/images-30.png.png)

---

## Example: uniform sampling

![](output/images-31.png.png)

---

## Example: smarter "importance" sampling

![](output/images-32.png.png)

---

TODO: an real example (blender live demo ?)

---

# How to sample a path?

---

![](output/images-37.png.png)

---

![](output/images-38.png.png)

---

![](output/images-39.png.png)

---

![](output/images-40.png.png)

---

![](output/images-61.png.png)

---

# Which strategy should I use?

---

![](output/images-42.png.png)

---

![](output/images-43.png.png)

---

![](output/images-43.png.png)

---

## Multiple importance sampling

![](output/images-45.png.png)

---

~[](output/images-46.png.png)

---

# A few other interesting topics

- Acceleration structures
- Adaptive sampling
- Volume sampling
- Many light

---

# Acceleration structures

- Ray test intersection: `O(n)`

TODO: schema

---

# Adative sampling

TODO: images

---

And now, let's code. Our first raytracer in ten minutes

Show code! Yeah.
