#mission -03

<h1> transition 과제 </h1>

<p>Q 고려 사항</p>

  트랜지션 사용으로 내부 컨텐츠 확장시 외부 컨테이너 박스 또한 사이즈 변경으로 인해 확장할 것 

  내부 컨텐츠 컨테이너 미확장시 외부로 나오는 컨텐츠 처리

<h2> constructure </h2>

div>h1>span+div>ul>li*5>a
        
- div - 겉면 박스 </br>
- h1 - 제목 span 태그로 사이트 부분 따로 래핑 </br>
- div -  내부 박스 </br>
- ul - 각 사이트 링크 네임 리스트 활용 </br>
- li - 링크 이동 가능하게 a 태그로 내부 래핑 각 사이트 네임  

<h2> CSS </h2>

- box-sizing: border-box; 각 컨테이너 박스 (div, h1, ul, li ) 패딩으로 인한 사이즈 변경을 막기 위해 
보더박스 처리
- h1 태그에 margin:0; 처리를 해 기본 에이전트 스타일 마진 제거
- 겉면 div 박스는 내부 div 박스의 높이 변경에 따라 변해야 하므로 width는 지정하고 height는 미지정해
  기본 auto값 그대로 적용
- 내부 div 박스 마우스 오버 이벤트 발생 전 height 값 지정, 오버플로우 히든으로 펼쳐졌을 때 나타나야하는 컨텐츠 숨기기
- 내부 div 박스에 트랜지션 property duration function delay 순서로 지정
- 겉면 div 박스에 hover 가상클래스 사용, 마우스 오버 이벤트 발생시 height 값 **기존 1.75rem -> 오버 후 10rem** 변경되도록 지정
- a 엥커 태그 인라인 요소 속성으로 인해 사이즈 값 적용 불가 _display:block_ 으로 블록 속성으로 변화 주고
엥커 태그 선택 영역 확장 
- 엥커 태그 특성(밑줄 글자색 변경) 제거

<h2>What I learn</h2>

1. 패딩으로 인한 사이즈 변경 제어 방법 **box-sizing: border-box;**

2. div 박스 height 값 미저정으로 내부 컨텐츠 사이즈 변화에 따라 크기 변화 가능

3. 가상클래스 사용으로 트랜지션 적용 확인

4. 엥커 태그 선택 가능 영역 확장 _display:block_
