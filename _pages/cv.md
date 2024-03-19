---
layout: default
permalink: /cv/
title: cv
nav: true
nav_order: 3
cv_pdf: Sanket_Goutam_CV.pdf
---

<div class="post">
  <article>
    <embed src="{{ page.cv_pdf | prepend: 'assets/pdf/' | relative_url}}" width="{{ site.max_width }}" height="1200px" />
  </article>
</div>