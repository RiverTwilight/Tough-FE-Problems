# 前端疑难杂症合集

## Map 返回 Object 时的 Lint 问题

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/d34ae09a-fde3-41cf-a69c-2753f405b72a/Untitled.png)

```jsx
const launchOptimistic = rockets.map((elem) => ({
	country: elem.country,
	launches: elem.launches + 10,
}));
```

## React 中使用 input[type=file] 的问题

```jsx
if (this.props.webkitdirectory) {
			var inputEle = ReactDOM.findDOMNode(
				this.refs.input
			) as HTMLInputElement;

			inputEle.setAttribute("webkitdirectory", "");
		}
```

由于`webkitdirectory`不是 w3c 的标准属性，所以你无法在 JSX 中直接声明。

## 模拟安卓桌面滚动效果（粘性滚动）
