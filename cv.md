---
layout: resume
title: Curriculum Vitae 
---

<i class="fa fa-fw fa-github"></i> [View Academic CV on Github](https://github.com/Akshayanti/myCV/blob/CVs/Resume_academic.pdf) <i class="fa fa-fw fa-github"></i> [View Professional CV on Github](https://github.com/Akshayanti/myCV/blob/CVs/Resume_professional.pdf)

## Current Occupation

{{site.data.cv.position}} at {{site.data.cv.affiliation}}, {{ site.data.cv.address }}

**Quick Navigation Links**:<b />
[[Education](#education)] [[Publications](#publications)] [[Theses](#theses)] [[Professional Experience](#professional-experience)] [[Other Details](#other-details)] [[References](#references)]

----

## Education

{% for pub in site.data.cv.education %}
`{{pub.date}}`
**{{pub.title}}**, **{{pub.affiliation}}, {{pub.location}}**<br />
{% if pub.note %} *({{pub.note}})*<br />{% endif %}
{% if pub.thesis %} Thesis Title: {{pub.thesis}}<br /> {% endif %}
{% if pub.thesis %} Supervisor(s): {{pub.supervisor}} {% if pub.supervisor2 %} and {{pub.supervisor2}}{% endif %}{% endif %}

{% endfor %}

## Publications

{% for pub in site.data.cv.publications %}
`{{pub.year}}`
{{pub.author}}<br />
**{{pub.title}}**<br />
*{{pub.journal}}*
{% if pub.note %} *({{pub.note}})* {% endif %}<br />
[[web]({% if pub.internal %}{{pub.url | prepend: site.url}}{% else %}{{pub.url}}{% endif %})]
{% if pub.doi %}[[doi]({{pub.doi}})]{% endif %}

{% endfor %}

## Theses

{% for pub in site.data.cv.theses %}
`{{pub.year}}`
**{{pub.title}}**<br />
{{% if pub.type %}} {{pub.type}}. Supervised by [{{pub.supervisor}}]({{pub.supervisor_link}})
{% if pub.supervisor2 %} and [{{pub.supervisor2}}]({{pub.supervisor2_link}}){% endif %}.{{% endif %}}<br />
*{{pub.school}}*<br />
In *{{pub.address}}* <br />
{% if pub.url %}[[View Thesis]({{pub.url}})]{% endif %}

{% endfor %}

## Professional Experience

{% for pub in site.data.cv.positions %}
`{{pub.date}}`
**{{pub.title}}**, {{pub.company}}, {{pub.location}}<br />
{{% if pub.task %}} {{pub.task}} {{% endif %}}

{% endfor %}

## Other Details

### Spoken Languages

{% for pub in site.data.cv.language %}
`{{pub.level}}`
{{pub.name}}

{% endfor %}

### Awards and Extra-Curricular

{% for pub in site.data.cv.awards %}
`{{pub.year}}`
{{pub.detail}}

{% endfor %}

## References

{% for pub in site.data.cv.references %}
**{{pub.name}}**<br />
{{pub.affiliation}}<br />
<i class="fa fa-fw fa-envelope-square"></i> [{{pub.mail}}](mailto:{{pub.mail}})

{% endfor %}



<!-- ### Footer

Last updated: Oct 25, 2020 -->


