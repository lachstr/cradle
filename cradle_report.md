---
header-includes:
   - \usepackage[margin=1in, headheight=0pt, headsep=0pt]{geometry}
title: Animating Newton's Cradle
author: Lachlan Macartney
date: June 4, 2020
---


# 1 Aim(Question posed and why its interesting)

The purpose of this project is to animate Newton's Cradle from first princples. Newton's Cradle has been animated before however usually via a 'physics-free' key-frame method or one reliant on a complicated physics engine. It will demonstrate how strikingly real world behavior can be computed with simple, first-principles approach mathematical framework. It will also make apparent the issues which arise with numerical calculus techniques.

# 2 Method(Basic approach)

``Newton's Cradle can be modelled as mutilple pendulums confined to swing along a single axis which undergo elastic collisions with one another. The pendulums rest such that there is a small amount of horizontal displacement between them.''

## 2.1 Fundamental Framework

We will define the mathematics required for a generalised set of $n$ independent pendulums, then compute their interactions in a cartesian coordinate system $(x,y)$ which we will call the Cradle's Frame. For each $i \in \{1, 2, 3, ... , n\}$ let the $i$th pendulum have length $\ell$, radius $r_i$ and mass $m_i$. It will also need some displacement $\Delta x_i$ along the $x$-axis, so that it 'almost touches' the others at rest. Each pendlum has a single degree of freedom along the axis $(\theta_i)$ in its own reference frame which obeys the differential equation of a pendulum;

$$\ddot{\theta_i} = -\frac{g}{\ell}\sin(\theta_i)$$

A transform to the Cradle's Frame can be computed by; 

$$T(\theta_i, \Delta x_{i}) = (\ell\sin(\theta_i) + \Delta x_i, -\ell\cos(\theta_i))$$

We will say that a collision occurs if for any two pendulums $i, j$;

$$ |T(\theta_i, \Delta x_{i}) - T(\theta_j, \Delta x_{j})| = r_i + r_j$$

If we say that such a collision is elastic, from first principles we will arrive at;

$$\dot{\theta}_{i,\textrm{final}} = \frac{m_i-m_j}{m_i+m_j} \dot{\theta}_{i,\textrm{initial}} + \frac{2m_j}{m_i+m_j} \dot{\theta}_{j, \textrm{initial}} \quad \textrm{and} \quad \dot{\theta}_{j,\textrm{final}} = \frac{2m_i}{m_i+m_j} \dot{\theta}_{i,\textrm{initial}} + \frac{m_j-m_i}{m_i+m_j} \dot{\theta}_{j, \textrm{initial}}$$

We may also add the condition that each pendulum mass has the same density $\rho$ such that $m_i$ and $r_i$ are related via $m_i=\frac{4\pi\rho}{3}r_i^3$. For the traditional Newton's Cradle with equal mass and radii pendlums the above collision formulae simplify. However, such a non traditional cradle will be explored.


# 3 Results(Notable results - the best or final output of code)

# 4 Conclusions(Answer to your question/Summary)
