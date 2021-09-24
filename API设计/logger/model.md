# logger Model

<!-- TOC -->

- [logger Model](#logger-model)
  - [enum MessageType](#enum-messagetype)
  - [interface LogSubmitBody](#interface-logsubmitbody)
  - [interface LoggerInfo](#interface-loggerinfo)

<!-- /TOC -->

## enum MessageType

```ts
enum MessageType {
    LOG = 'log',
    INFO = 'info',
    WARN = 'warn',
    ERROR = 'error',
    DEBUG = 'debug'
}
```

## interface LogSubmitBody

```ts
interface LogSubmitBody {
    appName: string;
    userId: number;
    namespace: string;
    text: string;
}
```

## interface LoggerInfo

```ts
interface LogModel {
    id: number;
    appName: string;
    env: Env;
    type: MessageType;
    userId: number;
    namespace: string;
    text: string;
    createTime: number;
    lastModifiedTime: number;
}
```
