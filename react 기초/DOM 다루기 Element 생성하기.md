DOM 이란 무엇인가?

DOM이란 Document Object Model 
XML이나 HTML 문서에 접근하기 위한 일종의 인터페이스입니다.
이 객체 모델은 문서 내의 모든 요소를 정의하고, 각각의 요소에 접근하는 방법을 제공합니다.

이러한 DOM은 W3C의 표준 객체 모델이며, 다음과 같은 계층 구조로 표현됩니다.

![image](https://user-images.githubusercontent.com/105036532/188553030-a1682489-d8ea-46e5-9774-e2bff45edfe7.png)


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
