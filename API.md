<a id="opIdscheduler_timer_scheduler_timer_post"></a>

## POST Scheduler Timer

POST /scheduler/timer

> Body 请求参数

```json
{
  "timestamp": "string",
  "content": "string",
  "img_url": "string",
  "qqgroup_id": "string",
  "is_at_all": true
}
```

### 请求参数

| 名称 | 位置 | 类型                              | 必选 | 中文名      | 说明 |
| ---- | ---- | --------------------------------- | ---- | ----------- | ---- |
| body | body | [timer_model](#schematimer_model) | 否   | timer_model | none |

> 返回示例

> 200 Response

```json
"string"
```

### 返回结果

| 状态码 | 状态码含义                                                   | 说明 | 数据模型                                          |
| ------ | ------------------------------------------------------------ | ---- | ------------------------------------------------- |
| 200    | [OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)      | none | string                                            |
| 422    | [Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3) | none | [HTTPValidationError](#schemahttpvalidationerror) |

<a id="opIdscheduler_plan_scheduler_plan_post"></a>

## POST Scheduler Plan

POST /scheduler/plan

> Body 请求参数

```json
{
  "day": 0,
  "hour": 0,
  "minute": 0,
  "second": 0,
  "content": "string",
  "img_url": "string",
  "qqgroup_id": "string",
  "is_at_all": true
}
```

### 请求参数

| 名称 | 位置 | 类型                                      | 必选 | 中文名          | 说明 |
| ---- | ---- | ----------------------------------------- | ---- | --------------- | ---- |
| body | body | [scheduler_model](#schemascheduler_model) | 否   | scheduler_model | none |

> 返回示例

> 200 Response

```json
"string"
```

### 返回结果

| 状态码 | 状态码含义                                                   | 说明 | 数据模型                                          |
| ------ | ------------------------------------------------------------ | ---- | ------------------------------------------------- |
| 200    | [OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)      | none | string                                            |
| 422    | [Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3) | none | [HTTPValidationError](#schemahttpvalidationerror) |

<a id="opIdscheduler_cancel_scheduler_cancel_get"></a>

## GET Scheduler Cancel

GET /scheduler/cancel

### 请求参数

| 名称   | 位置  | 类型   | 必选 | 中文名 | 说明 |
| ------ | ----- | ------ | ---- | ------ | ---- |
| job_id | query | string | 是   |        | none |

> 返回示例

> 200 Response

```json
"string"
```

### 返回结果

| 状态码 | 状态码含义                                                   | 说明 | 数据模型                                          |
| ------ | ------------------------------------------------------------ | ---- | ------------------------------------------------- |
| 200    | [OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)      | none | string                                            |
| 422    | [Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3) | none | [HTTPValidationError](#schemahttpvalidationerror) |

<a id="opIdscheduler_list_scheduler_list_get"></a>

## GET Scheduler List

GET /scheduler/list

> 返回示例

> 200 Response

```json
"string"
```

### 返回结果

| 状态码 | 状态码含义                                              | 说明 | 数据模型 |
| ------ | ------------------------------------------------------- | ---- | -------- |
| 200    | [OK](https://tools.ietf.org/html/rfc7231#section-6.3.1) | none | string   |

<a id="opIddashboard_dashboard_get"></a>

## GET Dashboard

GET /dashboard

> 返回示例

> 200 Response

```json
{}
```

### 返回结果

| 状态码 | 状态码含义                                              | 说明 | 数据模型 |
| ------ | ------------------------------------------------------- | ---- | -------- |
| 200    | [OK](https://tools.ietf.org/html/rfc7231#section-6.3.1) | none | Inline   |

### 返回数据结构

# 数据模型

<h2 id="tocS_HTTPValidationError">HTTPValidationError</h2>

<a id="schemahttpvalidationerror"></a>
<a id="schema_HTTPValidationError"></a>
<a id="tocShttpvalidationerror"></a>
<a id="tocshttpvalidationerror"></a>

```json
{
  "detail": [
    {
      "loc": [
        "string"
      ],
      "msg": "string",
      "type": "string"
    }
  ]
}

```

HTTPValidationError

### 属性

| 名称   | 类型                                        | 必选  | 约束 | 中文名 | 说明 |
| ------ | ------------------------------------------- | ----- | ---- | ------ | ---- |
| detail | [[ValidationError](#schemavalidationerror)] | false | none | Detail | none |

<h2 id="tocS_ValidationError">ValidationError</h2>

<a id="schemavalidationerror"></a>
<a id="schema_ValidationError"></a>
<a id="tocSvalidationerror"></a>
<a id="tocsvalidationerror"></a>

```json
{
  "loc": [
    "string"
  ],
  "msg": "string",
  "type": "string"
}

```

ValidationError

### 属性

| 名称 | 类型    | 必选 | 约束 | 中文名   | 说明 |
| ---- | ------- | ---- | ---- | -------- | ---- |
| loc  | [anyOf] | true | none | Location | none |

anyOf

| 名称          | 类型   | 必选  | 约束 | 中文名 | 说明 |
| ------------- | ------ | ----- | ---- | ------ | ---- |
| » *anonymous* | string | false | none |        | none |

or

| 名称          | 类型    | 必选  | 约束 | 中文名 | 说明 |
| ------------- | ------- | ----- | ---- | ------ | ---- |
| » *anonymous* | integer | false | none |        | none |

continued

| 名称 | 类型   | 必选 | 约束 | 中文名     | 说明 |
| ---- | ------ | ---- | ---- | ---------- | ---- |
| msg  | string | true | none | Message    | none |
| type | string | true | none | Error Type | none |

<h2 id="tocS_timer_model">timer_model</h2>

<a id="schematimer_model"></a>
<a id="schema_timer_model"></a>
<a id="tocStimer_model"></a>
<a id="tocstimer_model"></a>

```json
{
  "timestamp": "string",
  "content": "string",
  "img_url": "string",
  "qqgroup_id": "string",
  "is_at_all": true
}

```

timer_model

### 属性

| 名称       | 类型    | 必选  | 约束 | 中文名           | 说明                             |
| ---------- | ------- | ----- | ---- | ---------------- | -------------------------------- |
| timestamp  | string  | true  | none | 时间戳           | 在设置的时间戳的时间执行发送消息 |
| content    | string  | true  | none | 内容             | 发送的内容                       |
| img_url    | string  | false | none | 图片链接         | 发送的图片的url                  |
| qqgroup_id | string  | true  | none | QQ群号           | 发送到哪个QQ群                   |
| is_at_all  | boolean | true  | none | 是否艾特全体成员 | 是否艾特全体成员                 |

<h2 id="tocS_scheduler_model">scheduler_model</h2>

<a id="schemascheduler_model"></a>
<a id="schema_scheduler_model"></a>
<a id="tocSscheduler_model"></a>
<a id="tocsscheduler_model"></a>

```json
{
  "day": 0,
  "hour": 0,
  "minute": 0,
  "second": 0,
  "content": "string",
  "img_url": "string",
  "qqgroup_id": "string",
  "is_at_all": true
}

```

scheduler_model

### 属性

| 名称       | 类型    | 必选  | 约束 | 中文名           | 说明                       |
| ---------- | ------- | ----- | ---- | ---------------- | -------------------------- |
| day        | integer | true  | none | 每隔几天发送一次 | 不能为0，1为每天发送一次   |
| hour       | integer | true  | none | 几时             | 在需要发送的当天的几时发送 |
| minute     | integer | true  | none | 几分             | 在需要发送的当天的几分发送 |
| second     | integer | true  | none | 几秒             | 在需要发送的当天的几秒发送 |
| content    | string  | true  | none | 内容             | 发送的内容                 |
| img_url    | string  | false | none | 图片链接         | 发送的图片的url            |
| qqgroup_id | string  | true  | none | QQ群号           | 发送到哪个QQ群             |
| is_at_all  | boolean | true  | none | 是否艾特全体成员 | 是否艾特全体成员           |

