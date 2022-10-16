# 前端疑难杂症合集

## Map 返回 Object 时的 Lint 问题

![image](https://user-images.githubusercontent.com/52880665/196023762-76da513c-f5e6-4063-aee0-d45d18033c61.png)

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
