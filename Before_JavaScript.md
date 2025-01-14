최종 프로젝트와 관련되어, 직접적인 나의 역할 부분이 아니지만, 백엔드 부분을 하면서 프론트는 과연 무엇을 할까, 그 중에서 프론트와 관련있는 javaScripts는 무엇일까 궁금해서 검색해보다가, '웹 프로그래밍 및 자바스크립트' 관련한 수업을 무료로 들을 수가 있었다. 이에 대해 배운 것을 다음과 같이 작성하였다.

---
## 1. HTML과 CSS

HTML과 CSS는 웹 개발의 기본적인 언어들로, 웹 페이지의 구조와 스타일을 정의하는 데 사용된다.

### 1-1.**HTML (HyperText Markup Language)**  
- **역할**: 웹 페이지의 구조와 내용을 정의하는 언어.  
- **사용 예시**: 제목, 단락, 목록, 이미지, 링크 등을 정의.  
- **구성 요소**:
  - 태그(tag): `<html>`, `<head>`, `<body>`, `<h1>`, `<p>` 등.
  - 속성(attribute): 태그에 추가적인 정보를 제공. 예: `<img src="image.jpg" alt="이미지 설명">`
- **예제**:
  ```html
  <!DOCTYPE html>
  <html>
    <head>
      <title>웹 페이지 제목</title>
    </head>
    <body>
      <h1>안녕하세요!</h1>
      <p>이것은 HTML 예제입니다.</p>
    </body>
  </html>
  ```

### 1-2. **CSS (Cascading Style Sheets)**  
- **역할**: HTML로 정의된 웹 페이지의 스타일과 레이아웃을 지정하는 언어.  
- **사용 예시**: 글꼴, 색상, 여백, 정렬, 크기 등을 설정.  
- **종류**:
  1. **인라인(Inline)**: HTML 태그 내에 스타일 정의.
     ```html
     <h1 style="color: blue;">파란색 제목</h1>
     ```
  2. **내부(Internal)**: HTML 문서의 `<style>` 태그 안에 작성.
     ```html
     <style>
       p {
         color: green;
       }
     </style>
     ```
  3. **외부(External)**: 별도의 CSS 파일로 작성.  
     ```css
     /* styles.css */
     body {
       background-color: lightgray;
     }
     ```
     HTML에서 링크:
     ```html
     <link rel="stylesheet" href="styles.css">
     ```

### 1-3. HTML과 CSS의 관계  
- HTML은 **뼈대**를, CSS는 그 뼈대를 **꾸미는 도구**라고 생각하면 된다.
- HTML로는 콘텐츠를 배치하고, CSS로는 그 콘텐츠를 디자인한다.

**예제:**
```html
<!DOCTYPE html>
<html>
<head>
  <title>HTML과 CSS 예제</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background-color: #f0f0f0;
    }
    h1 {
      color: blue;
    }
    p {
      color: gray;
    }
  </style>
</head>
<body>
  <h1>HTML과 CSS</h1>
  <p>이 웹 페이지는 HTML과 CSS로 만들어졌습니다.</p>
</body>
</html>
```

----
## 2. 쿼리(Query) 

**쿼리**란, **데이터베이스(DB)**와 같은 시스템에서 정보를 요청하거나 특정 작업을 수행하기 위해 작성하는 명령이다. 주로 데이터베이스에서 원하는 데이터를 검색, 삽입, 수정, 삭제 등의 작업을 수행할 때 사용된다.

---

### **쿼리의 주요 역할**
1. **데이터 검색**  
   - 데이터베이스에서 특정 조건에 맞는 데이터를 조회.  
   - 예: 고객 목록, 제품 정보, 주문 기록 등.

2. **데이터 조작**  
   - 데이터를 추가(Insert), 수정(Update), 삭제(Delete)하는 작업.

3. **데이터 구조 관리**  
   - 테이블 생성, 수정, 삭제 등 데이터베이스의 구조를 정의.

---

### **SQL과 쿼리**
쿼리는 보통 **SQL(Structured Query Language)**을 사용하여 작성된다. SQL은 관계형 데이터베이스에서 표준으로 사용하는 언어이다.

---

### **쿼리의 종류**
1. **데이터 조회 (SELECT)**  
   - 특정 데이터나 조건에 맞는 데이터를 가져온다.
   - **예제**:
     ```sql
     SELECT * FROM users;
     SELECT name, age FROM users WHERE age > 20;
     ```

2. **데이터 삽입 (INSERT)**  
   - 테이블에 새로운 데이터를 추가.
   - **예제**:
     ```sql
     INSERT INTO users (name, age) VALUES ('홍길동', 25);
     ```

3. **데이터 수정 (UPDATE)**  
   - 기존 데이터를 수정.
   - **예제**:
     ```sql
     UPDATE users SET age = 30 WHERE name = '홍길동';
     ```

4. **데이터 삭제 (DELETE)**  
   - 특정 데이터를 삭제.
   - **예제**:
     ```sql
     DELETE FROM users WHERE age < 18;
     ```

5. **테이블 관리 (CREATE, DROP, ALTER)**  
   - 데이터베이스나 테이블을 생성, 삭제, 변경.
   - **예제**:
     ```sql
     CREATE TABLE users (
         id INT PRIMARY KEY,
         name VARCHAR(50),
         age INT
     );

     DROP TABLE users;
     ```

---

### **쿼리의 특징**
- **조건 지정 가능**: `WHERE` 절을 사용해 특정 조건에 맞는 데이터를 처리.  
- **정렬**: `ORDER BY`로 데이터를 정렬 가능.  
- **그룹화**: `GROUP BY`로 데이터를 그룹화해 요약.  
- **조인(Join)**: 여러 테이블의 데이터를 연결해 조회.  

---

### **쿼리 예제**
**회원 데이터에서 30세 이상의 이름을 가져오고, 이름 순으로 정렬:**  
```sql
SELECT name 
FROM users 
WHERE age >= 30 
ORDER BY name ASC;
```

---

### **실생활 예**
1. 쇼핑몰에서 특정 상품 검색 → 데이터베이스에 쿼리를 보내 검색 수행.
2. 은행 시스템에서 고객의 거래 내역 조회 → 쿼리로 데이터를 가져옴.
3. 학교 시스템에서 특정 학생의 성적 검색 → 쿼리를 통해 데이터 추출.

쿼리는 데이터베이스와의 대화라고 생각하면 이해하기 쉽다.

----
## 3. 웹 프로그래밍(Web programming)
프로그래밍(Programming)이란, 사람이 원하는대로 컴퓨터가 작동할 수 있도록 컴퓨터 언어로 명령어를 나열하는 행위다.
**웹 프로그래밍(Web programming)**이란, **웹 애플리케이션**이나 **웹 사이트**를 개발하기 위해 프로그래밍 언어와 기술을 사용하는 과정을 의미합니다. 사용자가 브라우저를 통해 웹 애플리케이션에 접근하여 다양한 기능과 서비스를 이용할 수 있도록 만드는 작업이다.

---

### **웹 프로그래밍의 주요 구성 요소**
웹 프로그래밍은 **클라이언트(Front-End)**와 **서버(Back-End)**의 두 가지 주요 부분으로 나뉜다.

#### **1. 클라이언트(Front-End)**
- 사용자가 직접 보고 상호작용하는 부분.
- **주요 기술**:
  - **HTML**: 웹 페이지의 구조를 정의.
  - **CSS**: 페이지의 디자인과 스타일링.
  - **JavaScript**: 동적인 동작과 사용자 인터페이스를 구현.
- **예**:
  사용자가 클릭 가능한 버튼, 드롭다운 메뉴, 애니메이션 효과 등.

#### **2. 서버(Back-End)**
- 웹 애플리케이션의 데이터 처리 및 비즈니스 로직을 담당.
- **주요 기술**:
  - **프로그래밍 언어**: Python, Java, PHP, Node.js 등.
  - **데이터베이스**: MySQL, PostgreSQL, MongoDB 등.
  - **웹 서버**: Apache, Nginx 등.
- **역할**:
  - 클라이언트 요청 처리.
  - 데이터베이스와 상호작용.
  - 응답 생성 및 전달.

---

### **웹 프로그래밍의 흐름**
1. 사용자가 브라우저에서 URL 입력.
2. **클라이언트 요청**이 서버로 전달.
3. 서버는 요청에 따라 데이터를 처리하고 결과를 생성.
4. **서버 응답**이 클라이언트로 전송.
5. 브라우저가 데이터를 렌더링해 사용자에게 표시.

---

### **웹 프로그래밍의 주요 언어 및 기술**
#### **1. 프론트엔드(Front-End)**
- **HTML**: 구조 정의.
- **CSS**: 스타일링.
- **JavaScript**: 동적인 동작 및 이벤트 처리.
- **프레임워크/라이브러리**: React, Angular, Vue.js 등.

#### **2. 백엔드(Back-End)**
- **서버 언어**: Python(Django, Flask), Java(Spring), Node.js(Express) 등.
- **데이터베이스**: MySQL, MongoDB, PostgreSQL 등.
- **API**: RESTful API, GraphQL 등.

#### **3. 기타 기술**
- **웹 서버**: Nginx, Apache.
- **클라우드 플랫폼**: AWS, Azure, Google Cloud 등.
- **도구**: Docker, Git, CI/CD.

---

### **웹 프로그래밍의 유형**
1. **정적 웹 사이트**: 고정된 콘텐츠를 제공하며, 변경하려면 HTML 파일을 직접 수정해야 한다.
2. **동적 웹 애플리케이션**: 사용자 요청에 따라 콘텐츠와 데이터를 동적으로 생성.
   - 예: SNS, 온라인 쇼핑몰, 검색 엔진.

---

### **웹 프로그래밍의 주요 개념**
1. **HTTP/HTTPS**: 클라이언트-서버 간의 통신 프로토콜.
2. **REST API**: 웹 서비스에서 데이터 전송을 위한 설계 방식.
3. **쿠키/세션**: 사용자 인증 및 상태 관리.
4. **웹 보안**: SQL Injection, XSS, CSRF 방지 등.

---

### **웹 프로그래밍 예제**
#### **HTML + CSS + JavaScript (프론트엔드)**
```html
<!DOCTYPE html>
<html>
<head>
  <title>웹 프로그래밍 예제</title>
  <style>
    body { font-family: Arial, sans-serif; background-color: #f0f0f0; }
    h1 { color: blue; }
  </style>
</head>
<body>
  <h1>안녕하세요!</h1>
  <button onclick="alert('버튼이 눌렸습니다!')">클릭하세요</button>
</body>
</html>
```

#### **Python Flask (백엔드)**
```python
from flask import Flask

app = Flask(__name__)

@app.route('/')
def home():
    return "안녕하세요! Flask로 만든 웹 애플리케이션입니다."

if __name__ == '__main__':
    app.run(debug=True)
```

---

### **웹 프로그래밍의 실제 사용 예**
1. **쇼핑몰 웹 사이트**: 상품 검색, 장바구니, 결제 기능.
2. **SNS 플랫폼**: 게시글 작성, 좋아요, 댓글 기능.
3. **온라인 뱅킹**: 계좌 조회, 이체, 거래 내역 관리.

---

즉, 웹 프로그래밍은 사용자와 시스템 간의 상호작용을 원활하게 만들어주는 핵심 기술이다.


----

## 4. 자바 스크립트(JavaScript)

**자바스크립트(JavaScript)**는 웹 페이지를 **동적**이고 **대화형**으로 만들어주는 **프로그래밍 언어**다.

웹 브라우저에서 실행되며, HTML과 CSS와 함께 웹 개발의 3대 핵심 기술 중 하나로 꼽힌다고 한다.

---

### **자바스크립트란?**
- **정의**: 웹 애플리케이션의 동작을 제어하고 사용자와 상호작용을 가능하게 하는 **스크립트 언어**.
- **범용성**: 웹 브라우저 외에도 서버(Node.js), 모바일 앱, 데스크톱 앱 등 다양한 환경에서 사용.
- **주요 특징**:
  - 인터프리터 언어(실시간 실행 가능).
  - 객체 지향과 함수형 프로그래밍을 모두 지원.
  - 브라우저에 기본적으로 내장되어 추가 설치 없이 사용 가능.

---

### **자바스크립트의 역할**
#### **1. 웹 페이지의 동적 기능 추가**
HTML은 구조를 정의하고, CSS는 스타일을 지정하는 데 사용된다. 자바스크립트는 웹 페이지에 **동적 동작**을 추가한다.
- **예**:
  - 버튼 클릭 시 새로운 콘텐츠 표시.
  - 애니메이션 효과.
  - 실시간 데이터 업데이트(AJAX).

#### **2. 사용자와의 상호작용**
웹 페이지에서 이벤트(클릭, 키 입력, 마우스 움직임 등)를 감지하고 처리.
- **예**:
  - 입력 양식 검증.
  - 알림 창 표시.
  - 드래그 앤 드롭 구현.

#### **3. 백엔드와의 통신 (AJAX, Fetch API)**
서버와 비동기 통신을 통해 데이터를 주고받아 페이지를 새로 고치지 않고 업데이트.
- **예**:
  - 실시간 댓글 시스템.
  - 검색 결과 자동 완성.
  - 무한 스크롤.

#### **4. DOM 조작**
HTML 문서를 객체(Document Object Model)로 변환하여 콘텐츠를 동적으로 변경.
- **예**:
  - 특정 텍스트를 수정하거나 추가.
  - 이미지를 바꾸거나 스타일을 동적으로 적용.
  - 요소를 추가하거나 삭제.

#### **5. 웹 애니메이션 구현**
CSS와 결합하여 복잡한 애니메이션을 제어하거나, Canvas와 WebGL을 사용해 2D/3D 그래픽 제작.
- **예**:
  - 슬라이드쇼.
  - 게임 개발.

---

### **자바스크립트의 주요 구성 요소**
1. **문법**: 
   - 변수 선언 (`let`, `const`, `var`).
   - 조건문 (`if`, `else`).
   - 반복문 (`for`, `while`).
2. **DOM API**: 
   - 웹 페이지 요소를 선택 및 수정.
   - `document.getElementById()`, `document.querySelector()`.
3. **이벤트 처리**:
   - 사용자 행동 감지 및 반응.
   - `addEventListener()` 사용.
4. **비동기 처리**:
   - 서버 통신 및 작업 실행 순서 제어.
   - `Promise`, `async/await`.
5. **브라우저 API**:
   - 로컬 저장소(`localStorage`), 쿠키 관리.
   - WebSocket, Geolocation, Notification API.

---

### **자바스크립트의 실행 환경**
#### **1. 웹 브라우저**
- 대부분의 웹 브라우저는 자바스크립트 엔진(예: Chrome의 V8)을 내장.
- 브라우저에서 HTML, CSS와 함께 동작.

#### **2. Node.js**
- 자바스크립트를 브라우저 외부에서 실행 가능하게 만든 런타임.
- 서버 개발, 파일 시스템 조작, 네트워크 작업에 사용.

---

### **자바스크립트 코드 예제**
#### **동적 버튼 동작 추가**
```html
<!DOCTYPE html>
<html>
<head>
  <title>JavaScript 예제</title>
</head>
<body>
  <h1>안녕하세요!</h1>
  <button id="myButton">클릭하세요</button>
  <p id="text"></p>
  
  <script>
    const button = document.getElementById('myButton');
    const text = document.getElementById('text');

    button.addEventListener('click', () => {
      text.textContent = '버튼이 눌렸습니다!';
    });
  </script>
</body>
</html>
```

#### **서버와 통신 (Fetch API 사용)**
```javascript
fetch('https://api.example.com/data')
  .then(response => response.json())
  .then(data => {
    console.log(data); // 서버에서 받은 데이터 출력
  })
  .catch(error => {
    console.error('오류 발생:', error);
  });
```

---

### **자바스크립트의 활용 사례**
1. **웹 애플리케이션**: Gmail, Facebook, YouTube.
2. **데스크톱 애플리케이션**: Electron 프레임워크로 Slack, Visual Studio Code 제작.
3. **서버 개발**: Node.js를 사용한 REST API, 실시간 채팅 서버.
4. **게임 개발**: HTML5 Canvas와 WebGL을 활용한 게임.

---

### **자바스크립트의 강점**
- **웹 표준**: 모든 브라우저에서 기본적으로 실행 가능.
- **확장성**: 다양한 라이브러리(React, Vue, Angular)와 프레임워크.
- **실시간 상호작용**: 동적이고 사용자 친화적인 웹 사이트 제작.

자바스크립트는 웹의 심장과 같은 역할을 하며, 현대 웹 애플리케이션에서 필수적인 기술이라고 한다.


----

여러 가지 명칭들과, 이애하기 쉽게 특징까지 공부함으로 인해 좀 더 컴퓨터 언어에 접근하지 않았을까 생각이 들었다.