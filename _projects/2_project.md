---
layout: page
title: Traffic Analysis System based on FCN-BLA model
description: Capstone Project from July,2021 to June, 2022
img: assets/img/capstone2022/capstone2022_model.png
importance: 2
category: work
---

<p class="font-weight-bold">1-year Capstone Project With <a href='https://www.gsu.edu/'>Georgia State University</a> mentoring by <a href='http://cai.csgsu.org/'>Prof.Zhipeng Cai</a></p>
<p class="font-weight-bold">We Proposed FCN-BLA and implemented Real-time traffic analysis system for Intelligence Transportation System(ITS).</p>


<h3>FCN-BLA</h3>

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/capstone2022/capstone2022_model.png" title="FCN-BLA" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Model Structure of the model, FCN-BLA
</div>

We proposed FCN-BLA that Improved the architecture of a <a href="https://arxiv.org/abs/1707.09476">FCN-rLSTM</a> with BI-LSTM and Attention.

Compared to <a href="https://arxiv.org/abs/1707.09476">FCN-rLSTM</a>,  
    1. Changed to an Encoder-Decoder architecture  
    2. Bidirectionally containing spatio-temporal information from sequential images  
    3. Directly referring to encoded input features for dealing with an existing bottleneck problem  
    
In <a href="https://gram.web.uah.es/data/datasets/trancos/index.html">Trancos Dataset</a>, we obtained 4% performance improvement of count error as 4.205.

  
<h3>Traffic Analysis System</h3>
  
<div class="row justify-content-sm-center">
    <div class="col-sm-6 mt-3 mt-md-0">
        {% include figure.html path="assets/img/capstone2022/capstone2022_input.png" title="model input" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-6 mt-3 mt-md-0">
        {% include figure.html path="assets/img/capstone2022/capstone2022_system.png" title="system" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    batch input 
</div>

Using FCN-BLA, we designed Traffic Analysis System for real-time vehicle counting of multiple CCTVs.  
For real-time inference, we used HLS(HTTP Live Streaming) and Socket Programming.  
To deal with sudden overloads of model requests, we made an waiting queue that stacks batches from multiple CCTVs.  


<h3>Application</h3>
<div class="row justify-content-sm-center">
    <div class="col-sm-6 mt-3 mt-md-0">
        {% include figure.html path="assets/img/capstone2022/capstone2022_service.png" title="service" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-6 mt-3 mt-md-0">
        {% include figure.html path="assets/img/capstone2022/capstone2022_android.png" title="android" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Web Application and Android app(Namhaeseon Chojeon 2nd Bridge)
</div>

We applied our Traffic Analysis System to a National Highway API provided by <a href="https://www.its.go.kr/map/cctv"> National Transport Information Center</a>, Korea and implemented a Web-based service and an android app.



You can find our <a href="https://github.com/CapstonAIVC/IVCS">code</a> and <a href="">final report</a>
