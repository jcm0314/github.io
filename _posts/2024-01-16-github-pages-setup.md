---
layout: post
title: "GitHub Pages 블로그 설정 완벽 가이드"
date: 2024-01-16 14:30:00 +0900
categories: [tech, development]
tags: [github-pages, jekyll, blog]
---

GitHub Pages를 사용해서 개인 블로그를 만드는 방법을 단계별로 설명해드리겠습니다!

## GitHub Pages란?

GitHub Pages는 GitHub에서 제공하는 정적 사이트 호스팅 서비스입니다. 
Jekyll, Hugo, 또는 순수 HTML/CSS로 만든 웹사이트를 무료로 호스팅할 수 있습니다.

## 1. 저장소 생성

먼저 GitHub에서 새로운 저장소를 생성해야 합니다:

```bash
# 저장소 이름은 반드시 username.github.io 형식이어야 합니다
# 예: myusername.github.io
```

## 2. Jekyll 설치

로컬에서 Jekyll을 설치하고 개발 환경을 설정합니다:

```bash
# Ruby 설치 (Windows의 경우 RubyInstaller 사용)
# macOS의 경우 Homebrew 사용
brew install ruby

# Jekyll 설치
gem install jekyll bundler

# 새 Jekyll 사이트 생성
jekyll new my-blog
cd my-blog
```

## 3. 기본 설정

`_config.yml` 파일에서 블로그 설정을 변경합니다:

```yaml
title: My Blog
email: your-email@example.com
description: 블로그 설명
baseurl: ""
url: "https://username.github.io"
```

## 4. 테마 적용

Jekyll에는 여러 테마가 있습니다. minima 테마를 사용하는 경우:

```yaml
# _config.yml
theme: minima
```

## 5. 포스트 작성

`_posts` 폴더에 마크다운 파일로 포스트를 작성합니다:

```markdown
---
layout: post
title: "포스트 제목"
date: 2024-01-16 12:00:00 +0900
categories: [category]
tags: [tag1, tag2]
---

포스트 내용...
```

## 6. 로컬 테스트

```bash
bundle exec jekyll serve
```

브라우저에서 `http://localhost:4000`으로 접속하여 확인합니다.

## 7. GitHub에 배포

```bash
git add .
git commit -m "Initial blog setup"
git push origin main
```

## 8. GitHub Pages 활성화

1. GitHub 저장소 페이지로 이동
2. Settings → Pages
3. Source를 "Deploy from a branch"로 설정
4. Branch를 "main"으로 선택
5. Save 클릭

## 장점

- **무료 호스팅**: 완전 무료로 사용 가능
- **자동 배포**: Git push만 하면 자동으로 배포
- **커스터마이징**: 원하는 대로 디자인 변경 가능
- **SEO 친화적**: 검색 엔진 최적화에 유리

## 마무리

GitHub Pages는 개발자들이 블로그를 시작하기에 최고의 플랫폼입니다. 
이 가이드를 따라하시면 멋진 개인 블로그를 만들 수 있을 것입니다!

---

*다음 포스트에서는 Jekyll 테마 커스터마이징에 대해 다루겠습니다.* 