# bytemd-plugin-image-lazy

一个用于 ByteMD 编辑器的图片懒加载插件。

## 特性

- 支持原生懒加载
- 支持自定义加载占位图
- 支持自定义类名
- 支持使用 Intersection Observer 实现懒加载

## 安装

```bash
npm install bytemd-plugin-image-lazy
# or
yarn add bytemd-plugin-image-lazy
# or
pnpm add bytemd-plugin-image-lazy
```

## 使用

```typescript
import { Editor } from "bytemd";
import imageLazyLoad from "bytemd-plugin-image-lazy";

const plugins = [
  imageLazyLoad({
    useNativeLazy: true, // 是否使用原生懒加载
    placeholderSrc: "", // 自定义加载占位图
    className: "", // 自定义类名
  }),
];

function App() {
  return <Editor plugins={plugins} />;
}
```

## 配置项

| 参数           | 类型    | 默认值 | 说明                 |
| -------------- | ------- | ------ | -------------------- |
| useNativeLazy  | boolean | true   | 是否使用原生懒加载   |
| placeholderSrc | string  | ''     | 自定义加载占位图 URL |
| className      | string  | ''     | 自定义类名           |

## 开发

```bash
# 安装依赖
pnpm install

# 构建
pnpm build
```

## License

MIT © [luckySnail](https://luckysnail.cn)
