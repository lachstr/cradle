---
title: Animating Newton's Cradle
author: Lachlan Macartney
date: June 4, 2020
---

# 1 Aim(Question posed and why its interesting)

The purpose of this project is to animate Newton's Cradle from first princples. Newton's Cradle has been animated before however usually via a 'physics-free' key-frame method or one reliant on a complicated physics engine. It will demonstrate how strikingly real world behavior can be computed with simple, first-principles approach mathematical framework. It will also make apparent the issues which arise with numerical calculus techniques.

# 2 Method(Basic approach)

*``Newton's cradle can be modelled as mutilple pendulums confined to swing along a single axis which undergo elastic collisions with one another. The pendulums rest such that there is a small amount of horizontal displacement between them.''*

## 2.1 Equal mass pendulums

- Has its own 1-dimensional co-ordinate system ($\theta_i$)
- Obeys differential equation $$\ddot{\theta_i} = -\frac{g}{\ell}\sin(\theta_i)$$
- Has some $\Delta x_i$ along the $x$-axis, so they are 'almost touching' at rest.

## 2.2 Equal density pendulums

- Has length $\ell$, radius $r_i$, mass $m_i=\frac{4\pi\rho}{3}r_i^3$ where $\rho$ is a metal density.



# 3 Results(Notable results - the best or final output of code)

# 4 Conclusions(Answer to your question/Summary)
