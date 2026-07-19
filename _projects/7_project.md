---
layout: page
title: Efficient Domain Adaptation
description: Remote Sensing with limited data 🎉
img: assets/img/embedding.png
importance: 7
category: work
---

__Collaboration:__ [Defence Science and Technology Group (DSTG)](https://www.dst.defence.gov.au/)

__Abstract__

Few-shot learning is critical for data-scarce domains like remote sensing, but foundation models like CLIP struggle when novel concepts are poorly separated in pretrained latent spaces. To optimize performance with minimal parameters, this study evaluates parameter-efficient fine-tuning (PEFT) methods. Results show Low-rank Adaptation (LoRA) is highly effective, particularly for indistinguishable classes. Additionally, we propose a lightweight steering-vector-based mechanism for targeted representation modulation using significantly fewer parameters. Integrated with existing techniques, this approach consistently boosts downstream performance, demonstrating the value of structured, representation-aware adaptation in data-scarce environments like remote sensing.

In this study, we investigated different methods in zero-shot and few-shot settings:

    ---
    - Model soup
    - Model ensemble
    - Cache model/ Tip-Adapter
    - Clip-Adapter
    - APE
    - Task Residual
    - LoRA
    - Activate Steering Vector
    ---

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/combine.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Visualization of different images from remote sensing dataset <strong>x-View1</strong>.
</div>
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/1466_png.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/2399_png.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Visualization of different images from remote sensing dataset <strong>x-View1</strong>.
</div>
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/embedding.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Embedding visualization of dataset __x-View1__.
</div>
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/text embedding similarity.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Class similarity visualization across 60 novel categories in the xView-1 dataset. Feature similarities are computed using text embeddings from both the pre-trained RemoteCLIP model and its LoRA fine-tuned counterpart. The comparison demonstrates that while numerous novel classes overlap significantly in the original pretrained latent space, LoRA fine-tuning successfully adapts the text encoder to expand the margins between these classes.
</div>

We propose __Adaptive Steering Vector (AdaSV)__, a learnable framework that embeds __Trainable Steering Vectors (TSVs)__ across layers to generate gradual representation shifts. This approach aims to enhance class distinction using substantially fewer parameters while matching the performance of current few-shot adaptation methods.

<div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/tsv.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-4 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/table.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Left figure shows how to construct a steering vector and add to a transformer layer. Right figure shows the results on CIFAR-10 and x-View 1.
</div>
