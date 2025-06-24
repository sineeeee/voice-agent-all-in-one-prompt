---
title: vPOS
language_tabs:
  - shell: Shell
  - http: HTTP
  - javascript: JavaScript
  - ruby: Ruby
  - python: Python
  - php: PHP
  - java: Java
  - go: Go
toc_footers: []
includes: []
search: true
code_clipboard: true
highlight_theme: darkula
headingLevel: 2
generator: "@tarslib/widdershins v4.0.30"

---

# vPOS

Base URLs:

# Authentication

# V1/店铺产品订单

<a id="opIdedit"></a>

## PUT 修改店铺产品订单

PUT /restful/v1/vpos/shopProductOrder

修改店铺产品订单

> Body 请求参数

```json
{
  "id": 0,
  "customerPhone": "string",
  "customerName": "string",
  "status": "string",
  "estimatedWaitTime": 0,
  "notes": "string",
  "type": "string",
  "subtotal": 0,
  "details": [
    {
      "id": 0,
      "shopId": 0,
      "productId": 0,
      "orderId": 0,
      "price": "string",
      "quantity": 0,
      "totalAmount": 0,
      "options": "string",
      "productJson": "string",
      "status": "string",
      "remark": "string"
    }
  ],
  "discount": 0,
  "tax": 0,
  "billTotal": 0,
  "paidAmount": 0,
  "paymentStatus": "string",
  "paymentMethod": "string",
  "paymentInfo": "string",
  "shopId": 0,
  "customerId": 0,
  "completedAt": "2019-08-24T14:15:22Z",
  "remark": "string",
  "bookTime": "2019-08-24T14:15:22Z"
}
```

### 请求参数

|名称|位置|类型|必选|说明|
|---|---|---|---|---|
|body|body|[VposShopProductOrderBo](#schemavposshopproductorderbo)| 否 |none|

> 返回示例

> 200 Response

```
{"code":0,"msg":"string","data":{}}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[RVoid](#schemarvoid)|

<a id="opIdadd"></a>

## POST 新增店铺产品订单

POST /restful/v1/vpos/shopProductOrder

新增店铺产品订单

> Body 请求参数

```json
{
  "id": 0,
  "customerPhone": "string",
  "customerName": "string",
  "status": "string",
  "estimatedWaitTime": 0,
  "notes": "string",
  "type": "string",
  "subtotal": 0,
  "details": [
    {
      "id": 0,
      "shopId": 0,
      "productId": 0,
      "orderId": 0,
      "price": "string",
      "quantity": 0,
      "totalAmount": 0,
      "options": "string",
      "productJson": "string",
      "status": "string",
      "remark": "string"
    }
  ],
  "discount": 0,
  "tax": 0,
  "billTotal": 0,
  "paidAmount": 0,
  "paymentStatus": "string",
  "paymentMethod": "string",
  "paymentInfo": "string",
  "shopId": 0,
  "customerId": 0,
  "completedAt": "2019-08-24T14:15:22Z",
  "remark": "string",
  "bookTime": "2019-08-24T14:15:22Z"
}
```

### 请求参数

|名称|位置|类型|必选|说明|
|---|---|---|---|---|
|body|body|[VposShopProductOrderBo](#schemavposshopproductorderbo)| 否 |none|

> 返回示例

> 200 Response

```
{"code":0,"msg":"string","data":{}}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[RVoid](#schemarvoid)|

<a id="opIdgetInfo"></a>

## GET 获取店铺产品订单详细信息

GET /restful/v1/vpos/shopProductOrder/{id}

获取店铺产品订单详细信息

### 请求参数

|名称|位置|类型|必选|说明|
|---|---|---|---|---|
|id|path|integer(int64)| 是 |主键|

> 返回示例

> 200 Response

```
{"code":0,"msg":"string","data":{"id":0,"orderNo":"string","customerPhone":"string","customerName":"string","status":"string","estimatedWaitTime":0,"notes":"string","type":"string","subtotal":0,"discount":0,"tax":0,"billTotal":0,"paidAmount":0,"paymentStatus":"string","paymentMethod":"string","paymentInfo":"string","shopId":0,"customerId":0,"shopName":"string","completedAt":"2019-08-24T14:15:22Z","createTime":"2019-08-24T14:15:22Z","updateTime":"2019-08-24T14:15:22Z","remark":"string","details":[{}],"orders":[{"id":0,"orderNo":"string","customerPhone":"string","customerName":"string","status":"string","estimatedWaitTime":0,"notes":"string","type":"string","subtotal":0,"discount":0,"tax":0,"billTotal":0,"paidAmount":0,"paymentStatus":"string","paymentMethod":"string","paymentInfo":"string","shopId":0,"customerId":0,"shopName":"string","completedAt":"2019-08-24T14:15:22Z","createTime":"2019-08-24T14:15:22Z","updateTime":"2019-08-24T14:15:22Z","remark":"string","details":[{}],"orders":[{"id":null,"orderNo":null,"customerPhone":null,"customerName":null,"status":null,"estimatedWaitTime":null,"notes":null,"type":null,"subtotal":null,"discount":null,"tax":null,"billTotal":null,"paidAmount":null,"paymentStatus":null,"paymentMethod":null,"paymentInfo":null,"shopId":null,"customerId":null,"shopName":null,"completedAt":null,"createTime":null,"updateTime":null,"remark":null,"details":null,"orders":null,"ips":null}],"ips":["string"]}],"ips":["string"]}}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[RVposShopProductOrderVo](#schemarvposshopproductordervo)|

<a id="opIdlist"></a>

## GET 查询店铺产品订单列表

GET /restful/v1/vpos/shopProductOrder/list

查询店铺产品订单列表

### 请求参数

|名称|位置|类型|必选|说明|
|---|---|---|---|---|
|params|query|object| 否 |请求参数|
|pageNum|query|integer(int32)| 是 |页码|
|pageSize|query|integer(int32)| 是 |每页大小|
|id|query|integer(int64)| 否 |订单编号|
|ids|query|string| 否 |none|
|orderNo|query|string| 否 |订单号|
|customerPhone|query|string| 否 |订购人电话|
|customerName|query|string| 否 |订购人姓名|
|status|query|string| 否 |订单状态|
|notes|query|string| 否 |客户备注|
|type|query|string| 否 |订单类型|
|paymentStatus|query|string| 否 |支付状态|
|paymentMethod|query|string| 否 |支付方式|
|paymentInfo|query|string| 否 |支付信息|
|shopId|query|string| 否 |所属店铺编号|
|customerId|query|string| 否 |客户编号|
|completedAt|query|string(date-time)| 否 |完成时间|
|createTime|query|string(date-time)| 否 |创建时间|
|remark|query|string| 否 |备注|
|bookTime|query|string(date-time)| 否 |预约时间|

> 返回示例

> 200 Response

```
{"code":0,"msg":"string","data":[{"id":0,"orderNo":"string","customerPhone":"string","customerName":"string","status":"string","estimatedWaitTime":0,"notes":"string","type":"string","subtotal":0,"discount":0,"tax":0,"billTotal":0,"paidAmount":0,"paymentStatus":"string","paymentMethod":"string","paymentInfo":"string","shopId":0,"customerId":0,"shopName":"string","completedAt":"2019-08-24T14:15:22Z","createTime":"2019-08-24T14:15:22Z","updateTime":"2019-08-24T14:15:22Z","remark":"string","details":[{}],"orders":[{"id":0,"orderNo":"string","customerPhone":"string","customerName":"string","status":"string","estimatedWaitTime":0,"notes":"string","type":"string","subtotal":0,"discount":0,"tax":0,"billTotal":0,"paidAmount":0,"paymentStatus":"string","paymentMethod":"string","paymentInfo":"string","shopId":0,"customerId":0,"shopName":"string","completedAt":"2019-08-24T14:15:22Z","createTime":"2019-08-24T14:15:22Z","updateTime":"2019-08-24T14:15:22Z","remark":"string","details":[{}],"orders":[{}],"ips":["string"]}],"ips":["string"]}]}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[RListVposShopProductOrderVo](#schemarlistvposshopproductordervo)|

<a id="opIdremove"></a>

## DELETE 删除店铺产品订单

DELETE /restful/v1/vpos/shopProductOrder/{ids}

删除店铺产品订单

### 请求参数

|名称|位置|类型|必选|说明|
|---|---|---|---|---|
|ids|path|array[integer]| 是 |主键串|

> 返回示例

> 200 Response

```
{"code":0,"msg":"string","data":{}}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[RVoid](#schemarvoid)|

# V1/顾客信息

<a id="opIdedit_1"></a>

## PUT 修改顾客信息

PUT /restful/v1/vpos/customer

修改顾客信息

> Body 请求参数

```json
{
  "id": 0,
  "name": "string",
  "phoneNumber": "string",
  "address": "string",
  "email": "string",
  "languagePref": "string",
  "remark": "string",
  "creditRating": 0
}
```

### 请求参数

|名称|位置|类型|必选|说明|
|---|---|---|---|---|
|body|body|[VposCustomerBo](#schemavposcustomerbo)| 否 |none|

> 返回示例

> 200 Response

```
{"code":0,"msg":"string","data":{}}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[RVoid](#schemarvoid)|

<a id="opIdadd_1"></a>

## POST 新增顾客信息

POST /restful/v1/vpos/customer

新增顾客信息

> Body 请求参数

```json
{
  "id": 0,
  "name": "string",
  "phoneNumber": "string",
  "address": "string",
  "email": "string",
  "languagePref": "string",
  "remark": "string",
  "creditRating": 0
}
```

### 请求参数

|名称|位置|类型|必选|说明|
|---|---|---|---|---|
|body|body|[VposCustomerBo](#schemavposcustomerbo)| 否 |none|

> 返回示例

> 200 Response

```
{"code":0,"msg":"string","data":{}}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[RVoid](#schemarvoid)|

<a id="opIdgetInfo_4"></a>

## GET 获取顾客信息详细信息

GET /restful/v1/vpos/customer/{id}

获取顾客信息详细信息

### 请求参数

|名称|位置|类型|必选|说明|
|---|---|---|---|---|
|id|path|integer(int64)| 是 |主键|

> 返回示例

> 200 Response

```
{"code":0,"msg":"string","data":{"id":0,"name":"string","phoneNumber":"string","address":"string","email":"string","languagePref":"string","createTime":"2019-08-24T14:15:22Z","updateTime":"2019-08-24T14:15:22Z","remark":"string","creditRating":0}}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[RVposCustomerVo](#schemarvposcustomervo)|

<a id="opIdlistTodayOrders"></a>

## GET Caller档案 当日所有订单

GET /restful/v1/vpos/customer/listTodayOrders/{id}

Caller档案 当日所有订单

### 请求参数

|名称|位置|类型|必选|说明|
|---|---|---|---|---|
|id|path|integer(int64)| 是 |顾客id|

> 返回示例

> 200 Response

```
{"code":0,"msg":"string","data":[{"id":0,"orderNo":"string","customerPhone":"string","customerName":"string","status":"string","estimatedWaitTime":0,"notes":"string","type":"string","subtotal":0,"discount":0,"tax":0,"billTotal":0,"paidAmount":0,"paymentStatus":"string","paymentMethod":"string","paymentInfo":"string","shopId":0,"customerId":0,"shopName":"string","completedAt":"2019-08-24T14:15:22Z","createTime":"2019-08-24T14:15:22Z","updateTime":"2019-08-24T14:15:22Z","remark":"string","details":[{}],"orders":[{"id":0,"orderNo":"string","customerPhone":"string","customerName":"string","status":"string","estimatedWaitTime":0,"notes":"string","type":"string","subtotal":0,"discount":0,"tax":0,"billTotal":0,"paidAmount":0,"paymentStatus":"string","paymentMethod":"string","paymentInfo":"string","shopId":0,"customerId":0,"shopName":"string","completedAt":"2019-08-24T14:15:22Z","createTime":"2019-08-24T14:15:22Z","updateTime":"2019-08-24T14:15:22Z","remark":"string","details":[{}],"orders":[{}],"ips":["string"]}],"ips":["string"]}]}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[RListVposShopProductOrderVo](#schemarlistvposshopproductordervo)|

<a id="opIdlistMost5OrderProduct"></a>

## GET Caller档案 此人5个最多选择的菜品

GET /restful/v1/vpos/customer/listMost5OrderProduct/{id}

Caller档案 此人5个最多选择的菜品

### 请求参数

|名称|位置|类型|必选|说明|
|---|---|---|---|---|
|id|path|integer(int64)| 是 |顾客id|

> 返回示例

> 200 Response

```
{"code":0,"msg":"string","data":[{"id":0,"code":"string","name":"string","options":"string","prices":"string","category":"string","categoryId":0,"shopId":0,"description":"string","ingredients":"string","allergens":"string","sauce":"string","image":"string","recommended":"string","promo":"string","promoDiscount":0,"status":"string","createTime":"2019-08-24T14:15:22Z","updateTime":"2019-08-24T14:15:22Z","remark":"string","totalQuantity":0}]}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[RListVposShopProductVo](#schemarlistvposshopproductvo)|

<a id="opIdlistLast5Orders"></a>

## GET Caller档案 最近5次订单

GET /restful/v1/vpos/customer/listLast5Orders/{id}

Caller档案 最近5次订单

### 请求参数

|名称|位置|类型|必选|说明|
|---|---|---|---|---|
|id|path|integer(int64)| 是 |顾客id|

> 返回示例

> 200 Response

```
{"code":0,"msg":"string","data":[{"id":0,"orderNo":"string","customerPhone":"string","customerName":"string","status":"string","estimatedWaitTime":0,"notes":"string","type":"string","subtotal":0,"discount":0,"tax":0,"billTotal":0,"paidAmount":0,"paymentStatus":"string","paymentMethod":"string","paymentInfo":"string","shopId":0,"customerId":0,"shopName":"string","completedAt":"2019-08-24T14:15:22Z","createTime":"2019-08-24T14:15:22Z","updateTime":"2019-08-24T14:15:22Z","remark":"string","details":[{}],"orders":[{"id":0,"orderNo":"string","customerPhone":"string","customerName":"string","status":"string","estimatedWaitTime":0,"notes":"string","type":"string","subtotal":0,"discount":0,"tax":0,"billTotal":0,"paidAmount":0,"paymentStatus":"string","paymentMethod":"string","paymentInfo":"string","shopId":0,"customerId":0,"shopName":"string","completedAt":"2019-08-24T14:15:22Z","createTime":"2019-08-24T14:15:22Z","updateTime":"2019-08-24T14:15:22Z","remark":"string","details":[{}],"orders":[{}],"ips":["string"]}],"ips":["string"]}]}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[RListVposShopProductOrderVo](#schemarlistvposshopproductordervo)|

<a id="opIdremove_1"></a>

## DELETE 删除顾客信息

DELETE /restful/v1/vpos/customer/{ids}

删除顾客信息

### 请求参数

|名称|位置|类型|必选|说明|
|---|---|---|---|---|
|ids|path|array[integer]| 是 |主键串|

> 返回示例

> 200 Response

```
{"code":0,"msg":"string","data":{}}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[RVoid](#schemarvoid)|

# V1/通话记录

<a id="opIdedit_2"></a>

## PUT 修改通话记录

PUT /restful/v1/vpos/callHistory

修改通话记录

> Body 请求参数

```json
{
  "id": 0,
  "phoneNumber": "string",
  "customerName": "string",
  "callTime": 0,
  "transcript": "string",
  "summary": "string",
  "intentTags": "string",
  "orderId": 0,
  "customerId": 0,
  "shopId": 0,
  "voiceAgent": "string",
  "remark": "string"
}
```

### 请求参数

|名称|位置|类型|必选|说明|
|---|---|---|---|---|
|body|body|[VposCallHistoryBo](#schemavposcallhistorybo)| 否 |none|

> 返回示例

> 200 Response

```
{"code":0,"msg":"string","data":{}}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[RVoid](#schemarvoid)|

<a id="opIdadd_2"></a>

## POST 新增通话记录

POST /restful/v1/vpos/callHistory

新增通话记录

> Body 请求参数

```json
{
  "id": 0,
  "phoneNumber": "string",
  "customerName": "string",
  "callTime": 0,
  "transcript": "string",
  "summary": "string",
  "intentTags": "string",
  "orderId": 0,
  "customerId": 0,
  "shopId": 0,
  "voiceAgent": "string",
  "remark": "string"
}
```

### 请求参数

|名称|位置|类型|必选|说明|
|---|---|---|---|---|
|body|body|[VposCallHistoryBo](#schemavposcallhistorybo)| 否 |none|

> 返回示例

> 200 Response

```
{"code":0,"msg":"string","data":{}}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[RVoid](#schemarvoid)|

<a id="opIdgetInfo_5"></a>

## GET 获取通话记录详细信息

GET /restful/v1/vpos/callHistory/{id}

获取通话记录详细信息

### 请求参数

|名称|位置|类型|必选|说明|
|---|---|---|---|---|
|id|path|integer(int64)| 是 |主键|

> 返回示例

> 200 Response

```
{"code":0,"msg":"string","data":{"id":0,"phoneNumber":"string","customerName":"string","callTime":0,"transcript":"string","summary":"string","intentTags":"string","orderId":0,"customerId":0,"shopId":0,"voiceAgent":"string","createTime":"2019-08-24T14:15:22Z","updateTime":"2019-08-24T14:15:22Z","remark":"string"}}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[RVposCallHistoryVo](#schemarvposcallhistoryvo)|

<a id="opIdlist_2"></a>

## GET 查询通话记录列表

GET /restful/v1/vpos/callHistory/list

查询通话记录列表

### 请求参数

|名称|位置|类型|必选|说明|
|---|---|---|---|---|
|params|query|object| 否 |请求参数|
|pageNum|query|integer(int32)| 是 |页码|
|pageSize|query|integer(int32)| 是 |每页大小|
|id|query|integer(int64)| 否 |通话记录编号|
|phoneNumber|query|string| 否 |顾客号码|
|customerName|query|string| 否 |顾客姓名|
|transcript|query|string| 否 |通话内容|
|summary|query|string| 否 |简介对话摘要|
|intentTags|query|string| 否 |意图标签|
|orderId|query|integer(int64)| 否 |关联的订单|
|customerId|query|integer(int64)| 否 |关联客户id|
|shopId|query|integer(int64)| 否 |关联店铺id|
|voiceAgent|query|string| 否 |关联接听的|

> 返回示例

> 200 Response

```
{"code":0,"msg":"string","data":[{"id":0,"phoneNumber":"string","customerName":"string","callTime":0,"transcript":"string","summary":"string","intentTags":"string","orderId":0,"customerId":0,"shopId":0,"voiceAgent":"string","createTime":"2019-08-24T14:15:22Z","updateTime":"2019-08-24T14:15:22Z","remark":"string"}]}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[RListVposCallHistoryVo](#schemarlistvposcallhistoryvo)|

<a id="opIdremove_2"></a>

## DELETE 删除通话记录

DELETE /restful/v1/vpos/callHistory/{ids}

删除通话记录

### 请求参数

|名称|位置|类型|必选|说明|
|---|---|---|---|---|
|ids|path|array[integer]| 是 |主键串|

> 返回示例

> 200 Response

```
{"code":0,"msg":"string","data":{}}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[RVoid](#schemarvoid)|

# V1/店铺产品

<a id="opIdgetInfo_1"></a>

## GET 获取店铺产品详细信息

GET /restful/v1/vpos/shopProduct/{id}

获取店铺产品详细信息

### 请求参数

|名称|位置|类型|必选|说明|
|---|---|---|---|---|
|id|path|integer(int64)| 是 |主键|

> 返回示例

> 200 Response

```
{"code":0,"msg":"string","data":{"id":0,"code":"string","name":"string","options":"string","prices":"string","category":"string","categoryId":0,"shopId":0,"description":"string","ingredients":"string","allergens":"string","sauce":"string","image":"string","recommended":"string","promo":"string","promoDiscount":0,"status":"string","createTime":"2019-08-24T14:15:22Z","updateTime":"2019-08-24T14:15:22Z","remark":"string","totalQuantity":0}}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[RVposShopProductVo](#schemarvposshopproductvo)|

<a id="opIdlistInfo"></a>

## GET 获取整个过敏源，食材，调料清单

GET /restful/v1/vpos/shopProduct/listInfo

获取整个过敏源，食材，调料清单

### 请求参数

|名称|位置|类型|必选|说明|
|---|---|---|---|---|
|shopId|query|object| 是 |所属店铺编号|

> 返回示例

> 200 Response

```
{"code":0,"msg":"string","data":{"id":0,"code":"string","name":"string","options":"string","prices":"string","category":"string","categoryId":0,"shopId":0,"description":"string","ingredients":"string","allergens":"string","sauce":"string","image":"string","recommended":"string","promo":"string","promoDiscount":0,"status":"string","createTime":"2019-08-24T14:15:22Z","updateTime":"2019-08-24T14:15:22Z","remark":"string","totalQuantity":0}}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[RVposShopProductVo](#schemarvposshopproductvo)|

<a id="opIdlist_1"></a>

## GET 获取整个菜单

GET /restful/v1/vpos/shopProduct/list

获取整个菜单

### 请求参数

|名称|位置|类型|必选|说明|
|---|---|---|---|---|
|shopId|query|object| 是 |所属店铺编号|

> 返回示例

> 200 Response

```
{"code":0,"msg":"string","data":[{"id":0,"code":"string","name":"string","options":"string","prices":"string","category":"string","categoryId":0,"shopId":0,"description":"string","ingredients":"string","allergens":"string","sauce":"string","image":"string","recommended":"string","promo":"string","promoDiscount":0,"status":"string","createTime":"2019-08-24T14:15:22Z","updateTime":"2019-08-24T14:15:22Z","remark":"string","totalQuantity":0}]}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[RListVposShopProductVo](#schemarlistvposshopproductvo)|

<a id="opIdgetInfo_2"></a>

## GET 获取指定菜的过敏原_食材_调味品

GET /restful/v1/vpos/shopProduct/info/{ids}

获取指定菜的过敏原_食材_调味品

### 请求参数

|名称|位置|类型|必选|说明|
|---|---|---|---|---|
|ids|path|array[integer]| 是 |none|

> 返回示例

> 200 Response

```
{"code":0,"msg":"string","data":[{"id":0,"code":"string","name":"string","options":"string","prices":"string","categoryId":0,"shopId":0,"description":"string","ingredients":"string","allergens":"string","sauce":"string","image":"string","recommended":"string","promo":"string","promoDiscount":0,"status":"string","delFlag":"string","createDept":0,"createBy":0,"createTime":"2019-08-24T14:15:22Z","updateBy":0,"updateTime":"2019-08-24T14:15:22Z","tenantId":"string","remark":"string"}]}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[RListVposShopProduct](#schemarlistvposshopproduct)|

# V1/店铺

<a id="opIdgetInfo_3"></a>

## GET 获取店铺详细信息

GET /restful/v1/vpos/shop/{id}

获取店铺详细信息

### 请求参数

|名称|位置|类型|必选|说明|
|---|---|---|---|---|
|id|path|integer(int64)| 是 |主键|

> 返回示例

> 200 Response

```
{"code":0,"msg":"string","data":{"id":0,"code":"string","name":"string","address":"string","phoneNumber":"string","twilioNumber":"string","email":"string","cuisineType":"string","languagesSupported":"string","businessHours":"string","transferNumber":"string","description":"string","type":"string","status":"string","createTime":"2019-08-24T14:15:22Z","updateTime":"2019-08-24T14:15:22Z","remark":"string","preparingTime":0,"special":"string"}}
```

### 返回结果

|状态码|状态码含义|说明|数据模型|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|OK|[RVposShopVo](#schemarvposshopvo)|

# 数据模型

<h2 id="tocS_VposShopProductOrderBo">VposShopProductOrderBo</h2>

<a id="schemavposshopproductorderbo"></a>
<a id="schema_VposShopProductOrderBo"></a>
<a id="tocSvposshopproductorderbo"></a>
<a id="tocsvposshopproductorderbo"></a>

```json
{
  "id": 0,
  "customerPhone": "string",
  "customerName": "string",
  "status": "string",
  "estimatedWaitTime": 0,
  "notes": "string",
  "type": "string",
  "subtotal": 0,
  "details": [
    {
      "id": 0,
      "shopId": 0,
      "productId": 0,
      "orderId": 0,
      "price": "string",
      "quantity": 0,
      "totalAmount": 0,
      "options": "string",
      "productJson": "string",
      "status": "string",
      "remark": "string"
    }
  ],
  "discount": 0,
  "tax": 0,
  "billTotal": 0,
  "paidAmount": 0,
  "paymentStatus": "string",
  "paymentMethod": "string",
  "paymentInfo": "string",
  "shopId": 0,
  "customerId": 0,
  "completedAt": "2019-08-24T14:15:22Z",
  "remark": "string",
  "bookTime": "2019-08-24T14:15:22Z"
}

```

店铺菜品订单业务对象 vpos_shop_product_order

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|id|integer(int64)|true|none||订单编号|
|customerPhone|string|true|none||订购人电话|
|customerName|string|true|none||订购人姓名|
|status|string|true|none||订单状态|
|estimatedWaitTime|integer(int64)|false|none||等待时间|
|notes|string|false|none||客户备注|
|type|string|true|none||订单类型|
|subtotal|number|true|none||总价|
|details|[[VposShopProductOrderDetailBo](#schemavposshopproductorderdetailbo)]|false|none||订单明细|
|discount|number|false|none||折扣|
|tax|number|true|none||税费|
|billTotal|number|true|none||应付金额|
|paidAmount|number|false|none||实付金额|
|paymentStatus|string|true|none||支付状态|
|paymentMethod|string|true|none||支付方式|
|paymentInfo|string|false|none||支付信息|
|shopId|integer(int64)|true|none||所属店铺编号|
|customerId|integer(int64)|false|none||客户编号|
|completedAt|string(date-time)|false|none||完成时间|
|remark|string|false|none||备注|
|bookTime|string(date-time)|false|none||预约时间|

<h2 id="tocS_VposShopProductOrderDetailBo">VposShopProductOrderDetailBo</h2>

<a id="schemavposshopproductorderdetailbo"></a>
<a id="schema_VposShopProductOrderDetailBo"></a>
<a id="tocSvposshopproductorderdetailbo"></a>
<a id="tocsvposshopproductorderdetailbo"></a>

```json
{
  "id": 0,
  "shopId": 0,
  "productId": 0,
  "orderId": 0,
  "price": "string",
  "quantity": 0,
  "totalAmount": 0,
  "options": "string",
  "productJson": "string",
  "status": "string",
  "remark": "string"
}

```

店铺菜品订单详情业务对象 vpos_shop_product_order_detail

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|id|integer(int64)|true|none||编号|
|shopId|integer(int64)|true|none||店铺编号|
|productId|integer(int64)|true|none||店铺菜品编号|
|orderId|integer(int64)|true|none||订单编号|
|price|string|true|none||价格|
|quantity|integer(int32)|true|none||数量|
|totalAmount|number|true|none||合计|
|options|string|false|none||选项|
|productJson|string|false|none||下单时菜品的json快照|
|status|string|true|none||状态|
|remark|string|false|none||备注|

<h2 id="tocS_RVoid">RVoid</h2>

<a id="schemarvoid"></a>
<a id="schema_RVoid"></a>
<a id="tocSrvoid"></a>
<a id="tocsrvoid"></a>

```json
{
  "code": 0,
  "msg": "string",
  "data": {}
}

```

响应信息主体

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|code|integer(int32)|false|none||none|
|msg|string|false|none||none|
|data|object|false|none||none|

<h2 id="tocS_RVposShopProductOrderVo">RVposShopProductOrderVo</h2>

<a id="schemarvposshopproductordervo"></a>
<a id="schema_RVposShopProductOrderVo"></a>
<a id="tocSrvposshopproductordervo"></a>
<a id="tocsrvposshopproductordervo"></a>

```json
{
  "code": 0,
  "msg": "string",
  "data": {
    "id": 0,
    "orderNo": "string",
    "customerPhone": "string",
    "customerName": "string",
    "status": "string",
    "estimatedWaitTime": 0,
    "notes": "string",
    "type": "string",
    "subtotal": 0,
    "discount": 0,
    "tax": 0,
    "billTotal": 0,
    "paidAmount": 0,
    "paymentStatus": "string",
    "paymentMethod": "string",
    "paymentInfo": "string",
    "shopId": 0,
    "customerId": 0,
    "shopName": "string",
    "completedAt": "2019-08-24T14:15:22Z",
    "createTime": "2019-08-24T14:15:22Z",
    "updateTime": "2019-08-24T14:15:22Z",
    "remark": "string",
    "details": [
      {}
    ],
    "orders": [
      {
        "id": 0,
        "orderNo": "string",
        "customerPhone": "string",
        "customerName": "string",
        "status": "string",
        "estimatedWaitTime": 0,
        "notes": "string",
        "type": "string",
        "subtotal": 0,
        "discount": 0,
        "tax": 0,
        "billTotal": 0,
        "paidAmount": 0,
        "paymentStatus": "string",
        "paymentMethod": "string",
        "paymentInfo": "string",
        "shopId": 0,
        "customerId": 0,
        "shopName": "string",
        "completedAt": "2019-08-24T14:15:22Z",
        "createTime": "2019-08-24T14:15:22Z",
        "updateTime": "2019-08-24T14:15:22Z",
        "remark": "string",
        "details": [
          {}
        ],
        "orders": [
          {
            "id": null,
            "orderNo": null,
            "customerPhone": null,
            "customerName": null,
            "status": null,
            "estimatedWaitTime": null,
            "notes": null,
            "type": null,
            "subtotal": null,
            "discount": null,
            "tax": null,
            "billTotal": null,
            "paidAmount": null,
            "paymentStatus": null,
            "paymentMethod": null,
            "paymentInfo": null,
            "shopId": null,
            "customerId": null,
            "shopName": null,
            "completedAt": null,
            "createTime": null,
            "updateTime": null,
            "remark": null,
            "details": null,
            "orders": null,
            "ips": null
          }
        ],
        "ips": [
          "string"
        ]
      }
    ],
    "ips": [
      "string"
    ]
  }
}

```

响应信息主体

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|code|integer(int32)|false|none||none|
|msg|string|false|none||none|
|data|[VposShopProductOrderVo](#schemavposshopproductordervo)|false|none||店铺菜品订单视图对象 vpos_shop_product_order|

<h2 id="tocS_VposShopProductOrderVo">VposShopProductOrderVo</h2>

<a id="schemavposshopproductordervo"></a>
<a id="schema_VposShopProductOrderVo"></a>
<a id="tocSvposshopproductordervo"></a>
<a id="tocsvposshopproductordervo"></a>

```json
{
  "id": 0,
  "orderNo": "string",
  "customerPhone": "string",
  "customerName": "string",
  "status": "string",
  "estimatedWaitTime": 0,
  "notes": "string",
  "type": "string",
  "subtotal": 0,
  "discount": 0,
  "tax": 0,
  "billTotal": 0,
  "paidAmount": 0,
  "paymentStatus": "string",
  "paymentMethod": "string",
  "paymentInfo": "string",
  "shopId": 0,
  "customerId": 0,
  "shopName": "string",
  "completedAt": "2019-08-24T14:15:22Z",
  "createTime": "2019-08-24T14:15:22Z",
  "updateTime": "2019-08-24T14:15:22Z",
  "remark": "string",
  "details": [
    {}
  ],
  "orders": [
    {
      "id": 0,
      "orderNo": "string",
      "customerPhone": "string",
      "customerName": "string",
      "status": "string",
      "estimatedWaitTime": 0,
      "notes": "string",
      "type": "string",
      "subtotal": 0,
      "discount": 0,
      "tax": 0,
      "billTotal": 0,
      "paidAmount": 0,
      "paymentStatus": "string",
      "paymentMethod": "string",
      "paymentInfo": "string",
      "shopId": 0,
      "customerId": 0,
      "shopName": "string",
      "completedAt": "2019-08-24T14:15:22Z",
      "createTime": "2019-08-24T14:15:22Z",
      "updateTime": "2019-08-24T14:15:22Z",
      "remark": "string",
      "details": [
        {}
      ],
      "orders": [
        {
          "id": 0,
          "orderNo": "string",
          "customerPhone": "string",
          "customerName": "string",
          "status": "string",
          "estimatedWaitTime": 0,
          "notes": "string",
          "type": "string",
          "subtotal": 0,
          "discount": 0,
          "tax": 0,
          "billTotal": 0,
          "paidAmount": 0,
          "paymentStatus": "string",
          "paymentMethod": "string",
          "paymentInfo": "string",
          "shopId": 0,
          "customerId": 0,
          "shopName": "string",
          "completedAt": "2019-08-24T14:15:22Z",
          "createTime": "2019-08-24T14:15:22Z",
          "updateTime": "2019-08-24T14:15:22Z",
          "remark": "string",
          "details": [
            {}
          ],
          "orders": [
            {}
          ],
          "ips": [
            "string"
          ]
        }
      ],
      "ips": [
        "string"
      ]
    }
  ],
  "ips": [
    "string"
  ]
}

```

店铺菜品订单视图对象 vpos_shop_product_order

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|id|integer(int64)|false|none||订单编号|
|orderNo|string|false|none||订单号|
|customerPhone|string|false|none||订购人电话|
|customerName|string|false|none||订购人姓名|
|status|string|false|none||订单状态|
|estimatedWaitTime|integer(int64)|false|none||等待时间|
|notes|string|false|none||客户备注|
|type|string|false|none||订单类型|
|subtotal|number|false|none||总价|
|discount|number|false|none||折扣|
|tax|number|false|none||税费|
|billTotal|number|false|none||应付金额|
|paidAmount|number|false|none||实付金额|
|paymentStatus|string|false|none||支付状态|
|paymentMethod|string|false|none||支付方式|
|paymentInfo|string|false|none||支付信息|
|shopId|integer(int64)|false|none||所属店铺编号|
|customerId|integer(int64)|false|none||客户编号|
|shopName|string|false|none||none|
|completedAt|string(date-time)|false|none||完成时间|
|createTime|string(date-time)|false|none||创建时间|
|updateTime|string(date-time)|false|none||更新时间|
|remark|string|false|none||备注|
|details|[object]|false|none||none|
|orders|[[VposShopProductOrderVo](#schemavposshopproductordervo)]|false|none||[店铺菜品订单视图对象 vpos_shop_product_order]|
|ips|[string]|false|none||none|

<h2 id="tocS_VposShopProductOrderDetailVo">VposShopProductOrderDetailVo</h2>

<a id="schemavposshopproductorderdetailvo"></a>
<a id="schema_VposShopProductOrderDetailVo"></a>
<a id="tocSvposshopproductorderdetailvo"></a>
<a id="tocsvposshopproductorderdetailvo"></a>

```json
{
  "id": 0,
  "shopId": 0,
  "productId": 0,
  "productName": "string",
  "orderId": 0,
  "price": "string",
  "quantity": 0,
  "totalAmount": 0,
  "options": "string",
  "productJson": "string",
  "status": "string",
  "createTime": "2019-08-24T14:15:22Z",
  "updateTime": "2019-08-24T14:15:22Z",
  "remark": "string",
  "bookTime": "2019-08-24T14:15:22Z"
}

```

店铺菜品订单详情视图对象 vpos_shop_product_order_detail

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|id|integer(int64)|false|none||编号|
|shopId|integer(int64)|false|none||店铺编号|
|productId|integer(int64)|false|none||店铺菜品编号|
|productName|string|false|none||none|
|orderId|integer(int64)|false|none||订单编号|
|price|string|false|none||价格|
|quantity|integer(int32)|false|none||数量|
|totalAmount|number|false|none||合计|
|options|string|false|none||选项|
|productJson|string|false|none||下单时菜品的json快照|
|status|string|false|none||状态|
|createTime|string(date-time)|false|none||创建时间|
|updateTime|string(date-time)|false|none||更新时间|
|remark|string|false|none||备注|
|bookTime|string(date-time)|false|none||预约时间|

<h2 id="tocS_RVposShopProductVo">RVposShopProductVo</h2>

<a id="schemarvposshopproductvo"></a>
<a id="schema_RVposShopProductVo"></a>
<a id="tocSrvposshopproductvo"></a>
<a id="tocsrvposshopproductvo"></a>

```json
{
  "code": 0,
  "msg": "string",
  "data": {
    "id": 0,
    "code": "string",
    "name": "string",
    "options": "string",
    "prices": "string",
    "category": "string",
    "categoryId": 0,
    "shopId": 0,
    "description": "string",
    "ingredients": "string",
    "allergens": "string",
    "sauce": "string",
    "image": "string",
    "recommended": "string",
    "promo": "string",
    "promoDiscount": 0,
    "status": "string",
    "createTime": "2019-08-24T14:15:22Z",
    "updateTime": "2019-08-24T14:15:22Z",
    "remark": "string",
    "totalQuantity": 0
  }
}

```

响应信息主体

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|code|integer(int32)|false|none||none|
|msg|string|false|none||none|
|data|[VposShopProductVo](#schemavposshopproductvo)|false|none||店铺菜品视图对象 vpos_shop_product|

<h2 id="tocS_VposShopProductVo">VposShopProductVo</h2>

<a id="schemavposshopproductvo"></a>
<a id="schema_VposShopProductVo"></a>
<a id="tocSvposshopproductvo"></a>
<a id="tocsvposshopproductvo"></a>

```json
{
  "id": 0,
  "code": "string",
  "name": "string",
  "options": "string",
  "prices": "string",
  "category": "string",
  "categoryId": 0,
  "shopId": 0,
  "description": "string",
  "ingredients": "string",
  "allergens": "string",
  "sauce": "string",
  "image": "string",
  "recommended": "string",
  "promo": "string",
  "promoDiscount": 0,
  "status": "string",
  "createTime": "2019-08-24T14:15:22Z",
  "updateTime": "2019-08-24T14:15:22Z",
  "remark": "string",
  "totalQuantity": 0
}

```

店铺菜品视图对象 vpos_shop_product

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|id|integer(int64)|false|none||菜品编号|
|code|string|false|none||菜品代码|
|name|string|false|none||菜品名称|
|options|string|false|none||可选项|
|prices|string|false|none||单价|
|category|string|false|none||菜品分类名称|
|categoryId|integer(int64)|false|none||菜品分类编号|
|shopId|integer(int64)|false|none||所属店铺编号|
|description|string|false|none||描述|
|ingredients|string|false|none||主要成分|
|allergens|string|false|none||过敏源|
|sauce|string|false|none||调味品|
|image|string|false|none||图片|
|recommended|string|false|none||是否推荐|
|promo|string|false|none||是否活动|
|promoDiscount|number|false|none||活动折扣|
|status|string|false|none||状态|
|createTime|string(date-time)|false|none||创建时间|
|updateTime|string(date-time)|false|none||更新时间|
|remark|string|false|none||备注|
|totalQuantity|integer(int64)|false|none||none|

<h2 id="tocS_RVposShopVo">RVposShopVo</h2>

<a id="schemarvposshopvo"></a>
<a id="schema_RVposShopVo"></a>
<a id="tocSrvposshopvo"></a>
<a id="tocsrvposshopvo"></a>

```json
{
  "code": 0,
  "msg": "string",
  "data": {
    "id": 0,
    "code": "string",
    "name": "string",
    "address": "string",
    "phoneNumber": "string",
    "twilioNumber": "string",
    "email": "string",
    "cuisineType": "string",
    "languagesSupported": "string",
    "businessHours": "string",
    "transferNumber": "string",
    "description": "string",
    "type": "string",
    "status": "string",
    "createTime": "2019-08-24T14:15:22Z",
    "updateTime": "2019-08-24T14:15:22Z",
    "remark": "string",
    "preparingTime": 0,
    "special": "string"
  }
}

```

响应信息主体

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|code|integer(int32)|false|none||none|
|msg|string|false|none||none|
|data|[VposShopVo](#schemavposshopvo)|false|none||店铺视图对象 vpos_shop|

<h2 id="tocS_VposShopVo">VposShopVo</h2>

<a id="schemavposshopvo"></a>
<a id="schema_VposShopVo"></a>
<a id="tocSvposshopvo"></a>
<a id="tocsvposshopvo"></a>

```json
{
  "id": 0,
  "code": "string",
  "name": "string",
  "address": "string",
  "phoneNumber": "string",
  "twilioNumber": "string",
  "email": "string",
  "cuisineType": "string",
  "languagesSupported": "string",
  "businessHours": "string",
  "transferNumber": "string",
  "description": "string",
  "type": "string",
  "status": "string",
  "createTime": "2019-08-24T14:15:22Z",
  "updateTime": "2019-08-24T14:15:22Z",
  "remark": "string",
  "preparingTime": 0,
  "special": "string"
}

```

店铺视图对象 vpos_shop

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|id|integer(int64)|false|none||店铺编号|
|code|string|false|none||店铺代码|
|name|string|false|none||店铺名称|
|address|string|false|none||店铺地址|
|phoneNumber|string|false|none||电话号码|
|twilioNumber|string|false|none||Twilio号码|
|email|string|false|none||联系邮箱|
|cuisineType|string|false|none||菜系类型|
|languagesSupported|string|false|none||支持语言|
|businessHours|string|false|none||营业时间|
|transferNumber|string|false|none||人工客服电话|
|description|string|false|none||餐厅简介|
|type|string|false|none||店铺类型|
|status|string|false|none||店铺状态|
|createTime|string(date-time)|false|none||创建时间|
|updateTime|string(date-time)|false|none||更新时间|
|remark|string|false|none||备注|
|preparingTime|integer(int64)|false|none||等待时间|
|special|string|false|none||店铺特点|

<h2 id="tocS_VposCustomerBo">VposCustomerBo</h2>

<a id="schemavposcustomerbo"></a>
<a id="schema_VposCustomerBo"></a>
<a id="tocSvposcustomerbo"></a>
<a id="tocsvposcustomerbo"></a>

```json
{
  "id": 0,
  "name": "string",
  "phoneNumber": "string",
  "address": "string",
  "email": "string",
  "languagePref": "string",
  "remark": "string",
  "creditRating": 0
}

```

顾客信息业务对象 vpos_customer

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|id|integer(int64)|false|none||顾客编号|
|name|string|true|none||顾客姓名|
|phoneNumber|string|true|none||电话号码|
|address|string|false|none||外送地址|
|email|string|false|none||邮箱|
|languagePref|string|false|none||语言偏好|
|remark|string|false|none||备注|
|creditRating|integer(int64)|false|none||信用等级|

<h2 id="tocS_VposCallHistoryBo">VposCallHistoryBo</h2>

<a id="schemavposcallhistorybo"></a>
<a id="schema_VposCallHistoryBo"></a>
<a id="tocSvposcallhistorybo"></a>
<a id="tocsvposcallhistorybo"></a>

```json
{
  "id": 0,
  "phoneNumber": "string",
  "customerName": "string",
  "callTime": 0,
  "transcript": "string",
  "summary": "string",
  "intentTags": "string",
  "orderId": 0,
  "customerId": 0,
  "shopId": 0,
  "voiceAgent": "string",
  "remark": "string"
}

```

通话记录业务对象 vpos_call_history

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|id|integer(int64)|false|none||通话记录编号|
|phoneNumber|string|true|none||顾客号码|
|customerName|string|true|none||顾客姓名|
|callTime|integer(int64)|true|none||通话时长|
|transcript|string|true|none||通话内容|
|summary|string|true|none||简介对话摘要|
|intentTags|string|false|none||意图标签|
|orderId|integer(int64)|false|none||关联的订单|
|customerId|integer(int64)|false|none||关联客户id|
|shopId|integer(int64)|false|none||关联店铺id|
|voiceAgent|string|false|none||关联接听的|
|remark|string|false|none||备注|

<h2 id="tocS_RVposCustomerVo">RVposCustomerVo</h2>

<a id="schemarvposcustomervo"></a>
<a id="schema_RVposCustomerVo"></a>
<a id="tocSrvposcustomervo"></a>
<a id="tocsrvposcustomervo"></a>

```json
{
  "code": 0,
  "msg": "string",
  "data": {
    "id": 0,
    "name": "string",
    "phoneNumber": "string",
    "address": "string",
    "email": "string",
    "languagePref": "string",
    "createTime": "2019-08-24T14:15:22Z",
    "updateTime": "2019-08-24T14:15:22Z",
    "remark": "string",
    "creditRating": 0
  }
}

```

响应信息主体

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|code|integer(int32)|false|none||none|
|msg|string|false|none||none|
|data|[VposCustomerVo](#schemavposcustomervo)|false|none||顾客信息视图对象 vpos_customer|

<h2 id="tocS_VposCustomerVo">VposCustomerVo</h2>

<a id="schemavposcustomervo"></a>
<a id="schema_VposCustomerVo"></a>
<a id="tocSvposcustomervo"></a>
<a id="tocsvposcustomervo"></a>

```json
{
  "id": 0,
  "name": "string",
  "phoneNumber": "string",
  "address": "string",
  "email": "string",
  "languagePref": "string",
  "createTime": "2019-08-24T14:15:22Z",
  "updateTime": "2019-08-24T14:15:22Z",
  "remark": "string",
  "creditRating": 0
}

```

顾客信息视图对象 vpos_customer

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|id|integer(int64)|false|none||顾客编号|
|name|string|false|none||顾客姓名|
|phoneNumber|string|false|none||电话号码|
|address|string|false|none||外送地址|
|email|string|false|none||邮箱|
|languagePref|string|false|none||语言偏好|
|createTime|string(date-time)|false|none||创建时间|
|updateTime|string(date-time)|false|none||更新时间|
|remark|string|false|none||备注|
|creditRating|integer(int64)|false|none||信用等级|

<h2 id="tocS_RVposCallHistoryVo">RVposCallHistoryVo</h2>

<a id="schemarvposcallhistoryvo"></a>
<a id="schema_RVposCallHistoryVo"></a>
<a id="tocSrvposcallhistoryvo"></a>
<a id="tocsrvposcallhistoryvo"></a>

```json
{
  "code": 0,
  "msg": "string",
  "data": {
    "id": 0,
    "phoneNumber": "string",
    "customerName": "string",
    "callTime": 0,
    "transcript": "string",
    "summary": "string",
    "intentTags": "string",
    "orderId": 0,
    "customerId": 0,
    "shopId": 0,
    "voiceAgent": "string",
    "createTime": "2019-08-24T14:15:22Z",
    "updateTime": "2019-08-24T14:15:22Z",
    "remark": "string"
  }
}

```

响应信息主体

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|code|integer(int32)|false|none||none|
|msg|string|false|none||none|
|data|[VposCallHistoryVo](#schemavposcallhistoryvo)|false|none||通话记录视图对象 vpos_call_history|

<h2 id="tocS_VposCallHistoryVo">VposCallHistoryVo</h2>

<a id="schemavposcallhistoryvo"></a>
<a id="schema_VposCallHistoryVo"></a>
<a id="tocSvposcallhistoryvo"></a>
<a id="tocsvposcallhistoryvo"></a>

```json
{
  "id": 0,
  "phoneNumber": "string",
  "customerName": "string",
  "callTime": 0,
  "transcript": "string",
  "summary": "string",
  "intentTags": "string",
  "orderId": 0,
  "customerId": 0,
  "shopId": 0,
  "voiceAgent": "string",
  "createTime": "2019-08-24T14:15:22Z",
  "updateTime": "2019-08-24T14:15:22Z",
  "remark": "string"
}

```

通话记录视图对象 vpos_call_history

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|id|integer(int64)|false|none||通话记录编号|
|phoneNumber|string|false|none||顾客号码|
|customerName|string|false|none||顾客姓名|
|callTime|integer(int64)|false|none||通话时长|
|transcript|string|false|none||通话内容|
|summary|string|false|none||简介对话摘要|
|intentTags|string|false|none||意图标签|
|orderId|integer(int64)|false|none||关联的订单|
|customerId|integer(int64)|false|none||关联客户id|
|shopId|integer(int64)|false|none||关联店铺id|
|voiceAgent|string|false|none||关联接听的|
|createTime|string(date-time)|false|none||创建时间|
|updateTime|string(date-time)|false|none||更新时间|
|remark|string|false|none||备注|

<h2 id="tocS_RListVposShopProductOrderVo">RListVposShopProductOrderVo</h2>

<a id="schemarlistvposshopproductordervo"></a>
<a id="schema_RListVposShopProductOrderVo"></a>
<a id="tocSrlistvposshopproductordervo"></a>
<a id="tocsrlistvposshopproductordervo"></a>

```json
{
  "code": 0,
  "msg": "string",
  "data": [
    {
      "id": 0,
      "orderNo": "string",
      "customerPhone": "string",
      "customerName": "string",
      "status": "string",
      "estimatedWaitTime": 0,
      "notes": "string",
      "type": "string",
      "subtotal": 0,
      "discount": 0,
      "tax": 0,
      "billTotal": 0,
      "paidAmount": 0,
      "paymentStatus": "string",
      "paymentMethod": "string",
      "paymentInfo": "string",
      "shopId": 0,
      "customerId": 0,
      "shopName": "string",
      "completedAt": "2019-08-24T14:15:22Z",
      "createTime": "2019-08-24T14:15:22Z",
      "updateTime": "2019-08-24T14:15:22Z",
      "remark": "string",
      "details": [
        {}
      ],
      "orders": [
        {
          "id": 0,
          "orderNo": "string",
          "customerPhone": "string",
          "customerName": "string",
          "status": "string",
          "estimatedWaitTime": 0,
          "notes": "string",
          "type": "string",
          "subtotal": 0,
          "discount": 0,
          "tax": 0,
          "billTotal": 0,
          "paidAmount": 0,
          "paymentStatus": "string",
          "paymentMethod": "string",
          "paymentInfo": "string",
          "shopId": 0,
          "customerId": 0,
          "shopName": "string",
          "completedAt": "2019-08-24T14:15:22Z",
          "createTime": "2019-08-24T14:15:22Z",
          "updateTime": "2019-08-24T14:15:22Z",
          "remark": "string",
          "details": [
            {}
          ],
          "orders": [
            {}
          ],
          "ips": [
            "string"
          ]
        }
      ],
      "ips": [
        "string"
      ]
    }
  ]
}

```

响应信息主体

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|code|integer(int32)|false|none||none|
|msg|string|false|none||none|
|data|[[VposShopProductOrderVo](#schemavposshopproductordervo)]|false|none||[店铺菜品订单视图对象 vpos_shop_product_order]|

<h2 id="tocS_RListVposShopProductVo">RListVposShopProductVo</h2>

<a id="schemarlistvposshopproductvo"></a>
<a id="schema_RListVposShopProductVo"></a>
<a id="tocSrlistvposshopproductvo"></a>
<a id="tocsrlistvposshopproductvo"></a>

```json
{
  "code": 0,
  "msg": "string",
  "data": [
    {
      "id": 0,
      "code": "string",
      "name": "string",
      "options": "string",
      "prices": "string",
      "category": "string",
      "categoryId": 0,
      "shopId": 0,
      "description": "string",
      "ingredients": "string",
      "allergens": "string",
      "sauce": "string",
      "image": "string",
      "recommended": "string",
      "promo": "string",
      "promoDiscount": 0,
      "status": "string",
      "createTime": "2019-08-24T14:15:22Z",
      "updateTime": "2019-08-24T14:15:22Z",
      "remark": "string",
      "totalQuantity": 0
    }
  ]
}

```

响应信息主体

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|code|integer(int32)|false|none||none|
|msg|string|false|none||none|
|data|[[VposShopProductVo](#schemavposshopproductvo)]|false|none||[店铺菜品视图对象 vpos_shop_product]|

<h2 id="tocS_RListVposShopProduct">RListVposShopProduct</h2>

<a id="schemarlistvposshopproduct"></a>
<a id="schema_RListVposShopProduct"></a>
<a id="tocSrlistvposshopproduct"></a>
<a id="tocsrlistvposshopproduct"></a>

```json
{
  "code": 0,
  "msg": "string",
  "data": [
    {
      "id": 0,
      "code": "string",
      "name": "string",
      "options": "string",
      "prices": "string",
      "categoryId": 0,
      "shopId": 0,
      "description": "string",
      "ingredients": "string",
      "allergens": "string",
      "sauce": "string",
      "image": "string",
      "recommended": "string",
      "promo": "string",
      "promoDiscount": 0,
      "status": "string",
      "delFlag": "string",
      "createDept": 0,
      "createBy": 0,
      "createTime": "2019-08-24T14:15:22Z",
      "updateBy": 0,
      "updateTime": "2019-08-24T14:15:22Z",
      "tenantId": "string",
      "remark": "string"
    }
  ]
}

```

响应信息主体

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|code|integer(int32)|false|none||none|
|msg|string|false|none||none|
|data|[[VposShopProduct](#schemavposshopproduct)]|false|none||[店铺菜品对象 vpos_shop_product]|

<h2 id="tocS_VposShopProduct">VposShopProduct</h2>

<a id="schemavposshopproduct"></a>
<a id="schema_VposShopProduct"></a>
<a id="tocSvposshopproduct"></a>
<a id="tocsvposshopproduct"></a>

```json
{
  "id": 0,
  "code": "string",
  "name": "string",
  "options": "string",
  "prices": "string",
  "categoryId": 0,
  "shopId": 0,
  "description": "string",
  "ingredients": "string",
  "allergens": "string",
  "sauce": "string",
  "image": "string",
  "recommended": "string",
  "promo": "string",
  "promoDiscount": 0,
  "status": "string",
  "delFlag": "string",
  "createDept": 0,
  "createBy": 0,
  "createTime": "2019-08-24T14:15:22Z",
  "updateBy": 0,
  "updateTime": "2019-08-24T14:15:22Z",
  "tenantId": "string",
  "remark": "string"
}

```

店铺菜品对象 vpos_shop_product

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|id|integer(int64)|false|none||菜品编号|
|code|string|false|none||菜品代码|
|name|string|false|none||菜品名称|
|options|string|false|none||可选项|
|prices|string|false|none||单价|
|categoryId|integer(int64)|false|none||菜品分类|
|shopId|integer(int64)|false|none||所属店铺编号|
|description|string|false|none||描述|
|ingredients|string|false|none||主要成分|
|allergens|string|false|none||过敏源|
|sauce|string|false|none||调味品|
|image|string|false|none||图片|
|recommended|string|false|none||是否推荐|
|promo|string|false|none||是否活动|
|promoDiscount|number|false|none||活动折扣|
|status|string|false|none||状态|
|delFlag|string|false|none||删除标志（0代表存在 1代表删除）|
|createDept|integer(int64)|false|none||创建部门|
|createBy|integer(int64)|false|none||创建者|
|createTime|string(date-time)|false|none||创建时间|
|updateBy|integer(int64)|false|none||更新者|
|updateTime|string(date-time)|false|none||更新时间|
|tenantId|string|false|none||租户编号|
|remark|string|false|none||备注|

<h2 id="tocS_RListVposCallHistoryVo">RListVposCallHistoryVo</h2>

<a id="schemarlistvposcallhistoryvo"></a>
<a id="schema_RListVposCallHistoryVo"></a>
<a id="tocSrlistvposcallhistoryvo"></a>
<a id="tocsrlistvposcallhistoryvo"></a>

```json
{
  "code": 0,
  "msg": "string",
  "data": [
    {
      "id": 0,
      "phoneNumber": "string",
      "customerName": "string",
      "callTime": 0,
      "transcript": "string",
      "summary": "string",
      "intentTags": "string",
      "orderId": 0,
      "customerId": 0,
      "shopId": 0,
      "voiceAgent": "string",
      "createTime": "2019-08-24T14:15:22Z",
      "updateTime": "2019-08-24T14:15:22Z",
      "remark": "string"
    }
  ]
}

```

响应信息主体

### 属性

|名称|类型|必选|约束|中文名|说明|
|---|---|---|---|---|---|
|code|integer(int32)|false|none||none|
|msg|string|false|none||none|
|data|[[VposCallHistoryVo](#schemavposcallhistoryvo)]|false|none||[通话记录视图对象 vpos_call_history]|

