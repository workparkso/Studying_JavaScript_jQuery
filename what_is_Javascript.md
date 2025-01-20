최종 프로젝트를 하기 되면서, JavaScript에 관련해서 스치듯 듣게 되었다. 분명 중요한 것인데, 정확히 어떤 것인지 궁금했던 중에, 한정 기간동안 무료로 좋은 자료가 열린다는 소식을 듣고 신청하게 되었다. 그 중에서 JavaScirpt가 있었고, 이를 이해하기 위해 강의와 함께 공부를 시작하게 되었다. 

---

## JavaScript란?

JavaScript는 웹 개발에서 가장 널리 사용되는 프로그래밍 언어 중 하나로, 동적인 웹 페이지를 만들기 위해 사용된다.
HTML과 CSS가 웹 페이지의 구조와 스타일을 담당한다면, JavaScript는 웹 페이지에 동적인 동작을 부여한한다.  
주요 용도는 다음과 같다:  
- 사용자와의 상호작용 처리(버튼 클릭, 폼 제출 등)
- 데이터 유효성 검사
- 애니메이션 및 시각적 효과 추가
- 서버와의 통신(AJAX, Fetch API 등)

---

### <와 >는 무엇인가?

JavaScript에서 `<`와 `>`는 HTML 태그와 관련이 깊다.  
- `<script>`: HTML에서 자바스크립트를 삽입하거나 연결할 때 사용하는 태그다.
- `<`와 `>`는 HTML 태그를 구분하는 기호로, 브라우저가 태그를 인식하게 해준준다.

예를 들어:  
```html
<script>
  console.log("Hello, JavaScript!");
</script>
```

위 코드에서 `<script>`는 JavaScript 코드를 실행하기 위해 사용되는 태그다.

---

## 개발 환경 준비하기

자바스크립트를 배우기 전에 개발 환경을 준비해야 한한다.  
1. **크롬 브라우저 설치하기**  
   - [크롬 다운로드 링크](https://www.google.co.kr/chrome/)
2. **비주얼 스튜디오 코드 설치하기**  
   - [VS Code 다운로드 링크](https://code.visualstudio.com/)

---

## 자바스크립트 소스 작성 및 실행하기

#### 1. `<script>` 태그 안에 자바스크립트 작성하기
- `<script>` 태그는 HTML 문서 어디에서든 사용할 수 있다.
- 한 HTML 문서에서 여러 개의 `<script>` 태그를 사용할 수 있다.
- `<script>` 태그가 위치한 부분에서부터 JavaScript 코드가 실행된된다.

예시:
```html
<!DOCTYPE html>
<html>
<head>
  <title>JavaScript Example</title>
</head>
<body>
  <script>
    alert("JavaScript 실행!");
  </script>
</body>
</html>
```

---

#### 2. 내부 스크립트와 외부 스크립트
##### 내부 스크립트
HTML 파일 안에 `<script>` 태그를 사용해 직접 JavaScript 코드를 작성한한다.

##### 외부 스크립트
별도의 `.js` 파일을 생성하고, HTML에서 해당 파일을 `<script src="경로"></script>`로 연결한한다.

**외부 스크립트 파일 연결 예시:**
1. `js` 폴더에 `change.js`라는 파일을 생성한다.
2. `change.js`에 다음과 같은 코드를 작성한한다:
   ```javascript
   alert("외부 스크립트 실행!");
   ```
3. HTML 파일에서 외부 스크립트를 연결한한다:
   ```html
   <script src="js/change.js"></script>
   ```

---

## 사용자 입력 및 출력 방법

#### 1. 사용자 입력 값 받기: `prompt()` 함수
사용자에게 값을 입력받을 때 가장 간단히 사용할 수 있는 함수다.
```javascript
var name = prompt("이름을 입력하세요.");
console.log(name + "님, 반갑습니다!");
```

#### 2. 알림 창으로 출력하기: `alert()` 함수
웹 브라우저 화면에 간단한 알림을 출력한한다.
```javascript
alert("환영합니다!");
```

#### 3. 브라우저 화면에 출력하기: `document.write()` 함수
웹 페이지에 직접 결과를 출력한한다.
```javascript
var name = prompt("이름을 입력하세요:");
document.write(name + "님, 어서오세요!");
```

#### 4. 콘솔에 출력하기: `console.log()` 함수
브라우저의 개발자 도구 콘솔 창에 결과를 출력한한다.
```javascript
var name = prompt("이름을 입력하세요:");
console.log(name + "님, 환영합니다!");
```

---

## 자바스크립트 작성 규칙

1. **대소문자 구분**  
   - JavaScript는 대소문자를 구분한한다.  
     예: `var name`과 `var Name`은 서로 다른 변수다.
   
2. **들여쓰기와 가독성**  
   - 읽기 쉽도록 들여쓰기를 사용하도록 한다.
   ```javascript
   if (true) {
     console.log("Hello!");
   }
   ```

3. **세미콜론 사용**  
   - 문장의 끝에는 세미콜론(`;`)을 사용한다.  
   ```javascript
   var name = "John";
   alert(name);
   ```

4. **주석 사용**  
   - 주석은 코드의 가독성을 높이고 설명을 추가하는 데 유용하다.  
   ```javascript
   // 한 줄 주석
   /* 여러 줄 주석 */
   ```

5. **식별자 작성 규칙**  
   - 변수 이름은 문자, 숫자, `_`, `$`로만 구성되며, 숫자로 시작할 수 없다.  
   - 예약어(`var`, `if` 등)는 변수 이름으로 사용할 수 없다.  

---

## 추가 예제

### HTML에서 사용자와 상호작용하기
```html
<!DOCTYPE html>
<html>
<head>
  <title>JavaScript Example</title>
</head>
<body>
  <h1>JavaScript 예제</h1>
  <button onclick="greetUser()">클릭하세요</button>

  <script>
    function greetUser() {
      var name = prompt("이름을 입력하세요:");
      alert(name + "님, 환영합니다!");
    }
  </script>
</body>
</html>
```

위 예제에서 버튼을 클릭하면 `greetUser()` 함수가 실행되어 사용자와 상호작용한다.

---
## JavaScript, **백엔드(서버)**와 프론트엔드(클라이언트)와의 관계
JavaScript는 웹 개발에서 **백엔드(서버)**와 **프론트엔드(클라이언트)** 모두에서 중요한 역할을 한한다. 다음은 JavaScript가 백엔드와 프론트엔드 각각에서 어떤 역할을 하며, 이 둘을 어떻게 연결하는지 설명한 내용이이다.

---

### 1. JavaScript의 프론트엔드 역할
프론트엔드는 사용자와 직접 상호작용하는 웹 페이지의 **UI(User Interface)**를 개발하는 부분이이다.  
JavaScript는 웹 브라우저에서 동작하며, HTML과 CSS를 조작하거나 사용자 이벤트(클릭, 입력 등)를 처리하는 데 사용된된다.

#### 주요 역할:
- **동적인 UI 생성**  
  - HTML과 CSS를 조작해 버튼, 애니메이션, 팝업 등을 구현한다.
  - 예: 사용자가 버튼을 클릭하면 새로운 정보를 화면에 표시.
  
- **사용자 입력 처리**  
  - 사용자가 폼을 제출하거나 입력한 데이터를 즉시 처리.
  - 예: 입력값 유효성 검사.
  
- **비동기 데이터 통신(AJAX, Fetch API)**  
  - 서버와 통신하여 데이터를 가져오거나 보낸다.
  - 예: 사용자가 게시글을 작성하면 데이터가 서버로 전송되고 화면이 새로고침 없이 업데이트된다.
  
- **SPA(Single Page Application)** 개발  
  - React, Vue.js, Angular 같은 프레임워크를 사용해 브라우저에서 실행되는 복잡한 애플리케이션을 개발한다.

---

### 2. JavaScript의 백엔드 역할
백엔드는 사용자 요청을 처리하고 데이터베이스와 상호작용하며, 필요한 데이터를 클라이언트(프론트엔드)로 전달하는 역할을 한다.  
Node.js는 JavaScript가 서버에서도 실행될 수 있게 만든 런타임 환경으로, JavaScript가 백엔드에서 사용될 수 있게 해준다.

#### 주요 역할:
- **서버 생성 및 요청 처리**  
  - Node.js를 사용하여 서버를 만들고 HTTP 요청(예: GET, POST)을 처리.
  - 예: 사용자가 특정 페이지를 요청하면 데이터를 데이터베이스에서 가져와 반환.
  
- **데이터베이스 연동**  
  - MySQL, PostgreSQL, MongoDB 같은 데이터베이스와 상호작용.
  - 예: 회원 가입 시 사용자가 입력한 정보를 데이터베이스에 저장.
  
- **API 개발**  
  - RESTful API나 GraphQL API를 구축해 프론트엔드가 데이터를 요청하고 받을 수 있게 함.
  - 예: 게시판 애플리케이션에서 게시글 데이터를 제공하는 API.

- **실시간 처리**  
  - WebSocket을 사용해 채팅, 알림 같은 실시간 기능 구현.

---

### 3. JavaScript와 백엔드-프론트엔드의 관계

JavaScript는 **백엔드와 프론트엔드 간의 연결 고리**로 동작한다.  
프론트엔드와 백엔드가 데이터를 주고받으며 협력하는 방식은 다음과 같다:

#### 1) 프론트엔드 → 백엔드
- **요청(Request)**:  
  사용자가 입력한 데이터를 프론트엔드에서 백엔드로 전송한다.  
  예: 로그인 폼을 제출하면 사용자 ID와 비밀번호가 백엔드로 전송.

  ```javascript
  fetch('https://example.com/login', {
    method: 'POST',
    headers: {
      'Content-Type': 'application/json',
    },
    body: JSON.stringify({ username: 'user1', password: 'pass123' }),
  })
    .then(response => response.json())
    .then(data => console.log(data));
  ```

#### 2) 백엔드 → 프론트엔드
- **응답(Response)**:  
  백엔드는 요청을 처리한 후, 결과 데이터를 JSON 형태로 프론트엔드에 보낸다.  
  예: 로그인 성공 여부와 사용자 정보를 응답으로 보낸다.

  ```json
  {
    "status": "success",
    "message": "로그인 성공",
    "user": {
      "id": 123,
      "name": "홍길동"
    }
  }
  ```

#### 3) 비동기 처리
JavaScript의 비동기 처리 방식은 백엔드와의 데이터 통신에서 매우 중요한 역할을 한다.  
`AJAX`와 `Fetch API`를 사용하면 서버로부터 데이터를 받아오는 동안에도 사용자는 웹 페이지를 계속 사용할 수 있다.

---

### 4. 프론트엔드와 백엔드의 기술 스택 예시

#### 프론트엔드 기술
- HTML, CSS, JavaScript
- React.js, Vue.js, Angular
- Tailwind CSS, Bootstrap

#### 백엔드 기술
- Node.js (Express.js, Nest.js)
- Python (Django, Flask)
- Java (Spring Boot)

---

### 5. 간단한 예제: 프론트엔드와 백엔드 연동
#### 1) 백엔드(Node.js)
```javascript
// server.js
const express = require('express');
const app = express();

app.use(express.json());

app.post('/api/login', (req, res) => {
  const { username, password } = req.body;
  if (username === 'user1' && password === 'pass123') {
    res.json({ status: 'success', message: '로그인 성공' });
  } else {
    res.json({ status: 'fail', message: '로그인 실패' });
  }
});

app.listen(3000, () => console.log('Server is running on http://localhost:3000'));
```

#### 2) 프론트엔드(JavaScript)
```html
<!DOCTYPE html>
<html lang="ko">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Login Example</title>
</head>
<body>
  <h1>로그인</h1>
  <input id="username" type="text" placeholder="아이디">
  <input id="password" type="password" placeholder="비밀번호">
  <button id="loginBtn">로그인</button>

  <script>
    document.getElementById('loginBtn').addEventListener('click', () => {
      const username = document.getElementById('username').value;
      const password = document.getElementById('password').value;

      fetch('http://localhost:3000/api/login', {
        method: 'POST',
        headers: {
          'Content-Type': 'application/json',
        },
        body: JSON.stringify({ username, password }),
      })
        .then(response => response.json())
        .then(data => alert(data.message))
        .catch(error => console.error('Error:', error));
    });
  </script>
</body>
</html>
```

---

## 결론
JavaScript는 **프론트엔드에서 사용자와 상호작용**하고, **백엔드에서 데이터를 처리**하며, 이 둘을 이어주는 중요한 역할을 한다는 것을 알게되었다.
또한 Node.js를 사용하면 JavaScript 하나로 프론트엔드와 백엔드를 모두 개발할 수 있어 생산성을 높일 수 있다는 것을 보고, 다음 공부에 Node.js 포함해서 공부하면 좀 더 한걸음 다가가지 않을까 싶은 생각이 들었다.
