# 웹 기초 이론 (2023.03.14)

<br/>
<br/>

## 웹 (World Wide Web)

- 인터넷을 통해 접근 가능한 공용 웹 페이지의 상호 연결
- 인터넷을 기반으로 한 수 많은 응용 프로그램 중 하나

#### 웹의 구성 요소

- HTTP 프로토콜
  - 서버와 클라이언트 간의 데이터 전송을 관리하는 프로토콜
- URL(Uniform Resource Locator)
  - 인터넷에서 웹 페이지, 이미지, 비디오 등 리소스 위치를 가리키는 문자열
- HTML - 웹 페이지의 구조를 지정하는 기술적인 언어

  <br/>
  <br/>

## 클라이언트와 서버

- 서버 : 인터넷에 연결된 컴퓨터
- 클라이언트 : 사용자가 웹사이트에 접근하려고 하는 기기들
- 서버는 정보를 제공, 클라이언트는 정보를 요청한다. <br/>

  1. 사용자(클라이언트)주소창에 웹 주소 입력
  2. 웹 사이트는 서버에서 정보를 가져와 웹 브라우저에 출력
  3. 서버에 웹 사이트에 접속하면 보이는 웹 요소와 사용자 정보와 같은 여러 정보들이 저장된다.

  <br/>
  <br/>

## HTTP (HyperText Transfer Protocol)

- 인터넷에서 사용자(클라이언트)와 서버가 정보를 주고 받기 위한 일종의 규칙
- 사용자와 서버는 항상 연결되어 있는 상태는 아니다.

  - 서버는 주소에 해당하는 데이터를 보내고 연결 상태를 끊기 때문에 사용자를 기억하지 못하는 특징을 가진다 (stateless)

  <br/>
  <br/>

## 쿠키 (cookies)

: 웹 사이트를 방문했을 때 브라우저에 저장되는 기록물  
(예) 로그인 <br/>
=> 맨 처음 로그인 할 때 쿠키 저장 <br/>
=> 같은 사이트에 재접속 시 서버가 쿠키를 확인하여 로그인 상태 유지   <br/>
(예) 웹페이지에서 언어 설정 <br/>
=> 재접속 시 동일한 언어로 설정되어 있다 <br/>
#### 쿠키의 규칙
1. 쿠키는 도메인 1개에만 한정
2. 쿠키는 자동으로 전송
3. 쿠키는 브라우저에 자동으로 저장

#### 쿠키와 세션
- 세션 : 서버에 인증된 클라이언트의 정보를 서버에서 저장하고 관리하는 방식
- 쿠키는 세션 ID를 포함하고 있고 이를 서버에 전송
- 쿠키는 세션 ID를 전달하는 매개체 역할

  <br/>
  <br/>

## 토큰
- 쿠키를 사용할 수 없는 경우에 사용할 수 있는 것
- 쿠키는 웹 브라우저 환경에서만 사용 가능하다
- iOS, Android에서는 쿠키 사용 불가 -> 토큰 사용
#### JWT(Json Web Token)
- 세션과 달리 서버의 DB에 사용자를 생성하는 과정이 없다.
- ‘사인된 정보’를 string(문자열) 형태로 보내고, 이 사인된 정보(토큰)을 서버에 보내고 서버는 토큰이 유효한지만 검사 
##### JWT 진행 순서
1. 클라이언트 사용자가 아이디, 패스워드를 통해 웹서비스 인증
2. 서버에서 서명된(Signed) JWT를 생성하여 클라이언트에 응답으로 돌려주기
3. 클라이언트가 서버에 데이터를 추가적으로 요구할 때 JWT를 HTTP Header에 첨부
4. 서버에서 클라언트로부터 온 JWT를 검

  <br/>
  <br/>

## HTML, CSS, JavaScript
#### HTML
- 웹 문서의 뼈대를 만드는 HTML(HyperText Markup Language)
- 프로그래밍 언어가 아닌 웹 페이지의 구조를 기술하는 마크업 언어
#### CSS
- 웹 문서를 꾸미는 CSS(Cascading Style Sheets)
- 웹 문서의 디자인을 구성
#### JavaScript
- HTML, CSS로는 할 수 없는 동적으로 콘텐츠를 바꾸고 멀티미디어 제어, 애니메이션을 추가할 수 있는 스크립팅 언어

  <br/>
  <br/>

## 라이브러리와 프레임워크
<table>
  <tr>
    <td></td>
    <td>라이브러리</td>
    <td>프레임워크</td>
  </tr>
  <tr>
    <td>공통점</td>
    <td  colspan="2">- 누군가가 미리 작성해 놓은 코드를 포함 <br/>
- 개발 속도를 더 빠르게 만들어 준다. </td>
  </tr>
  <tr>
    <td>차이점</td>
    <td>- 필요할 때 가져와서 사용할 수 있다 <br/>
    - 제어의 주체가 '나'에게 있다 <br/>
    (예) React (프레임워크의 성격도 띄고 있다)</td>
    <td>- 제어 주체는 프레임워크 <br/>
    - 프레임워크의 규칙을 잘 지켜서 코드를 작성해야 한다. <br/>
    (예) Spring</td>
  </tr>
</table>

  <br/>
  <br/>

## API와 JSON
#### API(Application Programming Interface)
- 프론트엔드와 백엔드가 서로 통신을 하기 위해 약속한 인터페이스
#### JSON
- 백엔드에서 프론트엔드에게 보내는 응답에 대한 약속
- key-value 로 이루어진 형태
```
{
    "name": "seoyeon",
    "age": "26",
    "stack": [
        "JavaScript",
        "TypeScript"
    ]
}
```