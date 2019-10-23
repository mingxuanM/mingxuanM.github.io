---
layout: post
title: "RL: Policy gradient - Actor-Critics"
date: 2019-10-24
---

**Policy gradient** method is a RL learning algorithm that tries to learing a **control policy** directly. This is a different perspective from Q-learning which tries to learn the Q-values, and draw a policy ($\epsilon greedy$) from the Q-values afterwards. The goal is to learn a policy that can maximize the expected accumulative reward from any state, the expected accumulative reward is defined by the Bellman equation:

$$$$

**Actor-Critics** is one of the most popular policy gradient algorithm that adopts a two network structure, with one (Actor) learns the policy and another (Critic) evaluate the policy at each step. The derivation behind AC can be found in this [fantastic post][AC].

  [AC]: https://towardsdatascience.com/understanding-actor-critic-methods-931b97b6df3f

[Here][policy_gradient] is my implementations of different policy gradient algorithms (AC, A2C), applied on a moving object catching task.

  [policy_gradient]: https://github.com/mingxuanM/Puck_Catching_Agent

_A more detailed explanation of the code shall come later_


## Links

https://towardsdatascience.com/understanding-actor-critic-methods-931b97b6df3f

https://github.com/mingxuanM/Puck_Catching_Agent