#### 运行 ts
```ts
node -r ts-node/register xxx.ts
```
#### 在 chrome 中 debug
```js
node -r ts-node/register --inspect-brk xxx.ts 
```
之后打开 chrome ,点击新出现的 Node 图标即可
---
#### babel 的原理
* parse: 把代码 code 变成 AST
* traverse: 遍历 AST 进行修改
* enerate: 把 AST 变成代码 code2

即 code --(1)-> ast --(2)-> ast2 --(3)-> code2
---
#### 主要实验
* let 转 var
    * let_to_var.ts
* es6 转 es5
    * to_es5.ts
* 分析项目的 js 依赖
    * project_1
    * deps_1.ts        