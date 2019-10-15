---
layout: post
title: "Attention"
date: 2019-10-15
---

**Attention is the mechanism that can learn to align input features to a certain output element and combine input features according to the learnt alignment to produce the target output.**

## In a general seq2seq task: 

{% raw %}
  $ X =[x_1, x_2, ... x_n] $ -> encoder 
  
  -> encoded context (c) -> 
  
  decoder -> $ Y = [y_1, y_2, ... y_m] $
{% endraw %}

An attention model ($ W_{attention} $) can be applied to the encoded input sequence to get a encoded context representation of the totality rather than the RNN proccessed information (only contains information of time steps till current reached word).

To produce a certain output $y_t$, it takes all the encoded hidden states $[h_1, h_2, ... h_n]$ (from a RNN, LSTM or bi-directional maybe) with the last decoder hidden state  $s_{t-1}$ to produce a set of weights $A_t =[a_{1t}, a_{2t}, ... a_{nt}]$ for each input time steps w.r.t the output time step t.

Where:

Decoder hidden state: $ s_t = f(s_{t−1},y_{t−1},c_t) $;

Alignment weight: $ a_{it} = \frac{exp(W_{attention}(h_i,s_{t-1}))}{\sum_{i'=1}^{n} exp(W_{attention}(h_i',s_{t-1}))} $.

The hidden context for $y_t$ can then be calculated as:

$$ c_t = \sum_{i=1}^{n} a_{it} * h_i $$.

## In a img classification task: 
