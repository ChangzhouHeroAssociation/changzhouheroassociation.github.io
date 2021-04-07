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
                <a class="portfolio-link" data-toggle="modal"  href="exhibition" index="project.caption.title"  style="display:block; height: 100%; width: 100%;" >
                    <img class="img-fluid" src="{{ project.caption.thumbnail }}" alt="">
                </a>
                <div class="portfolio-caption">
                    <h4>{{ project.caption.title }}</h4>
                </div>
            </div>
            {% endfor %}
        </div>
    </div>
</div>
