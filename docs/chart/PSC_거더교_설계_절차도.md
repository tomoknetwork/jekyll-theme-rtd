---
layout: default
title: PSC 거더교 설계 절차도
nav_order: 1
---

# PSC 거더교 설계 절차도


```mermaid
flowchart TD
    %% 그래프 노드
    subgraph s1[" "]
        n1[교량 설계 시작]
        subgraph n2[교량 형식 결정]
            n2_1[PSC 거더교]
            n2_2[강거더교]
            n2_3[ED교]
        end
        n3[상부구조 단면설정]
        n4[설계조건 선정]
        n5[모델링 및 구조해석]
        subgraph n6[부재 설계]
            n6_1[바닥판]
            n6_2[거더]
            n6_3[가로보]
            n6_4[다이아프램]
            n6_5[연속부 슬래브]
        end
    end
    n7{단면검토}
    subgraph s2[" "]
        n8[상부구조 부재설계 완료]
        n9[하부구조 단면가정]
        n10[설계조건 선정]
        n11[모델링 및 구조해석]
        n12[내진해석]
        n13[받침이동량 검토]
        n14[신축이음 설계]
        n15[부재 설계]

        subgraph n16[교대 설계]
            n16_1[기초판]
            n16_2[벽체]
            n16_3[날개벽]
            n16_4[접속슬래브]
            n16_5[말뚝]
        end

        subgraph n17[교각 설계]
            n17_1[기초판]
            n17_2[기둥]
            n17_3[두부보]
            n17_4[받침부]
            n17_5[말뚝]
        end
    end
    n18{단면검토}
    n19[하부구조 부재설계 완료]
    n20[교량 설계 완료]
    
    %% 그래프 엣지
    n1 --> n2 --> n3 --> n4 --> n5 --> n6 --> n7 

    n7 --No--> n3
    n7 --Yes --> n8

    n8 --> n9 --> n10 --> n11 --> n12 --> n13 --> n14 --> n15
    n15 --> n16 --> n18
    n15 --> n17 --> n18

    n18 --No--> n8
    n18 --Yes-->n19

    n19-->n20

    %% 링크
    click n4 href "/chart/PSC_거더교_설계조건_선정.html"

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
    class s1,s2 transparent
    class n2 green
    class n6,n16,n17 gray
    
    class n3,n4,n5,n6_1,n6_2,n6_3,n6_4,n6_5,n8 yellow
    class n9,n10,n11,n12,n13,n14,n15,n16_1,n16_2,n16_3,n16_4,n16_5 blue
    class n17_1,n17_2,n17_3,n17_4,n17_5,n19 blue
    
    class n1,n2_1,n2_2,n2_3,n7,n18 white
    class n20 orange

```