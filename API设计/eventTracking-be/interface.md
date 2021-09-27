# eventTracking 埋点系统 - 服务端 API 设计

<!-- TOC -->

- [eventTracking 埋点系统 - 服务端 API 设计](#eventtracking-埋点系统---服务端-api-设计)
  - [1. 埋点上报 /eventTracking/submit/{env}/{type}](#1-埋点上报-eventtrackingsubmitenvtype)
  - [2. 查询埋点统计 /eventTracking/query](#2-查询埋点统计-eventtrackingquery)

<!-- /TOC -->

## 1. 埋点上报 /eventTracking/submit/{env}/{type}

|          |                              |
| -------- | ---------------------------- |
| 请求方法 | POST                         |
| 路由参数 | env: Env<br/>type: EventType |
| 请求体   | EventSubmitBody              |
| 响应对象 | 200 表示成功                 |
| 异常响应 | ExceptionResponse            |

## 2. 查询埋点统计 /eventTracking/query

|          |                                                                                                                                                                                                                                         |
| -------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 请求方法 | GET                                                                                                                                                                                                                                     |
| 查询参数 | appName?: string<br/>env?: Env<br/>method?: QueryMethod<br/>unit?: QueryUnit<br/>type?: EventType<br/>userId?: number<br/>customEvent?: string<br/>target?: string<br/>denominator?: string<br/>startTime?: number<br/>endTime?: number |
| 响应对象 | EventQuerySummary                                                                                                                                                                                                                       |
