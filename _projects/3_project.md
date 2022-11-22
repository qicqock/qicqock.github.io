---
layout: page
title: HoloLens 2 Project
description: XR Interface for POLBOT on Microsoft HoloLens 2
img: assets/img/7.jpg
importance: 3
category: work
---

<p class="font-weight-bold">Project with <a href='https://www.etri.re.kr/intro.html'>ETRI, Korea</a> (collaborated with <a href='https://scholar.google.com/citations?user=ls--5v0AAAAJ&hl=en'>Prof.Junseong Bang</a>)</p>

<h3>Introduction</h3>

POLBOT is an AI-based conversational voice bot service for <a href="https://minwon.police.go.kr/">Korean National Police Agency</a> that recognizes the voice on the phone and seeks to understand the intention of the caller to provide effective automated receptions.
 
By analyzing the voice from multiple speakers in real time, POLBOT can classify speakers and understand their intentions, which allows to provide automated voice responses to callers.

<p class="font-weight-bold">On the necessity of digital conversion of call centers, we developed an XR interface for POLBOT on Microsoft HoloLens 2.</p>


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


<h3>Exhibition</h3>
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

the project was exhibited at <a href="http://www.aiexpo.co.kr/">AI Expo Korea, 2022</a> demonstrating 
