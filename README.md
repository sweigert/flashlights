# Flashlights

This is a fun little project using differentiable programming to solve a complex task.
The idea is to draw any painting with flashlights.

![4.gif](material/4.gif)
_This is "[The Bedroom](https://www.vangoghmuseum.nl/en/collection/s0047v1962)" from Van Gogh_

[slides.pdf](material/slides.pdf) has the slides of my [decompiled](https://decompiled.de/) 2026 talk.

The jupyter notebooks contain the different live coding steps.
* [1.ipynb](code/1.ipynb)
  * The most straight-forward implementation of the drawing algorithm.
  * Cannot be trained because it contains python control-flow statements which cannot be tracked by pytorch.
* [2.ipynb](code/2.ipynb)
  * Vectorized pixel loop
  * Still cannot be trained because the loss has no gradient
* [3.ipynb](code/3.ipynb)
  * First version that can be trained because we use sigmoid now
* [4.ipynb](code/4.ipynb)
  * Add an additional parameter: Lens focus
  * This is where the gif comes from
* [5.ipynb](code/5.ipynb)
  * Introduce an additional cost for every flashlight proportional to its brightness
  * This allows to find the minimal number of required flashlights
