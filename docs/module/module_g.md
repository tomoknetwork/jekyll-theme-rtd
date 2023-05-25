---
layout: default
title: 모듈G. 환경조건에 따른 노출등급 결정
nav_order: 1
---

# 모듈G. 환경조건에 따른 노출등급 결정

```mermaid
%%{ init: { 'flowchart': { 'curve': 'linear' } } }%%
flowchart TD
    %% 그래프 노드
    n1[[모듈G. 환경조건에 따른\n노출등급 결정테스트]]
    subgraph s1[" "]
        n2[환경조건에 따른 노출등급 결정]
        l2[KDS 24 14 21_4.4.2_표4.4.2]
    end
    subgraph s2[" "]
        n3[콘크리트 최소피복두께 검토]
        l3[KDS 24 14 21_4.4.4.2_표4.4-3]
    end
    subgraph s3[" "]
        n4[노출등급에 따른 최소 콘크리트 강도 결정]
        l4[KDS 24 14 21_4.4.1_표4.4-1]
    end

    %% 그래프 엣지
    n1-->n2-->n3-->n4

    %% 링크
    click l2 href "https://www.kcsc.re.kr/StandardCode/Viewer/40145#title-1953" _blank
    click l3 href "https://www.kcsc.re.kr/StandardCode/Viewer/40145#title-2069" _blank
    click l4 href "https://www.kcsc.re.kr/StandardCode/Viewer/40145#title-1892" _blank

    
    %% 스타일 정의
    classDef transparent fill:none,stroke-width:0px
    classDef label fill:none,stroke-width:0px
    classDef white fill:#fff,stroke:#000
    classDef yellow fill:#f2eabd,stroke:#000
    classDef blue fill:#d7e8f5,stroke:#000
    classDef green fill:#d8f5d7,stroke:#000
    classDef gray fill:#ededed,stroke:#000
    classDef orange fill:#edc8ab,stroke:#000

    %% 스타일 적용
    class s1,s2,s3 transparent
    class l2,l3,l4 label
```
