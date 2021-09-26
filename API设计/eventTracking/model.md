# eventTracking Model

<!-- TOC -->

- [eventTracking Model](#eventtracking-model)
  - [enum EventType](#enum-eventtype)
  - [interface EventSubmitBody](#interface-eventsubmitbody)
  - [enum QueryMethod 埋点查询统计单位](#enum-querymethod-埋点查询统计单位)
  - [enum QueryUnit 统计单位](#enum-queryunit-统计单位)
  - [interface EventRecordModel](#interface-eventrecordmodel)
  - [interface EventStatistic](#interface-eventstatistic)
  - [interface EventQuerySummary 埋点事件统计数据](#interface-eventquerysummary-埋点事件统计数据)

<!-- /TOC -->

## enum EventType

```ts
enum EventType {
    USER_CLICK = 'USER_CLICK',
    USER_STAY = 'USER_STAY',
    PAGE_ENTER = 'PAGE_ENTER',
    PAGE_STAY = 'PAGE_STAY',
    VIDEO_OPEN = 'VIDEO_OPEN',
    VIDEO_STAY = 'VIDEO_STAY',
    FORM_PICK = 'FORM_PICK',
    FORM_STAY = 'FORM_STAY',
    API_REQUEST = 'API_REQUEST',
    API_RESPONSE = 'API_RESPONSE',
    CUSTOM = 'CUSTOM',
}
```

## interface EventSubmitBody

```ts
interface EventSubmitBody {
    appName: string;
    userId: number;
    customEvent?: string;
    target: string; // 埋点目标
    actionDetail?: string; // 埋点行为详细描述
    context: string; // 埋点具体数据：JSON 对象序列化结果
}
```

## enum QueryMethod 埋点查询统计单位

```ts
enum QueryMethod {
    COUNT = 'COUNT', // 数量统计
    DURATION = 'DURATION', // 时长统计
    RATE = 'RATE', // 比率统计
}
```

## enum QueryUnit 统计单位

```ts
enum QueryUnit {
    USER = 'USER',
    YEAR = 'YEAR',
    MONTH = 'MONTH',
    DAY = 'DAY',
}
```

## interface EventRecordModel

```ts
interface EventRecordModel {
    id: number;
    appName: string;
    env: Env;
    type: EventType;
    userId: number;
    customEvent: string | null;
    actionDetail: string;
    context: string;
    createTime: number;
    lastModifiedTime: number;
}
```

## interface EventStatistic

```ts
interface EventStatistic {
    startTime: number;
    endTime: number;
    userId?: number;
    value: number;
}
```

## interface EventQuerySummary 埋点事件统计数据

```ts
interface EventQuerySummary {
    records: EventRecordModel[];
    result: EventStatistic[]
}
```
