---
title: "Second_post"
subtitle: "Second_post's subtitle"
date: 2022-07-18T15:47:00+09:00
lastmod: 2022-07-18T15:47:00+09:00
draft: false
author: "Haksoo Ji"
authorLink: "https://github.com/MintZzz1009"
description: "This is testing <description>."
license: ""
images: [/images/sky_logo.png]

tags: ["Markdown", "Java", "Git", "submodule", "theme", "LoveIt"]
categories: ["dev"]

featuredImage: "Mint fabric"
featuredImagePreview: "/images/divazus-fabric-store-2VG1ggL5IuQ-unsplash.jpg"

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

<!--more-->

# This is testing.

## categories 와 tags 를 처음으로 생성

- 현재 ./public/categories/ 에는 ./essays 와 ./memoirs ./reviews ./index.html 만 있는 상태.
- 이 파일을 생성할 때 front matter 에 다음을 추가해봤다.
```markdown
tags: ["Markdown", "Java", "Git", "submodule", "theme", "LoveIt"]
categories: ["dev"]
```


## 여러가지 방법으로 이미지 파일 추가해보기.

- 1. 
```markdown
![Mint_block](/images/tools-for-motivation-m1DZR0Q9c6w-unsplash.jpg)
```

출력 :
![Mint_block](/images/tools-for-motivation-m1DZR0Q9c6w-unsplash.jpg)

- 2.
```markdown
![Mint_block](/images/tools-for-motivation-m1DZR0Q9c6w-unsplash.jpg "민트색 벽돌")
```

출력 :
![Mint_block](/images/tools-for-motivation-m1DZR0Q9c6w-unsplash.jpg "민트색 벽돌")

- 3.
```markdown
<!-- [id] 태그 사용 --> 
![Mint_block][Mint_block]

<!-- refernce -->
[Mint_block]: /images/tools-for-motivation-m1DZR0Q9c6w-unsplash.jpg "민트색 벽돌"
```
출력 :
![Mint_block][Mint_block]
[Mint_block]: /images/tools-for-motivation-m1DZR0Q9c6w-unsplash.jpg "민트색 벽돌"

>순서를 바꾼다면?
```markdown
<!-- refernce -->
[Light_mint_fabric]: /images/tools-for-motivation-m1DZR0Q9c6w-unsplash.jpg "민트 나선형 천"

![Mint_fabric][Light_mint_fabric]
```
출력 :
[Light_mint_fabric]: /images/tools-for-motivation-m1DZR0Q9c6w-unsplash.jpg "민트색 나선형 천"
![Mint_fabric][Light_mint_fabric]

- 4. short codes 사용
```markdown
<!-- 출력1 -->
{{< figure src="/images/sky_logo.png" title="sky_logo" height="50" width="50" >}}

<!-- 출력2 -->
{{< image src="/images/sky_logo" caption="Sky Logo from someone's instagram." src_s="/images/Sky-small.jpg" src_l="/images/Sky-large.jpg" >}}
```
출력1 :
{{< figure src="/images/sky_logo.png" title="sky_logo" height="50" width="50" >}}

출력 2 :
{{< image src="/images/sky_logo" caption="Sky Logo from someone's instagram." src_s="/images/Sky-small.jpg" src_l="/images/Sky-large.jpg" >}}

## short code 를 markdown 문서에서 보이도록 설정

```markdown
{{</* Shortcode */>}}
```
출력 :
{{</* Shortcode */>}}