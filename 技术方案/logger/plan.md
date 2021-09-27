# logger 日志系统 - SDK 技術方案

## SDK 技術方案思路

該 SDK 設計主要思路如下：

1. LoggerDispatcher 為具體包含日誌相關操作的類

2. LoggerDispatcher 應用單例模式

3. 通過 `connect` api 返回給調用方 LoggerDispatcher 實例

4. 通過 `disconnect` 註銷 LoggerDispatcher 實例

5. LoggerDispatcher 具體對外提供 `log`, `info`, `warn`, `error`, `debug`, `query` api

6. LoggerDispatcher 負責初始化關於環境參數、與後端連接、異常處理表現、以及對返回值的預處理(如有需要)

