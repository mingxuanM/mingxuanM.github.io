---
layout: post
title: "Pointer Attention in integer sorting"
date: 2019-10-23
---

**Pointer attention** is just a simple application of attention mechanism, which only produce **a pointer** to the most focused input element

[Here][pointer_attention] is my simple implementation of a pointer attention network with bi-directional gated-recurrent-unit as input encoder and a uni-directional GRU as previous output encoder. This network is applied to a list of random integer sorting task to evaluate its performance.

  [pointer_attention]: https://github.com/mingxuanM/pointer_attention_network

