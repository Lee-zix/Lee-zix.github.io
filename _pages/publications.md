---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---

{% if author.googlescholar %}
  You can also find my articles on <a href="{{author.googlescholar}}">Google Scholar</a>
{% endif %}

{% include base_path %}
{% capture written_year %}'None'{% endcapture %}
{% for post in site.publications %}
  {% capture year %}{{ post.date | date: '%Y' }}{% endcapture %}
  {% if year != written_year %}
    <h2 id="{{ year | slugify }}" class="archive__subtitle">{{ year }}</h2>
    {% capture written_year %}{{ year }}{% endcapture %}
  {% endif %}
  {% include archive-single-publications.html %}
{% endfor %}

<!-- # 2021

- **Long Bai**, Saiping Guan, Jiafeng Guo, Zixuan Li, Xiaolong Jin, Xueqi Cheng, *Integrating Deep Event-Level and Script-Level Information for Script Event Prediction*, EMNLP'2021. [[PDF](
https://aclanthology.org/2021.emnlp-main.777.pdf)][[Code](https://github.com/waltbai/MCPredictor)]

# 2020

- Yunqi Qiu, Kun Zhang, Yuanzhuo Wang, Xiaolong Jin, **Long Bai**, Saiping Guan, Xueqi Cheng, *Hierarchical Query Graph Generation for Complex Question Answering over Knowledge Graph*, CIKM'2020. [[PDF](https://dl.acm.org/doi/abs/10.1145/3340531.3411888)]
- Xingchen Deng, Lei Zhang, Yixing Fan, **Long Bai**, Jiafeng Guo, Pengfei Wang, *Bidirectional Dependency-Guided Attention for Relation Extraction*, ACML'2020. [[PDF](http://proceedings.mlr.press/v129/deng20a/deng20a.pdf)] -->
