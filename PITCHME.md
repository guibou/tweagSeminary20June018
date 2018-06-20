# Introduction to light synthesis

Guillaume.Bouchard@tweag.io

20 june, 2018


---

# Valeo lighting systems

- Virtual prototyping of (car) lamp

Challenges:

- Physically based rendering
- Finale images must look like photography
- Complex light paths (polarisation, interferences)

---

![](output/images-6.png.png)

(One day of rendering on a 2010 high end workstation)


---


# Mercenaries engineering

- Animation movies, you may have seen some

Challenges:

- Complex scenes (lot of geometry, details, materials, textures, lampes)
- Artistic freedom

---

![](mune.jpg)


---

- Watch the trailer with me

https://www.youtube.com/watch?v=fEPqgSNLfK8

---

## Artistic freedom

![](vampire.png)

---

# Image Synthesis

---

## Modelisation

![](output/images-2.png.png)

---

## Simulation

![](output/images-3.png.png)


---

## What is an image?

![](output/images-17.png.png)

---

## Rendering Equation

![](output/images-18.png.png)
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

# Materiel models

---

## Diffuse surface

![](materials/diffuse.png)

$$f(\omega_i, \omega_o) \propto C$$

---

## Glossy surface

![](materials/glossy.png)

$$f(\omega_i, \omega_o) \propto |\omega_i . n| ^ p$$

---

## Perfect mirror

![](materials/mirro.png)

$$f(\omega_i, \omega_o) \propto \delta (\omega_o - reflect(\omega_i))$$

---

## Perfect glass

![](materials/glass.png)

$$f(\omega_i, \omega_o) \propto \delta (\omega_o - refract(\omega_i))$$

(Snell's law)

---

## Material model in action

(Blender live demo)

---

# How to render?

---

- Can we solve the rendering equation?

- Too complex:

- --> Monte Carlo

---

## Monte Carlo in 5 minutes

![](output/images-27.png.png)

---


## Monte Carlo

![](output/images-28.png.png)

---

## Number of samples

![](output/images-29.png.png)

---

## Sampling strategy

![](output/images-30.png.png)

---

## Example: uniform

![](output/images-31.png.png)

---

## Example: "importance"

![](output/images-32.png.png)

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

![](output/images-44.png.png)

---

## Multiple importance sampling

![](output/images-45.png.png)

---

![](output/images-46.png.png)

---

# A few other interesting topics

---

## Acceleration structures

- Ray test intersection: `O(n)`

![](withoutBoxes.png)

---

## Acceleration structures

![](withBoxes.png)

---

## Adaptive sampling

![](no_adaptive.png)

---
## Adaptive sampling: heat map

![](heat_adaptive.png)

---


## Numbers

- 4K images (8 millions pixels), 100 layers, stereo
  - --> 25 Giga bytes of memory just for the final image

- from a few to millions of lights
- millions of geometry instances (composed of millions of triangles)

- One scene with 40 Giga bytes of memory for transformations matrices

- The little prince: 1 Tera bytes of texture in one image

---

## Numbers

- 25 images / second
- 1h30 movies

---

# Trivia: My first haskell project

- With a friend
- Haskell ray tracer
- I was supposed to teach him image synthesis
- We tried Haskell, because it looked boring (who uses types in 2015?)

https://github.com/gbataille/halray

---

# SmallPTHS

https://github.com/guibou/smallPTHS


- An experiment on raytracing / haskell / performance
- Goal: match the performance of `smallpt.cpp`, a reference implementation

- Laptop: Intel Core i7-4700HQ @ 2.4 GHz (4 cores, 8 threads) : 1.40x slower in linear, 1.7x slower in parallel.
- Workstation: Intel Core i7-6800K CPU @ 3.40GHz (6 cores, 12 threads) : 1.60x slower in linear, 3.2x slower in parallel.

- Great (and there is still a space leak and allocation in the main loop)
---

# Conclusion

- Thank you
- Questions ?

---

# Backup slides

---

## Rendering Equation
![](output/images-19.png.png)
---

## Rendering Equation
![](output/images-20.png.png)
---

## Quantites

![](output/images-26.png.png)
