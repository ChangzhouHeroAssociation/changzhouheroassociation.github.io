<!-- Portfolio Grid -->
<!-- Navigation -->
  <nav class="navbar navbar-expand-lg navbar-dark fixed-top" id="mainNav" style="background-color:#212529">
    <div class="container">
	  <a class="navbar-brand js-scroll-trigger" href="{{ site.baseurl }}/#">
          {%- if site.logo -%}
            <img height="{{ site.logo.height | default: 52 }}" src="{{ site.logo.path }}"/>
          {%- else -%}
            {{ site.title }}
          {%- endif -%}
      </a>
      <button class="navbar-toggler navbar-toggler-right" type="button" data-toggle="collapse" data-target="#navbarResponsive" aria-controls="navbarResponsive" aria-expanded="false" aria-label="Toggle navigation">
        Menu
        <i class="fas fa-bars"></i>
      </button>
      <div class="collapse navbar-collapse" id="navbarResponsive">
        <ul class="navbar-nav text-uppercase ml-auto">
		{%- for link in site.data.navigation[site.locale].nav -%}
		  <li class="nav-item">
		  {%- if link.url -%}
		    <a class="nav-link js-scroll-trigger" href="{{ link.url }}">{{ link.title }}</a>
		  {%- else if link.section -%}
		    <a class="nav-link js-scroll-trigger" href="{{ site.baseurl }}/#{{ link.section }}">{{ link.title }}</a>
		  {%- else -%}
		    <a class="nav-link js-scroll-trigger" href="#">{{ link.title }}</a>
		  {%- endif -%}
          </li>
		{% endfor %}
           <li class="nav-item">
                <a class="nav-link js-scroll-trigger" href="legal">{{ site.data.sitetext[site.locale].footer.elegant | default: "风采展示" }}</a>
           </li>
        </ul>
      </div>
    </div>
  </nav>
  <!-- End Navigation -->
  
<section class="bg-light page-section" id="{{ site.data.sitetext[site.locale].portfolio.section | default: " portfolio " }}">
    <div class="container">
        <div class="row">
            <div class="col-lg-12 text-center">
                <h2 class="section-heading text-uppercase">{{ site.data.sitetext[site.locale].footer.elegant | default: "风采展示" }}</h2>
                <h3 class="section-subheading text-muted">{{ site.data.sitetext[site.locale].portfolio.text | markdownify }}</h3>
            </div>
        </div>
        <div class="row">
            {% for project in site.platform %}
            <div class="col-md-4 col-sm-6 portfolio-item">
                <a class="portfolio-link" data-toggle="modal" href="#p{{ forloop.index }}">
                    <div class="portfolio-hover">
                        <div class="portfolio-hover-content">
                            <i class="{{ site.data.style.portfolio-icon | default: " fas fa-plus fa-3x " }}"></i>
                        </div>
                    </div>
                    <img class="img-fluid" src="{{ project.caption.thumbnail }}" alt="">
                </a>
                <div class="portfolio-caption">
                    <h4>{{ project.caption.title }}</h4>
                    <p class="text-muted">{{ project.caption.subtitle }}</p>
                </div>
            </div>
            {% endfor %}
        </div>
    </div>
</section>
{% exhibition.html %}

