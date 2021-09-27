# 通用数据模型

<!-- TOC -->

- [通用数据模型](#通用数据模型)
  - [enum Env](#enum-env)
  - [interface ExceptionResponse](#interface-exceptionresponse)

<!-- /TOC -->

## enum Env

```ts
enum Env {
    TEST = 'TEST', // 测试环境
    PRE = 'PRE', // 预发环境
    PROD = 'PROD', // 线上环境
}
```

## interface ExceptionResponse

```ts
interface ExceptionResponse {
    statusCode: number; // HttpStatus http状态码
    msg: string; // 异常信息
    detail: string; // 异常详细信息（可以是 JSON 序列化后结果）
}
```
