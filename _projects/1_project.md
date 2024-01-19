---
layout: page
title: RamBoAttack
description: Attack Against Deep Neural Network in Black-box settings
img: assets/img/project-img-1.jpg
importance: 1
category: work
related_publications: einstein1956investigations, einstein1950meaning
---

<!-- Every project has a beautiful feature showcase page.
It's easy to include images in a flexible 3-column grid format.
Make your photos 1/3, 2/3, or full width.

To give your project a background in the portfolio page, just add the img tag to the front matter like so:

    ---
    layout: page
    title: project
    description: a project with a background image
    img: /assets/img/12.jpg
    --- 
## RamBoAttack Against Deep Neural Network -->

Reproduce our results: [GitHub](https://github.com/RamBoAttack/RamBoAttack.github.io)

Check out our paper: [RamBoAttack: A Robust Query Efficient Deep Neural Network Decision Exploit](https://arxiv.org/abs/2112.05282)

Cite our research: 
```
@inproceedings{Vo2022,
    title = {RamBoAttack: A Robust Query Efficient Deep Neural Network Decision Exploit},
    year = {2022},
    journal = {Network and Distributed Systems Security (NDSS) Symposium},
    author = {Viet Quoc Vo, Ehsan Abbasnejad, Damith C. Ranasinghe},
}
```

#### ABSTRACT

Machine  learning  models  are  critically  susceptibleto  evasion  attacks  from  adversarial  examples.  Generally,  ad-versarial  examples—modified  inputs  deceptively  similar  to  the original  input—are  constructed  under  whitebox  access  settings by  adversaries  with  full  access  to  the  model.  However,  recent attacks  have  shown  a  remarkable  reduction  in  the  number  ofqueries  to  craft  adversarial  examples  using  blackbox  attacks. Particularly  alarming  is  the  now, practical,  ability  to  exploitsimply the classification decision (hard label only) from a trainedmodel’saccess   interfaceprovided   by   a   growing   number   of Machine  Learning  as  a  Service  (MLaaS)  providers—including Google, Microsoft, IBM—and used by a plethora of applications in corporating  these  models.  An  adversary’s  ability  to  exploitonly the predicted label from a model-query to craft adversarial examples  is  distinguished  as  a decision-based attack.

In   our   study,   we   first   deep-dive   into   recent   state-of-the-art  decision-based  attacks  in  ICLR  and  S&P  to  highlight  the costly nature of discovering low distortion adversarial employing approximate  gradient  estimation  methods.  We  develop  a robust class  of query  efficient attacks  capable  of  avoiding  entrapment in a local minimum and misdirections from noisy gradients seen in gradient estimation methods. The attack method we propose, RamBoAttack,  exploits  the  notion  of  Randomized  Block  Coordi-nate Descent to explore the hidden classifier manifold, targeting perturbations  to  manipulate  only  localized  input  features  to address  the  issues  of  gradient  estimation  methods.  Importantly, the RamBoAttack is  demonstrably  more  robust  to  the  different sample inputs available to an adversary and/or the targeted class. Overall,  for  a  given  target  class, RamBoAttackis  demonstrated to be more robust at achieving a lower distortion within a given query  budget.  We  curate  our  extensive  results  using  the  large-scale  high  resolution ImageNet dataset  and  open-source  our attack,  test  samples  and  artifacts  on [GitHub](https://github.com/RamBoAttack/RamBoAttack.github.io).

<!-- <div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/1.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/3.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/5.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Caption photos easily. On the left, a road goes through a tunnel. Middle, leaves artistically fall in a hipster photoshoot. Right, in another hipster photoshoot, a lumberjack grasps a handful of pine needles.
</div> -->
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/project-image-1.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Figure 3: Grad-CAM tool visualizes salient features of the starting image or target class: **digital watch**. Perturbation heat map (PHM) visualizes the normalized perturbation magnitude at each pixel. Comparing different pertur-bations crafted by different attacks highlights that the localized perturbations yielded  by  RamBoAttack  concentrate  on  salient  areas  illustrated  by  GRAD-CAM  and  embeds  these  targeted  perturbations  in  the  source  image  to  fool the classifier to predict the target class; even though, RamBoAttack does not exploit the knowledge of salient regions to generate perturbations.
</div>

<!-- You can also put regular text between your rows of images.
Say you wanted to write a little bit about your project before you posted the rest of the images.
You describe how you toiled, sweated, *bled* for your project, and then... you reveal its glory in the next row of images. -->


<!-- <div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.html path="assets/img/6.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-4 mt-3 mt-md-0">
        {% include figure.html path="assets/img/11.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    You can also have artistically styled 2/3 + 1/3 images, like these.
</div> -->


<!-- The code is simple.
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
{% endraw %} -->
