---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---

<style>
    ul.publications {
        list-style-type: none ;
        font-size: 16px ;
        margin: 5px 0px 5px 5px ;
        padding: 0px 0px 0px 0px ;
    }

    ul.publications li {
        /* Decrement the counter by 1. */
        counter-increment: pubs -1 ;
        /* -- */
        align-items: flex-start ;
        display: flex ;
        margin: 20px 0px 20px 15px ;
        padding: 0px 0px 0px 0px ;
    }

    ul.publications li::before {
        content: "P"counter( pubs )"" ;
        /* -- */
        background-color: #eaeaea ;
        border-radius: 5px 5px 5px 5px ;
        box-sizing: border-box ;
        margin-right: 10px ;
        min-width: 40px ;
        padding: 0px 5px 0px 5px ;
        text-align: center ;
    }
</style>

{% include base_path %}
<ul class="publications" style="counter-reset: pubs {{ site.publications.size | plus:1 }};">
  {% for post in site.publications reversed %}
    <li>
      {% include archive-single-publication.html %}
    </li>
  {% endfor %}
</ul>
