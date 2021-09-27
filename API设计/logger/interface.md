# logger 日志系统 - 服务端 API 设计

<!-- TOC -->

- [logger 日志系统 - 服务端 API 设计](#logger-日志系统---服务端-api-设计)
  - [1. 日志上报 /logger/submit/{env}/{type}](#1-日志上报-loggersubmitenvtype)
  - [2. 查询日志 /logger/query](#2-查询日志-loggerquery)

<!-- /TOC -->

## 1. 日志上报 /logger/submit/{env}/{type}

|          |                                |
| -------- | ------------------------------ |
| 请求方法 | POST                           |
| 路由参数 | env: Env<br/>type: MessageType |
| 请求体   | LogSubmitBody                  |
| 响应对象 | LogModel                       |
| 异常响应 | ExceptionResponse              |

## 2. 查询日志 /logger/query

|          |                                                                                                                                        |
| -------- | -------------------------------------------------------------------------------------------------------------------------------------- |
| 请求方法 | GET                                                                                                                                    |
| 查询参数 | appName: string<br/>env: Env<br/>type: MessageType<br/>namespace: string<br/>keyword: string<br/>startTime: number<br/>endTime: number |
| 响应对象 | LogModel[]                                                                                                                             |
| 异常响应 | ExceptionResponse                                                                                                                      |
