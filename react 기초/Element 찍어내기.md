Element 찍어내기 </br>
Function -> 재사용 가능한 Element </br>
Custom Element -> Uppercase </br>
Children 제한 없음 </br>

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
      const paint = (title, description) => (
        <>
          <h1>{title}</h1>
          <h3>{description}</h3>
        </>
      );

      // const Paint = ({ title, description }) => (
      //   <>
      //     <h1>{title}</h1>
      //     <h3>{description}</h3>
      //   </>
      // );
      //밑에 꺼와 위에꺼와 동일하다.
      const Paint = ({ title, description, children }) => {
        return (
          <>
            <h1>{title}</h1>
            <h3>{description}</h3>
            {children}
          </>
        );
      };
      const element = (
        <>
          <Paint title="Good" description="good">
            <h1>Hi</h1>
          </Paint>
          {paint("Bad", "bad")}
          {paint("So so", "so so")}
        </>
      );

      ReactDOM.render(element, rootElement);
    </script>
  </body>
</html>
```

JS와 JSX와 HTML를 다 썩어서 쓰고있다.
