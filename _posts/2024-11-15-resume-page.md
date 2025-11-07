---
title: <title></title>
---
<img src="/images/Jasmine_Shields.png"alt="resume">
    {% if site.theme_config.show_footer == true %}
<footer>
    <div class="dashed"></div>
    {% include horizontal_list.html collection=site.data.home.footer_entries %}
</footer>
    {% endif %}