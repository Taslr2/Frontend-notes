#  TS简介

>Typed JavaScript at Any Scale.
>添加了类型系统的 JavaScript，适用于任何规模的项目。

### TypeScript 的特性

1. ##### TypeScript 是静态类型

   类型系统按照「类型检查的时机」来分类，可以分为动态类型和静态类型。

   动态类型是指在运行时才会进行类型检查，这种语言的类型错误往往会导致运行时错误。JavaScript 是一门解释型语言，没有编译阶段，所以它是动态类型，以下这段代码在运行时才会报错：

   ​

   ```javascript
   let foo = 1;
   foo.split(' ');
   // Uncaught TypeError: foo.split is not a function
   // 运行时会报错（foo.split 不是一个函数），造成线上 bug
   ```

   静态类型是指编译阶段就能确定每个变量的类型，这种语言的类型错误往往会导致语法错误。TypeScript 在运行前需要先编译为 JavaScript，而在编译阶段就会进行类型检查，所以TypeScript 是静态类型，这段 TypeScript 代码在编译阶段就会报错了：

   ​

   ```typescript
   let foo = 1;
   foo.split(' ');
   // Property 'split' does not exist on type 'number'.
   // 编译时会报错（数字没有 split 方法），无法通过编译
   ```

   ​

