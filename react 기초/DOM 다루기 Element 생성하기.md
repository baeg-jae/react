DOM 이란 무엇인가?<br/>
<br/>
DOM이란 Document Object Model <br/>
XML이나 HTML 문서에 접근하기 위한 일종의 인터페이스입니다.<br/>
이 객체 모델은 문서 내의 모든 요소를 정의하고, 각각의 요소에 접근하는 방법을 제공합니다.<br/>
<br/>
이러한 DOM은 W3C의 표준 객체 모델이며, 다음과 같은 계층 구조로 표현됩니다.<br/>
<br/>
![image](https://user-images.githubusercontent.com/105036532/188553030-a1682489-d8ea-46e5-9774-e2bff45edfe7.png)<br/>

<br/>
자바스크립트는 이러한 객체 모델을 이용하여 다음과 같은 작업을 할 수 있습니다.<br/>
<br/>
-자바스크립트는 새로운 HTML 요소나 속성을 추가할 수 있습니다.<br/>
-자바스크립트는 존재하는 HTML 요소나 속성을 제거할 수 있습니다.<br/>
-자바스크립트는 HTML 문서의 모든 HTML 요소나 속성을 변경할 수 있습니다.<br/>
-자바스크립트는 HTML 문서의 모든 CSS 스타일을 변경할 수 있습니다.<br/>
-자바스크립트는 HTML 문서에 새로운 HTML 이벤트를 추가할 수 있습니다.<br/>
-자바스크립트는 HTML 문서의 모든 HTML 이벤트에 반응할 수 있습니다.<br/>
<br/>
DOM의 종류<br/>
<br/>
W3C DOM 표준은 세 가지 모델로 구분됩니다.<br/>
<br/>
1. Core DOM : 모든 문서 타임을 위한 DOM 모델<br/>
2. HTML DOM : HTML 문서를 위한 DOM 모델<br/>
3. XML DOM : XML 문서를 위한 DOM 모델<br/>

```js
<!DOCTYPE html>
<html lang="en">
  <body>
    <script
      crossorigin
      src="https://unpkg.com/react@17/umd/react.development.js"
    ></script>
    <script
      crossorigin
      src="https://unpkg.com/react-dom@17/umd/react-dom.development.js"
    ></script>
    <div id="root"></div>
    <script>
      const rootElement = document.getElementById("root");
      // const elementV = document.createElement("hi");
      // const element = React.createElement("hi", { children: "Hello, world!" });
      const element = React.createElement("hi", null, "Hello, world!");
      // element.textContent = "Hello, world!";
      console.log(element);
      ReactDOM.render(element, rootElement);
      // rootElement.appendChild(element);
    </script>
  </body>
</html>
```
