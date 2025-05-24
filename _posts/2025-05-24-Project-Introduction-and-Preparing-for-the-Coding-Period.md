---
title: "Project Introduction and Preparing for the Coding Period"
date: 2025-05-24 00:00:00 +0800
categories: [GSoC]
tags: [GSoC]
---

## Project Introduction

As part of Google Summer of Code 2025, I’ll be working with the SymPy organization on the project:
**“Classical Mechanics: Implement Wrapping Geometry and Pathways for Musculoskeletal Modeling”**.
Here is [My GSoC Project Page](https://summerofcode.withgoogle.com/programs/2025/projects/uvXG3nzX)

The goal of this project is to enhance SymPy’s symbolic mechanics capabilities by introducing **wrapping geometries** that allow modeling of how forces wrap around anatomical surfaces—crucial for realistic musculoskeletal simulations.

This work involves computing symbolic **geodesics** (shortest paths) and **geodesic tangent vectors** (force directions) on several 3D surfaces.

### Key Definitions

* `wrapping geometry`
  A surface (like a cone, ellipsoid, or torus) that a force-carrying structure wraps around, affecting the force direction and length.

* `geodesic`
  The shortest path between two points on a surface. On a curved surface, it bends while remaining on the surface to minimize distance.

The project will introduce the following classes to `sympy.mechanics`:

* `WrappingCone` – models a right circular cone
* `WrappingEllipsoid` – models a spheroidal shape
* `WrappingToroid` – models a torus

Each class will support symbolic computation of geodesic lengths and endpoint tangent vectors.

---

## Preparing for the Coding Period

During the community bonding period, I had my first meeting with my mentor **Hwayeon Kang**. We:

* Reviewed the project timeline and development milestones
* Finalized a weekly meeting schedule
* Decided to begin with **Phase 1: Conical Wrapping Geometry**

We'll start by implementing the `WrappingCone` class. Since cones are *developable surfaces*, they can be unfolded into a 2D sector—making it possible to derive exact symbolic expressions for geodesics and their tangent directions.

Initial work will focus on:

* Implementing `point_on_surface`, `geodesic_length`, and `geodesic_end_vectors` methods
* Writing tests and documentation
* Adding an example

Looking forward to diving deeper into the implementation and sharing progress, holdups and learnings as the project develops!
