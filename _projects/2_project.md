---
layout: page
title: Capstone Project
description: Traffic Analysis System based on FCN-BLA model
img: assets/img/capstone2022/capstone2022_model.png
importance: 2
category: work
---

<p class="font-weight-bold">1-year Capstone Project With <a href='https://www.gsu.edu/'>Georgia State University</a> mentoring by <a href='http://cai.csgsu.org/'>Prof.Zhipeng Cai</a></p>
<p class="font-weight-bold">Proposed FCN-BLA and implemented Real-time traffic analysis system for Intelligence Transportation System(ITS).</p>


<h2>FCN-BLA</h2>
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/capstone2022/capstone2022_model.png" title="FCN-BLA" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Model Structure of the model, FCN-BLA
</div>

proposed FCN-BLA that Improved the architecture of a <a href="https://arxiv.org/abs/1707.09476">FCN-rLSTM</a> with BI-LSTM and Attention.

Compared to <a href="https://arxiv.org/abs/1707.09476">FCN-rLSTM</a>,  
    1. Changed to an Encoder-Decoder architecture  
    2. Bidirectionally containing spatio-temporal information from sequential images  
    3. Directly referring to encoded input features for dealing with an existing bottleneck problem  
    
In <a href="https://gram.web.uah.es/data/datasets/trancos/index.html">Trancos Dataset</a>, obtained 4% performance improvement of count error as 4.205.

<h2>Traffic Analysis System</h2>
<div class="row justify-content-sm-center">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/capstone2022/capstone2022_input.png" title="model input" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    batch input of CCTV 1~8
</div>

<div class="row justify-content-sm-center">
    <div class="col-sm-4 mt-3 mt-md-0">
        {% include figure.html path="assets/img/capstone2022/capstone2022_system.png" title="system" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-4 mt-3 mt-md-0">
        {% include figure.html path="assets/img/capstone2022/capstone2022_client.png" title="client" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-4 mt-3 mt-md-0">
        {% include figure.html path="assets/img/capstone2022/capstone2022_android.png" title="android" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    System structure, client server, and an android implementation
</div>

The code is simple.
Just wrap your images with `<div class="col-sm">` and place them inside `<div class="row">` (read more about the <a href="https://getbootstrap.com/docs/4.4/layout/grid/">Bootstrap Grid</a> system).
To make images responsive, add `img-fluid` class to each; for rounded corners and shadows use `rounded` and `z-depth-1` classes.
Here's the code for the last row of images above:

{% raw %}
```html
<div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.html path="assets/img/6.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-4 mt-3 mt-md-0">
        {% include figure.html path="assets/img/11.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
```
{% endraw %}
