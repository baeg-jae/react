DOM 이란 무엇인가?

```<!DOCTYPE html>
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
</html>```javaScript
