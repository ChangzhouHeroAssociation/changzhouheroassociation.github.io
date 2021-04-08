 {% for project in site.platform %}
<div tabindex="-1" role="dialog" aria-hidden="true" id="p{{ loop.index }}">
    <div>
        <div class="modal-content"
            <div data-dismiss="modal">
                <div class="lr">
                    <div class="rl">111</div>
                </div>
            </div>
            <div>
                <div>
                    <!-- Project Details Go Here -->
                    <h2>{{ project.title }}</h2>
                    <p>{{ project.subtitle }}</p>
                    <img src="{{ project.image }}" alt="{{ project.alt }}">
                    <p>{{ project.content }}</p>
                    <button class="btn btn-primary" data-dismiss="modal" type="button">1111</button>
                </div>
            </div>
        </div>
    </div>
</div>
{% endfor %}