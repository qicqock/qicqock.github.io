---
layout: page
title: Prompt-based Learning of Dialogue State Tracking
description: 
img: assets/img/Pftune_DS2/pftune.png
importance: 1
category: work
---

<p class="font-weight-bold">Research Project of POLBOT at <a href="https://www.etri.re.kr/intro.html">ETRI, Korea </a> mentored by <a href='https://scholar.google.com/citations?user=ls--5v0AAAAJ&hl=en'>Prof.Junseong Bang</a></p>

<h3>Introduction</h3>

POLBOT is an AI-based conversational voice bot that provides an automated reception service for call centers of <a href="https://minwon.police.go.kr/">Korean National Police Agency</a>. 

For effective reception, Dialogue State Tracking (DST) is one of the key modules of POLBOT that is responsible for extracting users’ intentions and requirements from dialogues.

However, Due to difficulties of acquiring well-anotated datasets from the police department, few-shot DST was a main topic of our research project.

<h3>Reserach Approach </h3>

Among few-shot methods, I was particularly interested in <a href="https://arxiv.org/abs/2203.01552">DS2</a> that redefines DST into sentence summarization. 

However, I found some inefficiencies of the training process of DS2 
    1. Because of the unique idea of redefinition, the approach requires an extra fine-tuning process, which needs additional computational resources for training.
    2. it is very challenging to optimize all of the parameters of a large model with very little data.

<p class="font-weight-bold">To address the issues while maintaining few-shot performance of DS2, I applied prompt-based learning. </p>


<h3>Training process</h3>

The training process of DS2 is 
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/Pftune_DS2/training_ds2.png" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Training process of DS2
</div>

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/Pftune_DS2/training_pf_ds2.png" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/Pftune_DS2/prompt_tune.png" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Training process of prompt learning DS2
</div>

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/Pftune_DS2/pftune.png" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    
</div>

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/Pftune_DS2/result.png" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    
</div>

We proposed FCN-BLA that Improved the architecture of a <a href="https://arxiv.org/abs/1707.09476">FCN-rLSTM</a> with BI-LSTM and Attention.

Compared to <a href="https://arxiv.org/abs/1707.09476">FCN-rLSTM</a>,  
    1. Changed to an Encoder-Decoder architecture  
    2. Bidirectionally containing spatio-temporal information from sequential images  
    3. Directly referring to encoded input features for dealing with an existing bottleneck problem 
