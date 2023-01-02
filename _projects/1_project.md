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

<h3>Research Approach </h3>

Among few-shot methods, I was particularly interested in <a href="https://arxiv.org/abs/2203.01552">DS2</a> that redefines DST into sentence summarization. 

However, I found some inefficiencies of the training process of DS2  
    1. Because of redefinition of DST, the approach requires an extra fine-tuning process, which needs additional computational resources for training.  
    2. it is very challenging to optimize all of the parameters of a large model with very little data.  

<p class="font-weight-bold">To address the issues while maintaining few-shot performance of DS2, I applied prompt-based learning. </p>


<h3>Prompt-Based methods of DST</h3>
I chose two different prompt learning strategies, Prompt Tuning and Prefix Tuning.

<h5><a href="https://arxiv.org/abs/2104.08691">Prompt Tuning</a></h5>
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/Pftune_DS2/prompt_tune.png" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Prompt Tuning
</div>

<h5><a href="https://arxiv.org/abs/2101.00190">Prefix Tuning</a></h5>
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/Pftune_DS2/pftune.png" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Prefix Tuning
</div>

<h3>Result</h3>
I obtained a 98% comparable score of fine-tuning with updating only 2% parameters of the BART-large model using prefix tuning.

My proposed application also showed almost similar accuracy of fine-tuning in various few-shot settings conducted on MultiWOZ 2.1 dataset.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/Pftune_DS2/result.png" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Result
</div>
    
<!-- <div class="row">
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
</div> -->
