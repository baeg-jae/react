JSX란
JSX(JavaScript XML)은 JavaScript에 XML을 추가한 확장한 문법이다.
JSX는 리액트로 프로젝트를 개발할 때 사용되므로 공식적인 자바스크립트 문법은 아니다.
브라우저에서 실행하기 전에 바벨을 사용하여 일반 자바스크립트 형태의 코드로 변환된다.
JSX는 하나의 파일에 자바스크립트와 HTML을 동시에 작성하여 편리하다.
자바스크립트에서 HTML을 작성하듯이 하기 때문에 가독성이 높고 작성하기 쉽다.(주관적인 관점)

XML이란?
XML(Extensible Markup Language)은 W3C에서 개발된, 다른 특수한 목적을 갖는 마크업 언어를 만드는데 사용하도록 권장하는 다목적 마크업 언어이다. 
XML은 SGML의 단순화된 부분집합으로, 다른 많은 종류의 데이터를 기술하는 데 사용할 수 있다.

Bable이란
Bable is a JavaScript compiler.
정확히 Bable은 javascript로 결과물을 만들어주는 컴파일러입니다.
컴파일러 : 언어 해석기, 특정 언어를 다른 프로그래밍 언어로 옮기는 프로그램
https://babeljs.io/
```js
<!DOCTYPE html>
<html lang="en">
  <body>
    <script src="https://unpkg.com/react@17/umd/react.development.js"></script>
    <script src="https://unpkg.com/react-dom@17/umd/react-dom.development.js"></script>
    <script src="https://unpkg.com/@babel/standalone/babel.min.js"></script>

    <div id="root"></div>
    <script type="text/babel">
      const rootElement = document.getElementById("root");
      // const elementV = document.createElement("hi");
      // const element = React.createElement("hi", { children: "Hello, world!" });
      const text = "Hello, world";
      const titleClassName = "title";
      // const customH1 = <h1 className={titleClassName}>{text}</h1>;
      // const customH1 = <h1 className={titleClassName} children={text} />;
      const props = { className: titleClassName, children: text };
      const customH1 = <h1 {...props} />;
      //위 문장을 풀어쓰면 이렇게
      // const customH1 = (
      //   <h1 className={props.className} children={props.children} />
      // );
      const element = customH1;
      // const element = React.createElement("hi", {
      //   className: "title",
      //   children: ["Hello, world!!!!!", "  I love duck"]
      // });
      // element.textContent = "Hello, world!";
      ReactDOM.render(element, rootElement);
      // rootElement.appendChild(element);
    </script>
  </body>
</html>
```
