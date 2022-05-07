---
layout: single
title:  "Github Blog 작성"
categories: github
tag: [blog, github]
toc: true
author_profile: false
sidebar:
  nav: "docs"
search: true  
--- 

## STEP 1 페이지 생성

1. github.com 계정 생성
2. 테마선택 <br>
   https://github.com/topics/jekyll-theme <br>
   (이번 강좌는  minimal-mistakes)   
3. Fork <br>
   우측 상단 Fork 버튼
4. Repository name  변경<br>
  [githubid].github.io (예 :  osakapark.github.io ) <br>
  repository/setting  에서도 변경 가능 
5. Create fork


## STEP 2 _config.yml  편집
/_data/authors.yml
```yml
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
    - label: "Github"
      icon: "fab fa-fw fa-github"
      url: "https://github.com/osakapark"
```
/assets/images/
```
  - 그림 파일 추가
```  

## STEP 3 Category
_config.yml  주석풀기 
``` yml
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

#  수정 : 주석 풀면 안됨 그대로!!! (2022.05.07)     
```

 _pages/category-archive.md
``` yml
--- 
title: "Category"
layout: categories
permalink: /categories/
author_profile: true
sidebar_main: true
---
```

/_data/navigation.yml
``` yml
# main links
main:
  - title: "Category"
    url: /categories/
```


## STEP 4 Tag
/_pages/tag-archive.md
```yml
---
title: "Tag"
layout: tags
permalink: /tags/
author_profile: true
sidebar_main: true
---
```

/_data/navigation.yml
``` yml
main:
  - title: "Category"
    url: /categories/
  - title: "Tag"
    url: /tags/  
```

/_posts/2021-05-07-xxx.md
```
--- yml
layout: single
title:  "첫 포스팅"
categories: github
tag: [blog, github]
--- 
```

## STEP 5 404 Error 
/~pages/404.md

```md
---
title: "Page Not Found"
excerpt: "Page not found. Your pixels are in another canvas."
sitemap: false
permalink: /404.html
---

![](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSINa_zSqQSG_KsOcaRWc8hgoncoihL6eiTVtMKUHY8e7gub_cVFR96y_LEPD9Gk2knQ2o&usqp=CAU)
```

## STEP 6 Sidebar Navigation & Search
/_data/navigation.yml
```yml
main:
  - title: "Category"
    url: /categories/
  - title: "Tag"
    url: /tags/    
  - title: "Search"
    url: /search/

docs:
  - title: "main item"
    children:
      - title: "Category"
        url: /categories/
      - title: "Tag"
        url: /tags/
```

/_pages/search.md
```yml
---
title: Search
layout: search
permalink: /search/
---
```

/_post/(file)
```yml
---
layout: single
title:  "Github Blog 작성"
categories: github
tag: [blog, github]
toc: true
author_profile: false
sidebar:
  nav: "docs"
search: true  
--- 
```




## 참고 자료
 https://jekyllrb.com/docs/posts/
 
 https://mmistakes.github.io/minimal-mistakes/docs/quick-start-guide/
 
 마크다운 문법 강좌 : 편안한 Jekyll 사용법을 위한 마크다운 문법 
 
 
image  처리
```md
![record apeach]({{site.baseurl}}/images/2021-05-07-github-blog/apeach01.png)
```
 
 _config.yml
 ```yml
markdown : kramdown   #기본값
highlighter: rouge    #기본값
pagenate  # 페이지 숫자
timezone : Asia/Seoul  #현재 문제 있음
 ```

![record apeach]({{site.baseurl}}/images/2021-05-07-github-blog/apeach01.png)
![샘플 이미지](../images/2021-05-07-github-blog/apeach01.png)
