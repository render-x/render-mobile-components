# @x.render/render-text

<p>
<a href="https://www.npmjs.com/package/@x.render/render-text" target="__blank"><img src="https://img.shields.io/npm/v/@x.render/render-text" alt="NPM version" /></a>

<a href="https://www.npmjs.com/package/@x.render/render-text" target="__blank"><img src="https://img.shields.io/npm/dm/%40x.render%2Frender-text" alt="NPM Downloads" /></a>

</p>

[英文文档](./README.md)

## 描述

Text 用于显示文本，是一个 span 标签。

## 使用后

```bash
$ npm install  @x.render/render-text --save
```

```jsx
import View from " @x.render/render-view";
import Text from " @x.render/render-text";

const styles = {
  root: {
    width: 750,
    paddingTop: 20,
  },
  container: {
    padding: 20,
    borderStyle: "solid",
    borderColor: "#dddddd",
    borderWidth: 1,
    marginLeft: 20,
    marginRight: 20,
    marginBottom: 10,
  },
  textBlock: {
    fontWeight: "500",
    color: "blue",
  },
  logBox: {
    padding: 20,
    margin: 10,
    borderWidth: 1,
    borderColor: "#f0f0f0",
    backgroundColor: "#f9f9f9",
  },
};
const App = () => {
  return (
    <View style={styles.root}>
      <View
        style={{
          ...styles.container,
          ...{
            flexDirection: "row",
            justifyContent: "flex-start",
          },
        }}
      >
        <Text>text</Text>
        <Text
          style={{
            color: "#ff4200",
          }}
        >
          Mixing
        </Text>
      </View>

      <View style={styles.container}>
        <Text
          numberOfLines={1}
          style={{
            width: 300,
            textOverflow: "ellipsis",
          }}
        >
          Single line of text exceeds truncated text
        </Text>

        <Text
          numberOfLines={2}
          style={{
            width: 300,
            textOverflow: "ellipsis",
          }}
        >
          Multi-line text exceeds truncated text, exceeds truncated text,
          exceeds truncated text, exceeds truncated text
        </Text>
      </View>

      <View style={styles.container}>
        <Text style={{ textDecoration: "underline" }}>Text underline</Text>
        <Text style={{ textDecorationLine: "none" }}>no Underlined</Text>
        <Text style={{ textDecoration: "line-through" }}>
          Text strikethrough
        </Text>
      </View>

      <View style={styles.container}>
        <Text style={{ lineHeight: "120rpx" }}>
          Line height 120rpx, multi-line text text folding effect Multi-line
          text text folding effect
        </Text>
      </View>
    </View>
  );
};
export default App;
```

## 属性

| **属性**      | **类型** | **默认值** | **必填** | **描述** |
| ------------- | -------- | ---------- | -------- | -------- |
| numberOfLines | `number` | 1          | false    | 行数     |
