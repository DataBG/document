# logger Model

<!-- TOC -->

- [logger Model](#logger-model)
  - [enum MessageType](#enum-messagetype)
  - [interface LogSubmitBody](#interface-logsubmitbody)
  - [interface LogModel](#interface-logmodel)

<!-- /TOC -->

## enum MessageType

```ts
enum MessageType {
    LOG = 'LOG',
    INFO = 'INFO',
    WARN = 'WARN',
    ERROR = 'ERROR',
    DEBUG = 'DEBUG',
}
```

## interface LogSubmitBody

```ts
interface LogSubmitBody {
    appName: string;
    userId?: number;
    namespace?: string;
    text: string;
}
```

## interface LogModel

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
