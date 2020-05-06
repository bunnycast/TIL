200506 - frontend

## 1. html / css 구조적 특성
- html : 컨텐츠의 구조, 유지 보수 등을 고려하여 기획해야 함
- css 
  - layout : 어떻게 배치할 것인가? (<span style="color:red> 반응형 웹</span>)
  - deco

## 2. html 구조 분석 
- 논리적인 순서
- Symantic(의미에 맞는) 마크업
- Naming

## 3. Section vs Article
- 사용 방법은 비슷, 다만 완결된 정보일 경우(RSS) article 활용
- heading 정보를 포함함이 일반적 -> 상위 섹션의 헤딩 정보를 따름 

## 4. img 컨텐츠를 작성하는 방법
- css bg : 장식일 경우 (img alt='' 태그와 유사함)
- img 태그 : 반응형 구현에 적합

## 5. Section.book 클래스 구조
section.book
  h2 : 배경, 추천서적
    span : RB
  figure : 캡션있는 컨텐츠
    img
    figcaption
  dl : def. list, dt와 dd 포함 (cf. ul/ol은 li만을 가짐)
