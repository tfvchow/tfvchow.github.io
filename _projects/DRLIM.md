---
layout: page
title: Deep Learning
description: Deep Reinforcement Learning and Operations Management - A Preliminary Study for Next GRF Applications
img: assets/img/DNN.png
importance: 3
category: In Progress
related_publications:
---

The team is grateful to receive funding from the following sources:

- Departmental General Research Fund from PolyU (HKD 63,552)

<div class="row">
    <div class="col-sm-3 mt-md-0">
    </div>
    <div class="col-sm-6 mt-md-0">
        {% include figure.html path="assets/img/Learning_Curve.png" title="Learning curve of a failing agent" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-3 mt-md-0">
    </div>
</div>
<div class="caption">
    Learning curve of a failing agent (Picture: Machine Learning Memes for Convolutional Teens)
</div>

It goes without saying that deep learning has been a hot topic in the past decade, as seen in examples like AlphaGo and more recently ChatGPT. This project aims to explore the potential of deep reinforcement learning (DRL) in inventory management, targeting problem types that are hard to obtain optimal solutions and structural results for.

> In a recent book reviewing the latest issues in supply chain management, Snyder and Shen (2019) wrote that "[l]ost-sales problems with nonzero lead times are still, in many respects, an open problem and are an active area of research."

In fact, lost sales is unlikely to be precisely recorded, unless you will count how many times you turned away an unsatisfied customer. This means the observed data is censored, further complicating the problem, let alone that the suppliers aren't always reliable (orders might not be fulfilled in full or in time). Chen et al. (2024) is the only paper considering all three issues (lost-sales with lead time, censored demand, and uncertain supply) simultaneously, developed a highly-tailored learning algorithm for the problem.

We choose DRL instead as the learning algorithm because it is a natural fit for the problem. Simply put, think of managing inventory level as a game. In each round, the player (the inventory manager) makes a decision (the order quantity) based on the current state (the inventory level) and receives a reward or penalty (the profit or loss). This analogy is not rocket science, and that is why many researchers have tried to apply DRL to inventory management, as reviewed in Boute et al. (2021).

In this project, we will first focus on simple inventory problems (with lost sales and random uncensored demand only). Once we acquire some experience in training a DRL-based decision-making agent, we will move on to the problem in Chen et al. (2024).

>The ultimate goals of this project is facilitating: (i) applications of external grants with a research problem searching a [quasi-holy-grail in AI](https://aws.amazon.com/what-is/artificial-general-intelligence/) and (ii) reaching out to industrial and academic partners for collaboration.

**Objectives:**

- Write codebase for the simulation environment and the DRL algorithm.
- Train a DRL-based decision-making agent for simple inventory problems to attain (near-)optimal performance.
- Document the training process systematically for future reference.
- Extend the DRL-based decision-making agent to the problem in Chen et al. (2024).

**Reference(s):**

- Lawrence V. Snyder, Zuo-Jun Max Shen, *Fundamentals of Supply Chain Theory*, 2nd Edition, John Wiley & Sons, 2019.
- Boxiao Chen, Jiashuo Jiang, Jiawei Zhang, Zhengyuan Zhou, [Learning to Order for Inventory Systems with Lost Sales and Uncertain Supplies](https://arxiv.org/abs/2207.04550), *To Appear in Management Science*.
- Robert N. Boute, Joren Gijsbrechts, Willem van Jaarsveld, Nathalie Vanvuchelen, Deep reinforcement learning for inventory control: A roadmap, *European Journal of Operational Research*, 298(2), 401-412, 2022.
