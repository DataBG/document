# logger 日志系统 - SDK 技術方案

## SDK 技術方案思路

該 SDK 設計主要思路如下：

1. Logger 為具體包含日誌相關操作的對象

2. 通過 `init` 管理並初始化好 SDK 環境，並且負責建立與後端連接

3. Logger 具體對外提供 `log`, `info`, `warn`, `error`, `debug` api

4. 另外需單獨暴露一個 `query` api

5. 通過鎖機制強制調用方對 `init` 的調用順序優先於其他 api

## API 設計

### init

```ts
const init = (def: DEF) => {
  // 初始化 SDK 環境
  // 建立與後端連接
};
```

### log, info, warn, error, debug

- log, info, warn, error, debug 用 `f` 表示

```ts
const f = (env: ENV, type: MessageType.f, logger: LogSubmitBody) => {
  // 發送請求邏輯
};
```

### query

```ts
const query = (
  appName: string,
  env: Env,
  type: MessageType,
  namespace: string,
  keyword: string,
  startTime: string,
  endTime: string
) => {
  // 發送請求邏輯
};
```

## model

- DEF

```ts
interface DEF {
  appName: string;
  namespace: string;
  env: ENV;
}
```
