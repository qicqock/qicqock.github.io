---
layout: page
title: Prompt Learning of Dialogue State Tracking
description: 
img: assets/img/Pftune_DS2/pftune.png
importance: 1
category: work
---

<p class="font-weight-bold">Research Project of POLBOT at <a href="https://www.etri.re.kr/intro.html">ETRI, Korea </a> mentored by <a href='https://scholar.google.com/citations?user=ls--5v0AAAAJ&hl=en'>Prof.Junseong Bang</a></p>

<h3>Introduction</h3>

POLBOT is an AI-based conversational voice bot service for <a href="https://minwon.police.go.kr/">Korean National Police Agency</a> that provides automated receptions  of public safety domains.

In POLBOT, Dialogue State Tracking(DST) plays a fundamental role in understanding user's requirements exposed during multi-turn conversations.

However, Due to limitations of acquiring dataset from the police department, I researched few-shot methods of DST and pre-trained language model(PLM).


<p class="font-weight-bold"> We proposed FCN-BLA and implemented real-time Traffic Analysis System.</p>

<h3>Training</h3>

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



If you find further information, There are our <a href="https://github.com/CapstonAIVC/IVCS">code</a> and <a href="/assets/pdf/capstone2022_final_report.pdf">final report(korean)</a>.
Footer
©
