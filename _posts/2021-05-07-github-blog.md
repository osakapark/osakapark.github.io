---
layout: single
title:  "첫 포스팅"
categories: github
tag: blog
--- 


## STEP 1 페이지 생성

1. github.com 계정 생성
2. 테마선택 <br>
   https://github.com/topics/jekyll-theme <br>
   (이번 강좌는  minimal-mistakes)   
3. Fork <br>
   우측 상단 Fork 버튼
4. Repository name  변경<br>
  githubid.github.io (예 :  osakapark.github.io ) <br>
  repository/setting  에서도 변경 가능 
5. Create fork


## STEP 2 _config.yml  편집

/_data/authors.yml
```
osakapark_author:
  name        : "osakapark"
  bio         : "What's up?"
  #avatar      : "/assets/images/bio-photo-2.jpg"
  links:
    - label: "Email"
      icon: "fas fa-fw fa-envelope-square"
      url: "mailto:hansya@nate.com"
    - label: "Website"
      icon: "fas fa-fw fa-link"
      url: "https://osakapark.github.io"
    - label: "Github1"
      icon: "fab fa-fw fa-github"
      url: "https://github.com/osakapark"
```
/assets/images/
  - 그림 파일 추가

## STEP 3 Category
_config.yml  주석풀기
```
 jekyll-archives:
   enabled:
     - categories
     - tags
   layouts:
     category: archive-taxonomy
     tag: archive-taxonomy
   permalinks:
     category: /categories/:name/
     tag: /tags/:name/
```

