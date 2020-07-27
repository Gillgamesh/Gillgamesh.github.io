---
layout: project
date: 2020-02-05
title: Boneless Relativity
---

## Boneless Relativity

### Links

* [Source](https://gitlab.com/Gillgamesh/boneless_relativity)

### Description

A basic 3d particle physics simulator that does electromagnetic and gravitational forces. The simulation is done in Planck units (G=Ke=Kb=c=1) with each pixel equivalent to a planck length. Still demonstrates inverse square law. For sake of demonstration, editable modifiers have been added to magnetic, electric, and gravitational forces, with the default values being the ones found to be most interesting.
ie without the modifiers, with m=v=q=1 for both particles, gravitational and electric force are equal in magnitude, and assuming the particles to be parellel as is the magnetic force (this will likely not be the case after a while though) (you could specify a modifier for the strengths of each field, or set the charge to 0 to get a gravity simulator). Uses Processing's 3D rendering service and ControlP5 to save setup time. Really useful demonstration for classroom environments; made for my AP Physics C class senior year.

As an example, here's two charges with equal charge and mass, but one has a velocity slightly less than the other:while we initially have an oscillation due to gravitational/magnetic attraction vs electric repulsion, as their slightly different velocities and resultant difference in x position build up, we see that the oscillation along the y axis disapears. Here, the green gives you the gravitational force, blue the magnetic field direction, and the red the electric
force:

![Boneless Relativity](/assets/img/boneless-relativity1.gif)
