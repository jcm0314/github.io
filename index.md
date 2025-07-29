---
layout: home
title: 홈
---

# 안녕하세요! 👋

GitHub Pages 블로그에 오신 것을 환영합니다!

## 최근 게시물

{% raw %}{% for post in site.posts limit:5 %}
### [{{ post.title }}]({{ post.url }})
{{ post.excerpt }}
**{{ post.date | date: "%Y년 %m월 %d일" }}**
{% endfor %}{% endraw %}

## 카테고리

- [기술]({{ site.baseurl }}/categories/tech)
- [개발]({{ site.baseurl }}/categories/development)
- [일상]({{ site.baseurl }}/categories/daily)

## 소셜 미디어

- [GitHub](https://github.com/your-github-username)
- [Twitter](https://twitter.com/your-twitter-username) 