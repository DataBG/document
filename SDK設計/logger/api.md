# logger 日志系统 - SDK API 设计

關於文檔中的類型設計參考 /API 設計 中的相關文檔。

## init

|          |                   |
| -------- | ----------------- |
| 函數参数 | def: Def          |
| 返回值   | void              |
| 异常响应 | ExceptionResponse |

## log

- url: /logger/submit/{env}/log

|          |                                       |
| -------- | ------------------------------------- |
| 函數参数 | text: string <br />namespace?: string |
| 返回值   | res: LogModel                         |
| 异常响应 | ExceptionResponse                     |

## info

- url: /logger/submit/{env}/info

|          |                                       |
| -------- | ------------------------------------- |
| 函數参数 | text: string <br />namespace?: string |
| 返回值   | res: LogModel                         |
| 异常响应 | ExceptionResponse                     |

## warn

- url: /logger/submit/{env}/warn

|          |                                       |
| -------- | ------------------------------------- |
| 函數参数 | text: string <br />namespace?: string |
| 返回值   | res: LogModel                         |
| 异常响应 | ExceptionResponse                     |

## error

- url: /logger/submit/{env}/error

|          |                                       |
| -------- | ------------------------------------- |
| 函數参数 | text: string <br />namespace?: string |
| 返回值   | res: LogModel                         |
| 异常响应 | ExceptionResponse                     |

## debug

- url: /logger/submit/{env}/debug

|          |                                       |
| -------- | ------------------------------------- |
| 函數参数 | text: string <br />namespace?: string |
| 返回值   | res: LogModel                         |
| 异常响应 | ExceptionResponse                     |

## query

- url: /logger/query/all

|          |                   |
| -------- | ----------------- |
| 函數参数 | param: IQuery     |
| 返回值   | res: LogModel[]   |
| 异常响应 | ExceptionResponse |

## queryAll

- url: /logger/query

|          |                   |
| -------- | ----------------- |
| 函數参数 | x                 |
| 返回值   | res: LogModel[]   |
| 异常响应 | ExceptionResponse |
