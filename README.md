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
* 分析 project1 的 js 依赖
    * project_1
    * deps_1.ts        
* 递归分析 project2 的 js 依赖
> 使用递归获取嵌套依赖
    * project_2
    ```
    index -> a -> dir/a2 -> dir/dir_in_dir/a3
    index -> b -> dir/b2 -> dir/dir_in_dir/b3
    ```
    * deps_2.ts
* 分析 project3 的 js 循环依赖
> 设置缓存，每次检查当前依赖是否已经分析过，类似思路参考[剑指 Offer 35. 复杂链表的复制【链表-深度拷贝链表】](https://github.com/Hanqing1996/Leetcode/blob/master/js/%E5%89%91%E6%8C%87%20Offer%2035.%20%E5%A4%8D%E6%9D%82%E9%93%BE%E8%A1%A8%E7%9A%84%E5%A4%8D%E5%88%B6%E3%80%90%E9%93%BE%E8%A1%A8-%E6%B7%B1%E5%BA%A6%E6%8B%B7%E8%B4%9D%E9%93%BE%E8%A1%A8%E3%80%91.js)

