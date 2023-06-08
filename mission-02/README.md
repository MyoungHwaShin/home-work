<header>mission - 02</header>

<h1>로그인 폼 만들기</h1>

float과 display를 활용해 만들어보는 로그인폼

<h1>Mark up<h1>

<h2>구조</h2>

 >div - 겉 주황색 상자 
  > h1 - 로그인 헤더
  > form - 로그인 폼 
    >fieldset -  폼 그룹핑
      > legend - 필드셋 제목
      >ul - 아이디 / 비밀번호 / 로그인 버튼
        >li - 아이디 그룹
          >label - 값의 이름
          >p - '아이디' 네임 태그
          >input - 아이디 값 입력창
        >li - 비밀번호
         >label - 값의 이름
         >p - '비밀번호' 네임 태그
         >input - 비밀번호 값 입력창
        >li - 인풋 버튼
          >input type="버튼" - 버튼
    >div - 하단 가로 구분 선   
    >ul - 회원가입 & 아이디/비밀번호 찾기
     >li - 회원가입
      >span - 꺽쇠 상자
     >li - 아이디/비밀번호 찾기   
      >span - 꺽쇠 상자
           
- ul/li

  가로 두줄로 구성된 로그인 정보 입력창 구성에 용이한 ul/li 사용

  list-style:none;을 이용해 리스트 스타일 제거 
  
  position 사용시 위치를 용이하게 하기 위한 컨테이너 구성

- 하단 가로 구분선 기준으로 하단 또한 ul/li를 활용

<h1>CSS<h1>


- Wai-ARIA .a11yHidden 활용해 legend 숨김
- reset.css 이용해 기본 에이전트 스타일 제거
- 로그인 박스 fieldset 자체에 display: relative; 주어 내부 자식 요소들 absolute로 배치
- 자식요소 중 하나인 ul.login__Info에 display: relative; 주어 button과 li 요소들 구성
- 회원가입 & 아이디/비밀번호 찾기의 부모요소 ul 태그 .join 클래스 주고 display: absolute; 주어
  하단에 구성
- nth-child 선택자 활용해보기 위해 클래스 사용하지 않고 적용
- ul.join li:first-child에 float:left; 사용해 컨테이너상 왼쪽으로 배치
- ul.join li:nth-child(2) 블록요소로 인해 자동 줄바꿈 가로 동일선상 나열위해
  display:inline 적용

<h1> What I learn </h1>

block 과 inline이 float에 미치는 변화 확인 - display로 해결가능
clear:both 사용시 상속받은 float이 해제되면 밑으로 배치됨

부모 display:relative;, 자식 display:absolute로 
문서 내 자식 요소 배치에 유용.











