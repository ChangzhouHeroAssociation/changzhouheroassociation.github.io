--- 
layout: page 
title: elegant
Policy background: grey 
---

<div class="col-lg-12 text-center">
    <h2 class="section-heading text-uppercase">风采展示</h2>
    <div class="container">
        <div class="row">
            {% for project in site.platform %}
            <div class="col-md-4 col-sm-6 portfolio-item">
                 <img class="img-fluid" src="{{ project.caption.thumbnail }}" alt="">
                    <div class="portfolio-caption">
                     <a class="portfolio-link" data-toggle="modal"   index="project.caption.title"  style="display:block; height: 100%; width: 100%;" href="https://jun-mo.github.io/ho/exhibition"  >
                      {{ project.caption.title }}
                       </a>
                    </div>  
            </div>
            {% endfor %}
        </div>
    </div>
</div>
