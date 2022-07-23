---
title: "Second_post"
subtitle: "Second_post's subtitle"
date: 2022-07-18T15:47:00+09:00 
lastmod:                          #lastmod?
draft: false
author: "Haksoo Ji"
authorLink: "https://github.com/MintZzz1009"
description: "This is summary description in front-matter."
license: ""
images: [/images/sky_logo.png]

tags: ["Markdown", "Java", "Git", "submodule", "theme", "LoveIt"]
categories: ["dev"]

featuredImage: "featured-image.png"
featuredImagePreview: "https://hugoloveit.com/basic-markdown-syntax/featured-image.png"

hiddenFromHomePage: false
hiddenFromSearch: false
twemoji: false
lightgallery: true
ruby: true
fraction: true
fontawesome: true
linkToMarkdown: true
rssFullText: false

toc:
  enable: true
  auto: true
code:
  copy: true
  maxShownLines: 50
math:
  enable: false
  # ...
mapbox:
  # ...
share:
  enable: true
  # ...
comment:
  enable: true
  # ...
library:
  css:
    # someCSS = "some.css"
    # located in "assets/"
    # Or
    # someCSS = "https://cdn.example.com/some.css"
  js:
    # someJS = "some.js"
    # located in "assets/"
    # Or
    # someJS = "https://cdn.example.com/some.js"
seo:
  images: []
  # ...
---

This is summary of the second post.

<!--more-->

# This is testing.

## categories 와 tags 를 처음으로 생성

- 현재 ./public/categories/ 에는 ./essays 와 ./memoirs ./reviews ./index.html 만 있는 상태.
- 이 파일을 생성할 때 front matter 에 다음을 추가해봤다.
```markdown
tags: ["Markdown", "Java", "Git", "submodule", "theme", "LoveIt"]
categories: ["dev"]
```

___

## 여러가지 방법으로 이미지 파일 추가해보기.

### 1. 일반적인 방법 - markdown 형식 
#### ./static 디렉터리 내부의 이미지 파일 불러오기.
```markdown
<!-- 파일 경로 = "/blog/static/images/file.img" -->
![Mint_block](/images/tools-for-motivation-m1DZR0Q9c6w-unsplash.jpg)
```

*출력 :*
![Mint_block](/images/tools-for-motivation-m1DZR0Q9c6w-unsplash.jpg)

#### /content/posts/this_post 디렉터리 내부의 이미지 파일 불러오기.
```markdown
<!-- 파일 경로 = "/blog/content/posts/second_post/file.img" -->
![Mint_block](tools-for-motivation-m1DZR0Q9c6w-unsplash.jpg "민트색 벽돌")
```

*출력 :*
![Mint_block](tools-for-motivation-m1DZR0Q9c6w-unsplash.jpg "민트색 벽돌")

#### 표(table) 안에 이미지와 캡션 넣기.
```markdown
| ![Mint_block](tools-for-motivation-m1DZR0Q9c6w-unsplash.jpg |
| ***민트색 벽돌*** |
```


### 2. [id] tag 사용
```markdown
<!-- [id] 태그 사용 --> 
![Mint_block][Mint_block]

<!-- refernce -->
[Mint_block]: tools-for-motivation-m1DZR0Q9c6w-unsplash.jpg "The Mint Block"
```
  
*출력 :*
![Mint_block][Mint_block]
[Mint_block]: tools-for-motivation-m1DZR0Q9c6w-unsplash.jpg "The Mint Block"
    
순서를 바꾼다면?
```markdown
<!-- refernce -->
[Light_mint_fabric]: divazus-fabric-store-2VG1ggL5IuQ-unsplash.jpg "The fabric of mint color"

![Mint_fabric][Light_mint_fabric]
```
  
*출력 :*
[Light_mint_fabric]: divazus-fabric-store-2VG1ggL5IuQ-unsplash.jpg "The fabric of mint color"
![Mint_fabric][ Light_mint_fabric]


### 3. short codes 사용
#### figure
```markdown
<!-- 출력1 -->
{{< figure src="/images/sky_logo.png" title="sky_logo" height="50" width="50" >}}
```
  
*출력1 :*
{{< figure src="/images/sky_logo.png" title="sky_logo" height="50" width="50" >}}

#### image
{{< admonition info "This is info" false >}}
image 태그는 figure 태그를 대신할 수 있으면서 여러가지 옵션을 사용할 수 있다.  
>참조링크:
><https://hugoloveit.com/theme-documentation-extended-shortcodes/#image>
{{< /admonition >}}
```
<!-- 출력2 -->
{{< image src="/images/sky_logo.png" title="TITLE: SKY" caption="Sky Logo from someone's instagram." height="20" width="20" src_s="/images/sky_logo.png" src_l="/images/sky_logo.png" >}}
```    
*출력2 :*
{{< image src="/images/sky_logo.png" title="TITLE: SKY" caption="Sky Logo from someone's instagram." height="20" width="20" src_s="/images/sky_logo.png" src_l="/images/sky_logo.png" >}}
  

***

## short code 를 markdown 문서에서 보이도록 설정

태그 안의 내용을 `/*`,`*/`를 사용해서 주석처리한다.

```markdown
{{</* Shortcode */>}}
```
*출력 :*  
{{</* Shortcode */>}}
  
  

---

## 개행(줄바꿈)
### `<br/>`
`<br/>` 태그 입력 횟수 만큼 개행된다.
```markdown
A<br/>B
C<br/><br/>D
E
<br/>
F
```
A<br/>B
C<br/><br/>D
E
<br/>
F


### 공백문자 2칸 
`space bar` 즉, 공백문자 2칸 입력 후 엔터를 입력한다.
- A 입력 후, `space bar`+`space bar`+`enter`+`B`
```markdown
A  
B
```
A  
B

* A 입력 후, `enter`+`space bar`+`space bar`+`enter`+`B`
```markdown
A
  
  B
```
A
  
  B


### 엔터 2번 입력
글을 입력 후, `enter` 즉, 엔터를 두 번 입력하면 공백 라인이 추가된다.
- A 입력 후, `enter`+`enter`
```markdown
A

B
```
A

B
***


<!-- This is a comment -->
