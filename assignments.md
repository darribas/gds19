---
title: Assignments
category: assignment
layout: default
---

{% capture assessment %}{% include_relative content/website_data/assessment.md %}{% endcapture %}
{{ assessment | markdownify }}

{% capture criteria %}{% include_relative content/website_data/marking_criteria.md %}{% endcapture %}
{{ criteria | markdownify }}

{% capture task_forum %}{% include_relative content/website_data/task_forum.md %}{% endcapture %}
{{ task_forum | markdownify }}

{% capture task_01 %}{% include_relative content/website_data/task_01.md %}{% endcapture %}
{{ task_01 | markdownify }}

{% capture task_02 %}{% include_relative content/website_data/task_02.md %}{% endcapture %}
{{ task_02 | markdownify }}

{% capture task_03 %}{% include_relative content/website_data/task_03.md %}{% endcapture %}
{{ task_03 | markdownify }}


