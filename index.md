---
title: Microsoft Learn. Общие сведения об ИИ в упражнениях Azure
permalink: index.html
layout: home
---

# AI-900: введение в ИИ в упражнениях Azure

Эти практические упражнения предназначены для поддержки обучающих материалов в [Microsoft Learn](https://docs.microsoft.com/training/).

Для выполнения этих упражнений вам понадобится подписка Microsoft Azure. Зарегистрироваться для получения бесплатной пробной версии можно по адресу [https://azure.microsoft.com](https://azure.microsoft.com).

{% назначение лабораторий = site.pages | where_exp:"page", "page.url содержит "/Инструкции/упражнения" %}
| Упражнения |
| ------- | 
{% for activity in labs  %}| [{{ activity.lab.title }}]({{ site.github.url }}{{ activity.url }}) |
{% endfor %}
