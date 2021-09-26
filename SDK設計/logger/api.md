# logger 日志系统 - SDK API 设计

關於文檔中的類型設計參考 /API 設計 中的相關文檔。

## connect

- url: /logger/submit/connect

|          |     |
| -------- | --- |
| 函數参数 |   x  |
| 返回值   |   bool  |
| 异常响应 |  ExceptionResponse   |

## disconnect

- url: /logger/submit/disconnect

|          |     |
| -------- | --- |
| 函數参数 |   x  |
| 返回值   |  bool   |
| 异常响应 |   ExceptionResponse  |

## open

- url: /logger/submit/open

|          |     |
| -------- | --- |
| 函數参数 |   x  |
| 返回值   |   LoggerDispatcher  |
| 异常响应 |  ExceptionResponse   |

## close

- url: /logger/submit/close

|          |     |
| -------- | --- |
| 函數参数 |   x  |
| 返回值   |    bool |
| 异常响应 |   ExceptionResponse  |

## log

- url: /logger/submit/{env}/log

|          |                                                      |
| -------- | ---------------------------------------------------- |
| 函數参数 | env: Env<br/>type: `LOG`<br /> logger: LogSubmitBody |
| 返回值   | res: LogModel                                        |
| 异常响应 | ExceptionResponse                                    |

## info

- url: /logger/submit/{env}/info

|          |                                                       |
| -------- | ----------------------------------------------------- |
| 函數参数 | env: Env<br/>type: `INFO`<br /> logger: LogSubmitBody |
| 返回值   | res: LogModel                                         |
| 异常响应 | ExceptionResponse                                     |

## warn

- url: /logger/submit/{env}/warn

|          |                                                       |
| -------- | ----------------------------------------------------- |
| 函數参数 | env: Env<br/>type: `INFO`<br /> logger: LogSubmitBody |
| 返回值   | res: LogModel                                         |
| 异常响应 | ExceptionResponse                                     |

## error

- url: /logger/submit/{env}/error

|          |                                                        |
| -------- | ------------------------------------------------------ |
| 函數参数 | env: Env<br/>type: `ERROR`<br /> logger: LogSubmitBody |
| 返回值   | res: LogModel                                          |
| 异常响应 | ExceptionResponse                                      |

## debug

- url: /logger/submit/{env}/debug

|          |                                                        |
| -------- | ------------------------------------------------------ |
| 函數参数 | env: Env<br/>type: `DEBUG`<br /> logger: LogSubmitBody |
| 返回值   | res: LogModel                                          |
| 异常响应 | ExceptionResponse                                      |

## query

- url: /logger/query

|          |                                                                                                                                       |
| -------- | ------------------------------------------------------------------------------------------------------------------------------------- |
| 函數参数 | appName: string<br/>env: Env<br/>type: MessageType<br/>namespace: string<br/>regexp: string<br/>startTime: string<br/>endTime: string |
| 返回值   | res: LogModel[]                                                                                                                       |
| 异常响应 | ExceptionResponse                                                                                                                     |

