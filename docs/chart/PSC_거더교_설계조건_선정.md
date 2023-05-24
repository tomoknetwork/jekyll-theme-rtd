---
layout: default
title: PSC 거더교 설계조건 선정
nav_order: 2
---

# PSC 거더교 설계조건 선정

```mermaid
%%{ init: { 'flowchart': { 'curve': 'linear' } } }%%
flowchart TD
    n1[설계조건]
    n2[[모듈G. 환경조건에 따른\n노출등급 결정]]
    n3[[모듈H. 설계등급에 따른\n사용한계값 결정]]

    n1-->n2-->n3

    click n2 href "//module/module_g.html"
```