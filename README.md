[JS 기본사용법]

폴더명 => 
D:\ResWeb\200528\silsp\part03_JS
     \JS01_Intro\JS02_Basic
html => silsp.html

1. JS코드 위치별 분류
  1) 인라인 자바스크립트
      => html파일에 작성
      => html요소에 JS용도의
           속성을 만든다.
           이 속성을 "이벤트 핸들러"
           (Event Handler)속성
           이라고 한다.
      이벤트(Event) : 브라우저에서
       발생되는 모든 동적인 결과
    => 클릭, 더블클릭, 키보드 누름,
       마우스 위치 이동, 브라우저 로딩,
       브라우저 새로고침 등등...

      !결론 : 인라인 자바스크립트는
           html요소(= 태그)의
           이벤트핸들러 속성에 작성하는
           JS코드를 의미한다.
      이벤트 핸들러 속성 종류
      1) onclick
      2) onmouseover
      3) onmouseout
      4) onkeyup
      5) onload
      6) onsubmit
        ... 

      JS 찍어보기 => 
         alert('출력할 내용');


  2) 내부 자바스크립트
            (=Inner JS, 이너 JS)
      => html파일에 작성
     (1) 위치
       가. <head>영역 내부 하단
           a. </style> 태그 다음
           b. </head> 태그 이전
       나. <body>영역 내부 하단
           => </body> 태그 이전
     (2) 형식
       => <script>
               JS내용
             </script>  
               


  3) 외부 자바스크립트  
      => html파일과는 무관한
            외부 JS파일을 생성함.

     가. html 파일
       <script src="Path"></script>
     나. JS 파일
        <script> 를 제외한
        실제 JS 코드만 기재함


-----------------------------------

[JS는 HTML 을 제어할 수 있습니다.]
=> 요소, 속성, 텍스트, 콘텐트에 대하여
     생성, 수정, 삭제 할 수 있습니다.

     <시작태그 속성="속성값">
      콘텐트 또는 텍스트
     </종료태그>
     여기에 적용되는  CSS도 JS로
     생성, 수정, 삭제 할 수 있습니다.

cf. JS 주석(=comment, 코멘트)
   1. 1줄 주석 => //
   2. 여러줄 주석 => CSS 와 동일함
                           /*     */

document => html 문서
JS는 명령어 1줄을 작성한 후
마지막에 반드시 세미콜론(;)을 기재한다.


-----------------------------------

[JS를 내부, 외부코드로 작성할 때 주의점]
(인라인JS는 모두 적용되지 않음)
1. 대소문자를 구분함
2. 중괄호 / 소괄호는 순서대로 작성하며
    괄호의 짝이 맞아야 함.
    보기.   
       괄호 열기                 괄호 닫기
       { 
            {  ( 
                 코드{ 
                    코드  }
                                )
                                    }   }
3. 명령어 1줄이 끝나면 반드시 
     세미콜론 기재함(;)
       ; => 세미콜론, 구분(인)자, 
                          delimiter, 딜리미터
4. html, css 코드가 일반적으로
    JS코드 사용전에 선행되어야 한다.
5. 단 1개의 오타, 세미콜론누락,
    대소문자 구분오류, 기호 오기 등등이
    있을 경우 모두 정상실행되지 않는다.
6. 쌍따옴표, 홑따옴표 표기법에 주의한다.
    => 단순히 1개만 표기할 경우
         쌍따옴표, 홑따옴표 중 어느것이라도
          사용가능함.
         보기 : alert("OK");   (O)
                 alert('OK');   (O)
    
    => 코드 외부에서 쌍따옴표를 이미
         사용했을 경우
         내부 코드에 사용할 쌍따옴표는
         반드시 홑따옴표를 사용해야 함.
         보기 : 
     <p onclick="alert("OK")">...</p>
         (X)
     <p onclick="alert('OK')">...</p>
         (O)

    참고. JS에서 오류가 발생했을 경우
          기능키 F12을 눌러서 개발자도구에서
          오류를 확인하고 수정한다.
          (또는 플러그 인을 사용하여
                 오류를 확인할 수 있다.)



-------------------------------------

[JS 학습 방법 1]
1. 코딩 순서
  1) 입력
  2) 계산(=처리)
  3) 출력

   참고. 필요한 것만 고려하여 코딩한다.

2. 각 코딩 순서에서 사용되는 JS항목들
  1) 변수  
      => 입력/출력

  2) 자료형
  3) 연산자
  4) 제어문
  5) 배열
  6) 함수
  7) 객체


[JS 학습 방법 2]
=> 경험치를 쌓는다.
     코드 내용, 결과 처리에 대한
     이해가 되지 않는 것이
     일반적인 현상


   

----------------------------

[변수를 사용한 입출력]

1. 변수 사용법

변수 => 값을 임시저장하는 것
   보기. var 변수명 = 값;
          또는
          var 변수명;
          변수명 = 값;

   참고. var 대신 let 가능함.



2. 값의 입력

값을 가져오는 방법
  1) 값을 직접 입력
     => 숫자나 문자를 직접 표기
  2) html 코드에서 value속성을 사용함
     => form요소의 
          input, option, textarea의
          value를 사용하여 값을 가져온다.
  3) html 코드에서 style속성을 사용함
     => CSS의 속성을 사용하여
           특정 값을 입력

3. 값의 출력
  1) 알림창을 사용한 출력 
      => alert(출력사항);   // 알림창 또는 경고창
      출력사항 표시방법
       (1) 변수, 숫자 => 그냥 표기
       (2) 문자 => 따옴표를 사용함
  2) html의 특정 요소의 텍스트로 출력
  3) css의 특정 스타일속성의 값을 설정


------------------------------------------

[JS의 값 입력]
1. 직접 입력
2. html요소의 값 입력
3. html과 css의 속성값 입력

[JS의 값 출력]
1. 알림창 출력(=경고창 출력)
2. html요소의 값으로 출력
3. html과 css의 속성값 출력


[JS 프로그램 작성 순서]
1. 입력
2. 처리
3. 출력


-----------------------------
[JS의 값 입력 소스]
1. 직접 입력 => 
  1) var a = 4;
  2) let number = 3.5;
  3) var txt;
      txt = "가나다";
  
2. html요소의 값 입력 =>
    html 요소들 중에서 
    value속성이 있는 것들
   1) <input value="...">
   2) select - <option value="...">
   3) <textarea>...</textarea>

   주의. <p>가나다</p>
          이 때 "가나다"는 value 속성이 아님.
          text에 해당
          => value와 text의 구분이 필요함

    html요소의 값을 입력하기 위해 필요한 추가 속성
    => id속성(단, id 속성만 값을 입력할 수 있는 것은 아님)

    보기. html =>
            <input id="txt" value="가나다123">
          JS에서 html의 value 값 가져오기 =>
            document.getElementById("txt").value
    사용예.
           <body>
             <input id="txt" value="가나다123">

             <script>
               var txt01 = document
                                 .getElementById("txt")
                                 .value;
               // 변수 txt01에는 "가나다123"이 저장되어 있음
               // 즉, 아래의 코드와 동일한 결과
               //  var txt01 = "가나다123";

             </script>
           </body>

     추가내용 : 요소의 text 내용 입력받기
       보기. <p id="txt02">오늘 금요일!!!</p>
              <script>
               var sample = document.
                                   getElementById("txt02").
                                   innerText;
              // var sample = "오늘 금요일!!!"; 동일한 결과
              

         요소(=Element, 엘리먼트)
         = <시작태그 속성="속성값"> + 텍스트 + </종료태그>
             

3. html과 css의 속성값 입력 =>
    html 요소들 중에서 
    css의 속성을 JS의 속성으로 사용되는 이름(=JS의CSS속성)
   참고. JS의CSS속성 =>
          document
          .getElementById("id속성값")
          .style.JS의CSS속성;

      보기. CSS코드에서 글자색 속성
             선택자  {  color: #f00; }
             => "JS의CSS속성"  보기                      

          document
          .getElementById("id속성값")
          .style.color = "#f00";

      참고. css 속성값        JS 속성값
       1. 1단어 속성
               color          style.color
              display        style.display
       2. 2단어 속성
            font-size             style.fontSize
            text-decoration    style.textDecoration
            => 대쉬(dash)기호 제거하고 
                  2번째 단어부터 첫글자 대문자
       3. 전혀 다른 것
            float                   cssFloat
            거의 대부분 동일하지만
             극히 일부분만 JS에서 이미 명령어로 사용하고 있으므로
             전혀 다른 이름을 사용함.



          

-----------------------------------------------


 
[JS의 값 입력]
1. 직접 입력    
    var 변수 = 값;
2. html요소의 값 입력
3. html과 css의 속성값 입력

[JS의 값 출력]
1. 알림창 출력(=경고창 출력)

    alert(출력내용);
    1) 변수와 숫자는 값을 그대로 사용함
         보기1. 변수
           var a = "abc";
            alert(a);
         보기2. 숫자
           alert(-5);  
           alert(20.3);                 

    2) 문자(열)은 따옴표를 사용함
         보기.   alert("테스트");
                  alert("2+3");
         주의.   var a = "가나다";
                  alert(a);   => 가나다 출력됨
                  alert("a");  => a   출력됨
  

2. html요소의 값으로 출력

    document
    .getElementById("id속성값")
    .value = 출력할 내용;
         => input, option, textarea처럼
               value 속성이 있는 요소에 사용함.

    주의사항1. 요소의 텍스트로 출력
    document
    .getElementById("id속성값")
    .innerText = 출력할 내용;
         => <시작태그>내용</종료태그> 에서
               내용에 해당하는 위치에 출력됨
      보기. 
             <p id="test">ABC</p>
             이 요소에
    document
    .getElementById("test")
    .innerText = "가나다";

     <p id="test">ABC</p> 에서
     <p id="test">가나다</p> 로 변경된다.




   주의사항2. 요소의 텍스트에 하위요소를 적용하여 출력
    document
    .getElementById("id속성값")
    .innerHTML = <하위태그>출력할 내용</하위태그>;

      보기. 
             <p id="test">ABC</p>
             이 요소에
    document
    .getElementById("test")
    .innerHTML = "<b>가나다</b>";

     <p id="test">ABC</p> 에서
     <p id="test"><b>가나다</b></p> 로 변경된다.
       
               


3. html과 css의 속성값 출력

    document
    .getElementById("id속성값")
    .style.적용할CSS속성 = "해당CSS속성값";

    <p id="pTag">가나다</p>

    document
    .getElementById("pTag")
    .style.color = "#f00";

     "가나다" 글자색이 빨강색이 적용됨