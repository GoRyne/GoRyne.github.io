---
layout: post
title: "Google Analytics"
date: 2021-12-16 11:32:47 +0900
categories: jekyll update
background: "/img/posts/01.jpg"
comments: true
---

# Google Analytics 적용하기  

## 1. Analytics 가입
- 구글 계정으로 Google Analytics에 접속을 한다.
- Google Analytics 시작하기를 눌러 가입을 한다.
- 가입 절차를 진행하면서 세부적인 권한이나 정보를 입력한다.
- 통계 플랫폼을 웹으로 설정해주고 웹사이트 이름을 내가 식별하기 편한 이름으로 설정해준다.
- 구글 애널리틱스 설정이 끝났다.  
  
## 2. Analytics 적용하기
- 본인의 include 디렉토리에 `google-analytics.html` 파일이 있는지 확인해준다.
- 만약 없다면 아래의 코드를 include 디렉토리에 `google-analytics.html` 라는 이름으로 저장후 붙여넣어 준다.

```  
<script async src="https://www.googletagmanager.com/gtag/js?id={{ site.google_analytics }}"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());

  gtag('config', '{{ site.google_analytics }}');
</script>
```
- 이후 `config.yml` 파일에 아래의 코드를 붙여준다



  google_analytics: '추적ID'

- 여기 까지 정상적으로 끝마쳤다면 아래의 사진과 같이 애널리틱스가 정상적으로 작동하게 된다.
  
<img src="/img/alaytics.png" height="350" width="730">
  

