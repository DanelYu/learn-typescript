# The Basic

## tsc

TypeScript 编译器 可以通过`tsc xxx.ts` 来进行类型检查并编译输出为`xxx.js`

1. `--noEmitOnError` 使用此选项时,tsc 遇见类型错误后不会继续编译输出 js
2. `--init` 生成 tsconfig.json 配置文件
3. `--target` 编译的目标 js 版本

## Explicit Types 显式类型

> typescript 会自动进行类型推导,并不需要对所有的变量/函数等 都进行类型声明

```typescript
function greet(person: string, date: Date) {
    console.log(`Hello ${person}, today is ${date.toDateString()}!`)
}
```

## Erased Types 类型擦除

> TypeScript 默认编译目标版本 ES3

编译后大多数特定于 TypeScript 的代码都会被擦除,如`type` `interface` 等

## Strictness 严格模式

1. `noImplicitAny` 禁用隐式的 any 类型
2. `strictNullChecks` null 和 undefined 类型安全(空类型安全)
