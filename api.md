# 巨链财经 2.0

## 1.公共组件模块

### 1.1.banner 图列表

- 描述

  - 获取一级页面的 banner 图列表

- 请求 URL

  - `api/v2/banner`

- 请求方式

  - `GET`

- 参数

| 参数名 | 必选 | 类型 | 说明 |
| ------ | ---- | ---- | ---- |
|        |      |      |      |

- 返回示例

```javascript
{
  "success": true,
  "message": "ok",
  "data": [
    {
      "id": 1,
      "image": "http://cdn.juliancj.com/1546423764400.jpg",
      "url": "http://cdn.juliancj.com/1546423764400.jpg",
    },
    // ...
  ]
}
```

- 返回参数说明

| 参数名  | 类型 | 说明                                      |
| ------- | ---- | ----------------------------------------- |
| success | boo  | true 为成功，false 为失败                 |
| message | str  | 返回说明（成功则是 ok，失败则是错误原因） |
| data    | arr  | banner 图列表                             |
|         |      |                                           |
| id      | num  | 图片 id                                   |
| image   | str  | 图片 url                                  |
| url     | str  | 图片跳转 url                              |

- 备注
  - 暂无

### 1.2.广告

- 描述

  - 根据类型获取广告图列表

- 请求 URL

  - `api/v2/adsPictures?type=1`

- 请求方式

  - `GET`

- 参数

| 参数名 | 必选 | 类型   | 说明                                                           |
| ------ | ---- | ------ | -------------------------------------------------------------- |
| type   | 是   | number | 广告类型（1 首页视频; 2 首页宣传; 3 首页活动; 4 其他页广告图） |

- 返回示例

```javascript
{
  "success": true,
  "message": "ok",
  "data": [
    {
      "id": 1,
      "image": "http://cdn.juliancj.com/1546423764400.jpg",
      "url": "http://cdn.juliancj.com/1546423764400.jpg",
      "status": 1,
      "statusText" : "活动已结束"
    },
    // ...
  ]
}
```

- 返回参数说明

| 参数名     | 类型 | 说明                                         |
| ---------- | ---- | -------------------------------------------- |
| id         | num  | 图片或视频 id                                |
| image      | str  | 图片 url 或视频 url                          |
| url        | str  | 图片跳转 url                                 |
| status     | str  | 活动状态（1 活动进行中; 2 活动结束; 3 下线） |
| statusText | str  | 状态文本                                     |

- 备注
  - 暂无

### 1.3.猜你喜欢-一周热文模块

- 描述

  - 根据类型获取模块展示列表

- 请求 URL

  - `api/v2/mayLike?type=1`

- 请求方式

  - `GET`

- 参数

| 参数名 | 必选 | 类型   | 说明                           |
| ------ | ---- | ------ | ------------------------------ |
| type   | 是   | number | 类型（1 猜你喜欢; 2 一周热文） |

- 返回示例

```javascript
{
  "success": true,
  "message": "ok",
  "data": [
    {
      "id": 1,
      "title": "以太坊2.0呼之欲出：八家团队做最后冲刺",
    },
    // ...
  ]
}
```

- 返回参数说明

| 参数名 | 类型 | 说明     |
| ------ | ---- | -------- |
| id     | num  | 文章 id  |
| title  | str  | 文章标题 |

- 备注
  - 暂无

### 1.4.分享排行模块(资讯文章？？？)

- 描述

  - 获取分享排行模块展示列表

- 请求 URL

  - `api/v2/sharingRanking?page=1&pagesize=10`

- 请求方式

  - `GET`

- 参数

| 参数名   | 必选 | 类型   | 说明     |
| -------- | ---- | ------ | -------- |
| page     | 是   | number | 第几页   |
| pagesize | 是   | number | 每页条数 |

- 返回示例

```javascript
{
  "success": true,
  "message": "ok",
  "data": [
    "total":123,
    "list":[
      {
        "id": 6593,
        "title": "区块链信息服务管理备案系统上线，矿池、钱包、白皮书皆需备案 | 火星号每日精选0128",
        "banner": "https://hx24.huoxing24.com/image/news/2019/01/28/1548682875508941.jpg",
        "introduction": "做区块链领域的头条号，因你因我，让信息更平等、更透明。",
        "pageView": 9400,
        "source": 2,
        "recommend": 1,
        "likeNumber": 3374,
        "collection": 3374,
        "status": 1,
        "createTime": 1548716431441,
        "updateTime": 1548725107492,
        "category": {
          "id": 1,
          "name": "新闻",
          "articles": null
        },
        "user": {
          "id": 80,
          "name": "巨链财经",
          "avatar": "http://cdn.juliancj.com/1545979231118.png",
          "sex": 1,
          "introduction": "最专业的媒体平台",
          "feature": "专业，精准传输区块链价值",
          "auth": 2,
          "grade": 1,
          "score": 0,
          "recommend": null,
          "status": 1,
          "articleCount": 1431,
          "pageViewSum": 26137722,
          "fensSum":1665,
          "isFollowed": null
        }
      },
      // ...
    ]
  ]

```

- 返回参数说明

| 参数名            | 类型 | 说明                                                                                             |
| ----------------- | ---- | ------------------------------------------------------------------------------------------------ |
| total             | num  | 文章总数                                                                                         |
| list              | ary  | 文章集合                                                                                         |
|                   |      |                                                                                                  |
| id                | num  | 文章 id                                                                                          |
| title             | str  | 文章标题                                                                                         |
| banner            | str  | 文章封面                                                                                         |
| introduction      | str  | 文章简介                                                                                         |
| pageView          | num  | 文章浏览量                                                                                       |
| source            | num  | 文章来源（1 原创; 2 转载）                                                                       |
| recommend         | num  | 文章推荐（0 不推荐; 1 推荐）                                                                     |
| likeNumber        | num  | 文章点赞量                                                                                       |
| collection        | num  | 文章收藏量                                                                                       |
| status            | num  | 文章状态（-3 下线; -2 审核未通过; -1 草稿; 0 待审核; 1 审核通过）                                |
| createTime        | num  | 创建时间                                                                                         |
| updateTime        | num  | 最后修改时间                                                                                     |
| category          | obj  | 文章分类信息                                                                                     |
| category.id       | num  | 文章分类 id                                                                                      |
| category.name     | str  | 文章分类名称                                                                                     |
| user              | obj  | 作者信息                                                                                         |
| user.id           | num  | 作者 id                                                                                          |
| user.name         | str  | 作者名称                                                                                         |
| user.avatar       | str  | 作者头像                                                                                         |
| user.sex          | num  | 作者性别（1 女性 ,2 男性）                                                                       |
| user.introduction | str  | 作者简介                                                                                         |
| user.feature      | str  | 作者特点                                                                                         |
| user.auth         | num  | 作者认证状态 （0 未认证,1 个人认证, 2 企业认证, -1 认证未通过, 3 申请个人认证, 4 申请企业认证 ） |
| user.grade        | num  | 作者等级（目前 1 - 39）                                                                          |
| user.score        | num  | 作者积分                                                                                         |
| user.recommend    | num  | 作者是否推荐（ 0 否，1 是）                                                                      |
| user.status       | num  | 作者状态（ -2 删除, -1 黑名单, 0 暂停使用, 1 可用）                                              |
| user.articleCount | num  | 作者文章数                                                                                       |
| user.pageViewSum  | num  | 作者浏览数                                                                                       |
| user.fensSum      | num  | 作者粉丝数                                                                                       |
| user.isFollowed   | boo  | 登录用户是否关注（true 已关注, false 未关注）                                                    |

- 备注
  - 暂无

### 1.5.热门标签

- 描述

  - 获取热门标签模块列表

- 请求 URL

  - `api/v2/popularTags`

- 请求方式

  - `GET`

- 参数

| 参数名 | 必选 | 类型 | 说明 |
| ------ | ---- | ---- | ---- |
|        |      |      |      |

- 返回示例

```javascript
{
  "success": true,
  "message": "ok",
  "data": ["财经","金融","专业","深度",...]
}
```

- 返回参数说明

| 参数名 | 类型 | 说明 |
| ------ | ---- | ---- |
|        |      |      |

- 备注

  - 暂无

## 2.行情（第三方来源）

### 2.1.支持的交易对信息

- 描述

  - 获取支持的交易对信息

- 请求 URL

  - `api/v2/symbols`

- 请求方式

  - `GET`

- 参数

| 参数名 | 必选 | 类型 | 说明 |
| ------ | ---- | ---- | ---- |
|        |      |      |      |

- 备注
  - 暂无

### 2.2.单个交易对的行情信息

- 描述

  - 获取单个交易对的行情信息(`COINSUPER:BTCUSD` 比特币; `COINSUPER:ETHBTC` 以太坊)

- 请求 URL

  - `api/v2/tick/ticker?unit=cny`

- 请求方式

  - `GET`

- 参数

| 参数名 | 必选 | 类型 | 说明                                                    |
| ------ | ---- | ---- | ------------------------------------------------------- |
| ticker | 是   | str  | 要查询的交易对（`COINSUPER:BTCUSD`;`COINSUPER:ETHBTC`） |
| unit   | 是   | str  | 货币种类（cny 人民币）                                  |

- 备注
  - 暂无

### 2.3.交易所下的交易对信息

- 描述

  - 获取交易所下的交易对信息

- 请求 URL

  - `api/v2/ticks/tick?unit=cny`

- 请求方式

  - `GET`

- 参数

| 参数名 | 必选 | 类型 | 说明                         |
| ------ | ---- | ---- | ---------------------------- |
| tick   | 是   | str  | 要查询的交易所（`BITFINEX`） |
| unit   | 是   | str  | 货币种类（cny 人民币）       |

- 备注
  - 暂无

### 2.4.交易对 K 线数据

- 描述

  - 获取指定交易对 K 线数据

- 请求 URL

  - `api/v2/klines/ticker/time`

- 请求方式

  - `GET`

- 参数

| 参数名 | 必选 | 类型 | 说明                                   |
| ------ | ---- | ---- | -------------------------------------- |
| ticker | 是   | str  | 要查询的交易对（如 `BITFINEX:BTCUSD`） |
| time   | 是   | str  | 查询周期（M1 一周; D1 一天。。。）     |

- 备注
  - 暂无

### 2.5.币值排行

- 描述

  - 获取币值排行前 100

- 请求 URL

  - `api/v2/currency/ranks`

- 请求方式

  - `GET`

- 参数

| 参数名 | 必选 | 类型 | 说明 |
| ------ | ---- | ---- | ---- |
|        |      |      |      |

- 备注
  - 暂无

## 3.资讯

### 3.1.资讯子类列表

- 描述

  - 根据分类 id 获取资讯下的的文章列表

- 请求 URL

  - `api/v2/category/type/article?page=1&pagesize=10`

- 请求方式

  - `GET`

- 参数

| 参数名   | 必选 | 类型   | 说明                                           |
| -------- | ---- | ------ | ---------------------------------------------- |
| type     | 是   | number | 类型（1 新闻; 2 深度; 3 技术; 4 投研; 5 人物） |
| page     | 是   | number | 第几页                                         |
| pagesize | 是   | number | 每页条数                                       |

- 返回示例

```javascript
{
  "success": true,
  "message": "ok",
  "data": {
    "total":426,
    "list":[
      {
        "id": 6400,
        "title": "币江南：1.28比特币行情解读之江南说年（一）",
        "banner": "http://cdn.juliancj.com/Fj79bTYiIF9EhOkhnrrkbjV7drJs",
        "introduction": "财富不应当是生命的目的，它只是生活的工具。挡不住今天的诱惑，就会失去明天的幸福!",
        "pageView": 3374,
        "source": 1,
        "recommend": 1,
        "likeNumber": 3374,
        "collection": 3374,
        "status": 1,
        "createTime": 1548647116433,
        "updateTime": 1548647116433,
        "category": {
          "id": 2,
          "name": "深度",
          "articles": null
        },
        "user": {
          "id": 80,
          "name": "巨链财经",
          "avatar": "http://cdn.juliancj.com/1545979231118.png",
          "sex": 1,
          "introduction": "最专业的媒体平台",
          "feature": "专业，精准传输区块链价值",
          "auth": 2,
          "grade": 1,
          "score": 0,
          "recommend": null,
          "status": 1,
          "articleCount": 1431,
          "pageViewSum": 26137722,
          "fensSum":1665,
          "isFollowed": null
        }
      },
      // ...
    ]
  }
}
```

- 返回参数说明

| 参数名            | 类型 | 说明                                                                                             |
| ----------------- | ---- | ------------------------------------------------------------------------------------------------ |
| total             | num  | 文章总数                                                                                         |
| list              | ary  | 文章集合                                                                                         |
|                   |      |                                                                                                  |
| id                | num  | 文章 id                                                                                          |
| title             | str  | 文章标题                                                                                         |
| banner            | str  | 文章封面                                                                                         |
| introduction      | str  | 文章简介                                                                                         |
| pageView          | num  | 文章浏览量                                                                                       |
| source            | num  | 文章来源（1 原创; 2 转载）                                                                       |
| recommend         | num  | 文章推荐（0 不推荐; 1 推荐）                                                                     |
| likeNumber        | num  | 文章点赞量                                                                                       |
| collection        | num  | 文章收藏量                                                                                       |
| status            | num  | 文章状态（-3 下线; -2 审核未通过; -1 草稿; 0 待审核; 1 审核通过）                                |
| createTime        | num  | 创建时间                                                                                         |
| updateTime        | num  | 最后修改时间                                                                                     |
| category          | obj  | 文章分类信息                                                                                     |
| category.id       | num  | 文章分类 id                                                                                      |
| category.name     | str  | 文章分类名称                                                                                     |
| user              | obj  | 作者信息                                                                                         |
| user.id           | num  | 作者 id                                                                                          |
| user.name         | str  | 作者名称                                                                                         |
| user.avatar       | str  | 作者头像                                                                                         |
| user.sex          | num  | 作者性别（1 女性 ,2 男性）                                                                       |
| user.introduction | str  | 作者简介                                                                                         |
| user.feature      | str  | 作者特点                                                                                         |
| user.auth         | num  | 作者认证状态 （0 未认证,1 个人认证, 2 企业认证, -1 认证未通过, 3 申请个人认证, 4 申请企业认证 ） |
| user.grade        | num  | 作者等级（目前 1 - 39）                                                                          |
| user.score        | num  | 作者积分                                                                                         |
| user.recommend    | num  | 作者是否推荐（ 0 否，1 是）                                                                      |
| user.status       | num  | 作者状态（ -2 删除, -1 黑名单, 0 暂停使用, 1 可用）                                              |
| user.articleCount | num  | 作者文章数                                                                                       |
| user.pageViewSum  | num  | 作者浏览数                                                                                       |
| user.fensSum      | num  | 作者粉丝数                                                                                       |
| user.isFollowed   | boo  | 登录用户是否关注（true 已关注, false 未关注）                                                    |

- 备注
  - 暂无

### 3.2.资讯推荐和热门

- 描述

  - 根据分类 id 获取资讯下的的文章列表

- 请求 URL

  - `api/v2/information/type/article?page=1&pagesize=10`

- 请求方式

  - `GET`

- 参数

| 参数名   | 必选 | 类型   | 说明                   |
| -------- | ---- | ------ | ---------------------- |
| type     | 是   | number | 类型（1 推荐; 2 热门） |
| page     | 是   | number | 第几页                 |
| pagesize | 是   | number | 每页条数               |

- 返回示例

```javascript
{
  "success": true,
  "message": "ok",
  "data": {
    "total":426,
    "list":[
      {
        "id": 6400,
        "title": "币江南：1.28比特币行情解读之江南说年（一）",
        "banner": "http://cdn.juliancj.com/Fj79bTYiIF9EhOkhnrrkbjV7drJs",
        "introduction": "财富不应当是生命的目的，它只是生活的工具。挡不住今天的诱惑，就会失去明天的幸福!",
        "pageView": 3374,
        "source": 1,
        "recommend": 1,
        "likeNumber": 3374,
        "collection": 3374,
        "status": 1,
        "createTime": 1548647116433,
        "updateTime": 1548647116433,
        "category": {
          "id": 2,
          "name": "深度",
          "articles": null
        },
        "user": {
          "id": 80,
          "name": "巨链财经",
          "avatar": "http://cdn.juliancj.com/1545979231118.png",
          "sex": 1,
          "introduction": "最专业的媒体平台",
          "feature": "专业，精准传输区块链价值",
          "auth": 2,
          "grade": 1,
          "score": 0,
          "recommend": null,
          "status": 1,
          "articleCount": 1431,
          "pageViewSum": 26137722,
          "fensSum":1665,
          "isFollowed": null
        }
      },
      // ...
    ]
  }
}
```

- 返回参数说明

| 参数名            | 类型 | 说明                                                                                             |
| ----------------- | ---- | ------------------------------------------------------------------------------------------------ |
| total             | num  | 文章总数                                                                                         |
| list              | ary  | 文章集合                                                                                         |
|                   |      |                                                                                                  |
| id                | num  | 文章 id                                                                                          |
| title             | str  | 文章标题                                                                                         |
| banner            | str  | 文章封面                                                                                         |
| introduction      | str  | 文章简介                                                                                         |
| pageView          | num  | 文章浏览量                                                                                       |
| source            | num  | 文章来源（1 原创; 2 转载）                                                                       |
| recommend         | num  | 文章推荐（0 不推荐; 1 推荐）                                                                     |
| likeNumber        | num  | 文章点赞量                                                                                       |
| collection        | num  | 文章收藏量                                                                                       |
| status            | num  | 文章状态（-3 下线; -2 审核未通过; -1 草稿; 0 待审核; 1 审核通过）                                |
| createTime        | num  | 创建时间                                                                                         |
| updateTime        | num  | 最后修改时间                                                                                     |
| category          | obj  | 文章分类信息                                                                                     |
| category.id       | num  | 文章分类 id                                                                                      |
| category.name     | str  | 文章分类名称                                                                                     |
| user              | obj  | 待定                                                                                             |
| user.id           | num  | 作者 id                                                                                          |
| user.name         | str  | 作者名称                                                                                         |
| user.avatar       | str  | 作者头像                                                                                         |
| user.sex          | num  | 作者性别（1 女性 ,2 男性）                                                                       |
| user.introduction | str  | 作者简介                                                                                         |
| user.feature      | str  | 作者特点                                                                                         |
| user.auth         | num  | 作者认证状态 （0 未认证,1 个人认证, 2 企业认证, -1 认证未通过, 3 申请个人认证, 4 申请企业认证 ） |
| user.grade        | num  | 作者等级（目前 1 - 39）                                                                          |
| user.score        | num  | 作者积分                                                                                         |
| user.recommend    | num  | 作者是否推荐（ 0 否，1 是）                                                                      |
| user.status       | num  | 作者状态（ -2 删除, -1 黑名单, 0 暂停使用, 1 可用）                                              |
| user.articleCount | num  | 作者文章数                                                                                       |
| user.pageViewSum  | num  | 作者浏览数                                                                                       |
| user.fensSum      | num  | 作者粉丝数                                                                                       |
| user.isFollowed   | boo  | 登录用户是否关注（true 已关注, false 未关注）                                                    |

- 备注
  - 暂无

### 3.3.资讯文章详情

- 描述

  - 根据 id 获取资讯文章详情

- 请求 URL

  - `api/v2/article/id`

- 请求方式

  - `GET`

- 参数

| 参数名 | 必选 | 类型   | 说明    |
| ------ | ---- | ------ | ------- |
| id     | 是   | number | 文章 id |

- 返回示例

```javascript
{
  "success": true,
  "message": "ok",
  "data": {
    "id": 5685,
    "title": "Themis CEO 孟宏伟：区块链有待与实体产业深度融合",
    "banner": "https://img.jinse.com/1533395_image1.png",
    "introduction": "2019年新春将至，万象更新。金色财经推出《区块链行业大咖共话新春》系列专题，诚邀区块链大咖们总结过去、畅想新年。Themis CEO 孟宏伟接受金色财经专访并回顾2018、展望2019。",
    "content": "<p>2019年新春将至，万象更新。值此佳节之际，金色财经特推出《区块链行业大咖共话新春》系列专题，诚邀区块链大咖们总结过去、畅想新年。</p>。。。<p>“2019年，希望我们都能在这崭新的起点上发展、落地、走向实体。Themis再次祝大家新年快乐”。</p><p>来源：<a href=\"https://www.jinse.com/news/bitcoin/310826.html\" target=\"_blank\">金色财经</a></p>",
    "pageView": 4800,
    "source": 2,
    "recommend": 0,
    "likeNumber": 3374,
    "collection": 3374,
    "status": 1,
    "createTime": 1548328453750,
    "updateTime": 1548328453750,
    "category": {
      "id": 1,
      "name": "新闻",
      "articles": null
    },
    "user": {
      "id": 80,
      "name": "巨链财经",
      "avatar": "http://cdn.juliancj.com/1545979231118.png",
      "sex": 1,
      "introduction": "最专业的媒体平台",
      "feature": "专业，精准传输区块链价值",
      "auth": 2,
      "grade": 1,
      "score": 0,
      "recommend": null,
      "status": 1,
      "articleCount": 1431,
      "pageViewSum": 26137722,
      "fensSum":1665,
      "isFollowed": null
    },
    "keywords": [
      null
    ],
    "isCollected": false
  }
}
```

- 返回参数说明

| 参数名            | 类型 | 说明                                                                                             |
| ----------------- | ---- | ------------------------------------------------------------------------------------------------ |
| id                | num  | 文章 id                                                                                          |
| title             | str  | 文章标题                                                                                         |
| banner            | str  | 文章封面                                                                                         |
| introduction      | str  | 文章简介                                                                                         |
| content           | str  | 文章内容（富文本）                                                                               |
| pageView          | num  | 文章浏览量                                                                                       |
| source            | num  | 文章来源（1 原创; 2 转载）                                                                       |
| recommend         | num  | 文章推荐（0 不推荐; 1 推荐）                                                                     |
| likeNumber        | num  | 文章点赞量                                                                                       |
| collection        | num  | 文章收藏量                                                                                       |
| status            | num  | 文章状态（-3 下线; -2 审核未通过; -1 草稿; 0 待审核; 1 审核通过）                                |
| createTime        | num  | 创建时间                                                                                         |
| updateTime        | num  | 最后修改时间                                                                                     |
| category          | obj  | 文章分类信息                                                                                     |
| category.id       | num  | 文章分类 id                                                                                      |
| category.name     | str  | 文章分类名称                                                                                     |
| user              | obj  | 作者信息                                                                                         |
| user.id           | num  | 作者 id                                                                                          |
| user.name         | str  | 作者名称                                                                                         |
| user.avatar       | str  | 作者头像                                                                                         |
| user.sex          | num  | 作者性别（1 女性 ,2 男性）                                                                       |
| user.introduction | str  | 作者简介                                                                                         |
| user.feature      | str  | 作者特点                                                                                         |
| user.auth         | num  | 作者认证状态 （0 未认证,1 个人认证, 2 企业认证, -1 认证未通过, 3 申请个人认证, 4 申请企业认证 ） |
| user.grade        | num  | 作者等级（目前 1 - 39）                                                                          |
| user.score        | num  | 作者积分                                                                                         |
| user.recommend    | num  | 作者是否推荐（ 0 否，1 是）                                                                      |
| user.status       | num  | 作者状态（ -2 删除, -1 黑名单, 0 暂停使用, 1 可用）                                              |
| user.articleCount | num  | 作者文章数                                                                                       |
| user.pageViewSum  | num  | 作者浏览数                                                                                       |
| user.fensSum      | num  | 作者粉丝数                                                                                       |
| user.isFollowed   | boo  | 登录用户是否关注（true 已关注, false 未关注）                                                    |
| keywords          | ary  | 文章关键字                                                                                       |
| isCollected       | boo  | 文章是否收藏（true 收藏, false 未收藏）                                                          |

- 备注
  - 暂无

## 4.快讯

### 4.1.快讯列表

- 描述

  - 获取全部快讯

- 请求 URL

  - `api/v2/live?page=1&pagesize=10`

- 请求方式

  - `GET`

- 参数

| 参数名   | 必须 | 类型 | 说明     |
| -------- | ---- | ---- | -------- |
| page     | 是   | num  | 第几页   |
| pagesize | 是   | num  | 每页条数 |

- 返回示例

```javascript
{
  "success": true,
  "message": "ok",
  "data": {
    "total": 11095,
    "list": [
      {
        "id": 11202,
        "title": "行情 | A股收盘：区块链板块下跌2.71％",
        "content": "A股收盘，上证指数收跌0.11%，区块链板块下跌2.71％。80个概念股中，9只上涨，1只平盘，70只下跌。涨幅前三为：中南建设（+8.74％）、恒生电子（+4.71%）、创维数字（+4.49%）; 跌幅前三为：凯恩股份（-9.91％）、御银股份（-9.55%）、宣亚国际（-8.00％）",
        "grade": 4,
        "status": 0,
        "createTime": 1548745515287,
        "updateTime": 1548745515287
      },
      // ...
    ]
  }
}
```

- 返回参数说明

| 参数名  | 类型 | 说明                     |
| ------- | ---- | ------------------------ |
| id      | num  | 快讯 id                  |
| title   | str  | 快讯标题                 |
| content | str  | 快讯内容                 |
| grade   | num  | 快讯星级                 |
| status  | num  | 状态（0 不可用, 1 可用） |

- 备注
  - 暂无

### 4.2.快讯详情

- 描述

  - 根据 id 获取快讯详情

- 请求 URL

  - `api/v2/live/id`

- 请求方式

  - `GET`

- 参数

| 参数名 | 必须 | 类型 | 说明    |
| ------ | ---- | ---- | ------- |
| id     | 是   | num  | 快讯 id |

- 返回示例

```javascript
{
  "success": true,
  "message": "ok",
  "data": {
    "id": 11202,
    "title": "行情 | A股收盘：区块链板块下跌2.71％",
    "content": "A股收盘，上证指数收跌0.11%，区块链板块下跌2.71％。80个概念股中，9只上涨，1只平盘，70只下跌。涨幅前三为：中南建设（+8.74％）、恒生电子（+4.71%）、创维数字（+4.49%）; 跌幅前三为：凯恩股份（-9.91％）、御银股份（-9.55%）、宣亚国际（-8.00％）",
    "grade": 4,
    "status": 0,
    "createTime": 1548745515287,
    "updateTime": 1548745515287
  }
}
```

- 返回参数说明

| 参数名  | 类型 | 说明                     |
| ------- | ---- | ------------------------ |
| id      | num  | 快讯 id                  |
| title   | str  | 快讯标题                 |
| content | str  | 快讯内容                 |
| grade   | num  | 快讯星级                 |
| status  | num  | 状态（0 不可用, 1 可用） |

- 备注
  - 暂无

## 5.专栏

### 5.1.推荐和最新专栏文章

- 描述

  - 根据分类获取专栏中的推荐和最新文章列表

- 请求 URL

  - `api/v2/column/article?type=1`

- 请求方式

  - `GET`

- 参数

| 参数名 | 必须 | 类型 | 说明                         |
| ------ | ---- | ---- | ---------------------------- |
| type   | 是   | num  | 类型(1 推荐文章, 2 最新文章) |

- 返回示例

```javascript
{
  "success": true,
  "message": "ok",
  "data": [
    {
      "id": 6400,
      "title": "币江南：1.28比特币行情解读之江南说年（一）",
      "banner": "http://cdn.juliancj.com/Fj79bTYiIF9EhOkhnrrkbjV7drJs",
      "introduction": "财富不应当是生命的目的，它只是生活的工具。挡不住今天的诱惑，就会失去明天的幸福!",
      "pageView": 3374,
      "source": 1,
      "recommend": 1,
      "likeNumber": 3374,
      "collection": 3374,
      "status": 1,
      "createTime": 1548647116433,
      "updateTime": 1548647116433,
      "category": {
          "id": 2,
          "name": "深度",
          "articles": null
      },
      "user": {
        "id": 80,
        "name": "巨链财经",
        "avatar": "http://cdn.juliancj.com/1545979231118.png",
        "sex": 1,
        "introduction": "最专业的媒体平台",
        "feature": "专业，精准传输区块链价值",
        "auth": 2,
        "grade": 1,
        "score": 0,
        "recommend": null,
        "status": 1,
        "articleCount": 1431,
        "pageViewSum": 26137722,
        "fensSum":1665,
        "isFollowed": null
      }
    },
    // ...
  ]
}
```

- 返回参数说明

| 参数名            | 类型 | 说明                                                                                             |
| ----------------- | ---- | ------------------------------------------------------------------------------------------------ |
| id                | num  | 文章 id                                                                                          |
| title             | str  | 文章标题                                                                                         |
| banner            | str  | 文章封面                                                                                         |
| introduction      | str  | 文章简介                                                                                         |
| pageView          | num  | 文章浏览量                                                                                       |
| source            | num  | 文章来源（1 原创; 2 转载）                                                                       |
| recommend         | num  | 文章推荐（0 不推荐; 1 推荐）                                                                     |
| likeNumber        | num  | 文章点赞量                                                                                       |
| collection        | num  | 文章收藏量                                                                                       |
| status            | num  | 文章状态（-3 下线; -2 审核未通过; -1 草稿; 0 待审核; 1 审核通过）                                |
| createTime        | num  | 创建时间                                                                                         |
| updateTime        | num  | 最后修改时间                                                                                     |
| category          | obj  | 文章分类信息                                                                                     |
| category.id       | num  | 文章分类 id                                                                                      |
| category.name     | str  | 文章分类名称                                                                                     |
| user              | obj  | 作者信息                                                                                         |
| user.id           | num  | 作者 id                                                                                          |
| user.name         | str  | 作者名称                                                                                         |
| user.avatar       | str  | 作者头像                                                                                         |
| user.sex          | num  | 作者性别（1 女性 ,2 男性）                                                                       |
| user.introduction | str  | 作者简介                                                                                         |
| user.feature      | str  | 作者特点                                                                                         |
| user.auth         | num  | 作者认证状态 （0 未认证,1 个人认证, 2 企业认证, -1 认证未通过, 3 申请个人认证, 4 申请企业认证 ） |
| user.grade        | num  | 作者等级（目前 1 - 39）                                                                          |
| user.score        | num  | 作者积分                                                                                         |
| user.recommend    | num  | 作者是否推荐（ 0 否，1 是）                                                                      |
| user.status       | num  | 作者状态（ -2 删除, -1 黑名单, 0 暂停使用, 1 可用）                                              |
| user.articleCount | num  | 作者文章数                                                                                       |
| user.pageViewSum  | num  | 作者浏览数                                                                                       |
| user.fensSum      | num  | 作者粉丝数                                                                                       |
| user.isFollowed   | boo  | 登录用户是否关注（true 已关注, false 未关注）                                                    |

- 备注
  - 暂无

### 5.2.最新作者

- 描述

  - 获取最新入驻作者列表

- 请求 URL

  - `api/v2/column/residentAuthors`

- 请求方式

  - `GET`

- 参数

| 参数名 | 必须 | 类型 | 说明 |
| ------ | ---- | ---- | ---- |
|        |      |      |      |

- 返回示例

```javascript
{
  "success": true,
  "message": "ok",
  "data": [
    {
      "id": 111,
      "name": "一诺",
      "avatar": "http://cdn.juliancj.com/1544510612386.jpg",
      "sex": 1,
      "introduction": "区块链信仰者",
      "feature": "",
      "auth": 1,
      "grade": 1,
      "score": 0,
      "recommend": 1,
      "status": 1,
      "articleCount": 1431,
      "pageViewSum": 26137722,
      "fensSum":1665,
      "isFollowed": null
    },
    // ...
  ]
}
```

- 返回参数说明

| 参数名       | 类型 | 说明                                                                                             |
| ------------ | ---- | ------------------------------------------------------------------------------------------------ |
| id           | num  | 作者 id                                                                                          |
| name         | str  | 作者名称                                                                                         |
| avatar       | str  | 作者头像                                                                                         |
| sex          | num  | 作者性别（1 女性 ,2 男性）                                                                       |
| introduction | str  | 作者简介                                                                                         |
| feature      | str  | 作者特点                                                                                         |
| auth         | num  | 作者认证状态 （0 未认证,1 个人认证, 2 企业认证, -1 认证未通过, 3 申请个人认证, 4 申请企业认证 ） |
| user.grade   | num  | 作者等级（目前 1 - 39）                                                                          |
| score        | num  | 作者积分                                                                                         |
| recommend    | num  | 作者是否推荐（ 0 否，1 是）                                                                      |
| status       | num  | 作者状态（ -2 删除, -1 黑名单, 0 暂停使用, 1 可用）                                              |
| articleCount | num  | 作者文章数                                                                                       |
| pageViewSum  | num  | 作者浏览数                                                                                       |
| fensSum      | num  | 作者粉丝数                                                                                       |
| isFollowed   | boo  | 登录用户是否关注（true 已关注, false 未关注）                                                    |

- 备注
  - 暂无

### 5.3 活跃作者

- 描述

  - 获取活跃作者列表

- 请求 URL

  - `api/v2/column/activeAuthors?page=1&pagesize=10`

- 请求方式

  - `GET`

- 参数

| 参数名   | 必须 | 类型 | 说明     |
| -------- | ---- | ---- | -------- |
| page     | 是   | num  | 第几页   |
| pagesize | 是   | num  | 每页条数 |

- 返回示例

```javascript
{
  "success": true,
  "message": "ok",
  "data": {
    "total": 123,
    "list": [
      {
        "id": 111,
        "name": "一诺",
        "avatar": "http://cdn.juliancj.com/1544510612386.jpg",
        "sex": 1,
        "introduction": "区块链信仰者",
        "feature": "",
        "auth": 1,
        "grade": 1,
        "score": 0,
        "recommend": 1,
        "status": 1,
        "articleCount": 1431,
        "pageViewSum": 26137722,
        "fensSum":1665,
        "isFollowed": null
      },
      // ...
  ]
  }
}
```

- 返回参数说明

| 参数名       | 类型 | 说明                                                                                             |
| ------------ | ---- | ------------------------------------------------------------------------------------------------ |
| id           | num  | 作者 id                                                                                          |
| name         | str  | 作者名称                                                                                         |
| avatar       | str  | 作者头像                                                                                         |
| sex          | num  | 作者性别（1 女性 ,2 男性）                                                                       |
| introduction | str  | 作者简介                                                                                         |
| feature      | str  | 作者特点                                                                                         |
| auth         | num  | 作者认证状态 （0 未认证,1 个人认证, 2 企业认证, -1 认证未通过, 3 申请个人认证, 4 申请企业认证 ） |
| user.grade   | num  | 作者等级（目前 1 - 39）                                                                          |
| score        | num  | 作者积分                                                                                         |
| recommend    | num  | 作者是否推荐（ 0 否，1 是）                                                                      |
| status       | num  | 作者状态（ -2 删除, -1 黑名单, 0 暂停使用, 1 可用）                                              |
| articleCount | num  | 作者文章数                                                                                       |
| pageViewSum  | num  | 作者浏览数                                                                                       |
| fensSum      | num  | 作者粉丝数                                                                                       |
| isFollowed   | boo  | 登录用户是否关注（true 已关注, false 未关注）                                                    |

- 备注
  - 暂无

### 5.4.全部作者

- 描述

  - 无

- 请求 URL

  - `api/v2/column/authors?page=1&pagesize=10`

- 请求方式

  - `GET`

- 参数

| 参数名   | 必须 | 类型 | 说明     |
| -------- | ---- | ---- | -------- |
| page     | 是   | num  | 第几页   |
| pagesize | 是   | num  | 每页条数 |

- 返回示例

```javascript
{
  "success": true,
  "message": "ok",
  "data": {
    "total": 59,
    "list": [
      {
        "id": 111,
        "name": "一诺",
        "avatar": "http://cdn.juliancj.com/1544510612386.jpg",
        "sex": 1,
        "introduction": "区块链信仰者",
        "feature": "",
        "auth": 1,
        "grade": 1,
        "score": 0,
        "recommend": 1,
        "status": 1,
        "articleCount": 1431,
        "pageViewSum": 26137722,
        "fensSum":1665,
        "isFollowed": null
      },
      // ...
    ]
  }
}
```

- 返回参数说明

| 参数名       | 类型 | 说明                                                                                             |
| ------------ | ---- | ------------------------------------------------------------------------------------------------ |
| id           | num  | 作者 id                                                                                          |
| name         | str  | 作者名称                                                                                         |
| avatar       | str  | 作者头像                                                                                         |
| sex          | num  | 作者性别（1 女性 ,2 男性）                                                                       |
| introduction | str  | 作者简介                                                                                         |
| feature      | str  | 作者特点                                                                                         |
| auth         | num  | 作者认证状态 （0 未认证,1 个人认证, 2 企业认证, -1 认证未通过, 3 申请个人认证, 4 申请企业认证 ） |
| user.grade   | num  | 作者等级（目前 1 - 39）                                                                          |
| score        | num  | 作者积分                                                                                         |
| recommend    | num  | 作者是否推荐（ 0 否，1 是）                                                                      |
| status       | num  | 作者状态（ -2 删除, -1 黑名单, 0 暂停使用, 1 可用）                                              |
| articleCount | num  | 作者文章数                                                                                       |
| pageViewSum  | num  | 作者浏览数                                                                                       |
| fensSum      | num  | 作者粉丝数                                                                                       |
| isFollowed   | boo  | 登录用户是否关注（true 已关注, false 未关注）                                                    |

- 备注
  - 暂无

### 5.5.获取作者全部文章（资讯？项目？福利？）

- 描述

  - 根据作者 id 获取其全部文章列表

- 请求 URL

  - `api/v2/column/authors/id/article?page=1&pagesize=10`

- 请求方式

  - `GET`

- 参数

| 参数名   | 必须 | 类型 | 说明     |
| -------- | ---- | ---- | -------- |
| id       | 是   | num  | 作者 id  |
| page     | 是   | num  | 第几页   |
| pagesize | 是   | num  | 每页条数 |

- 返回示例

```javascript
{
  "success": true,
  "message": "ok",
  "data": {
    "total": 1,
    "list": [
      {
        "id": 6400,
        "title": "币江南：1.28比特币行情解读之江南说年（一）",
        "banner": "http://cdn.juliancj.com/Fj79bTYiIF9EhOkhnrrkbjV7drJs",
        "introduction": "财富不应当是生命的目的，它只是生活的工具。挡不住今天的诱惑，就会失去明天的幸福!",
        "pageView": 3374,
        "source": 1,
        "recommend": 1,
        "likeNumber": 3374,
        "collection": 3374,
        "status": 1,
        "createTime": 1548647116433,
        "updateTime": 1548647116433,
        "category": {
            "id": 2,
            "name": "深度",
            "articles": null
        },
        "user": {
          "id": 80,
          "name": "巨链财经",
          "avatar": "http://cdn.juliancj.com/1545979231118.png",
          "sex": 1,
          "introduction": "最专业的媒体平台",
          "feature": "专业，精准传输区块链价值",
          "auth": 2,
          "grade": 1,
          "score": 0,
          "recommend": null,
          "status": 1,
          "articleCount": 1431,
          "pageViewSum": 26137722,
          "fensSum":1665,
          "isFollowed": null
        }
      }
    ],
    // ...
  }
}
```

- 返回参数说明

| 参数名            | 类型 | 说明                                                                                             |
| ----------------- | ---- | ------------------------------------------------------------------------------------------------ |
| id                | num  | 文章 id                                                                                          |
| title             | str  | 文章标题                                                                                         |
| banner            | str  | 文章封面                                                                                         |
| introduction      | str  | 文章简介                                                                                         |
| pageView          | num  | 文章浏览量                                                                                       |
| source            | num  | 文章来源（1 原创; 2 转载）                                                                       |
| recommend         | num  | 文章推荐（0 不推荐; 1 推荐）                                                                     |
| likeNumber        | num  | 文章点赞量                                                                                       |
| collection        | num  | 文章收藏量                                                                                       |
| status            | num  | 文章状态（-3 下线; -2 审核未通过; -1 草稿; 0 待审核; 1 审核通过）                                |
| createTime        | num  | 创建时间                                                                                         |
| updateTime        | num  | 最后修改时间                                                                                     |
| category          | obj  | 文章分类信息                                                                                     |
| category.id       | num  | 文章分类 id                                                                                      |
| category.name     | str  | 文章分类名称                                                                                     |
| user              | obj  | 作者信息                                                                                         |
| user.id           | num  | 作者 id                                                                                          |
| user.name         | str  | 作者名称                                                                                         |
| user.avatar       | str  | 作者头像                                                                                         |
| user.sex          | num  | 作者性别（1 女性 ,2 男性）                                                                       |
| user.introduction | str  | 作者简介                                                                                         |
| user.feature      | str  | 作者特点                                                                                         |
| user.auth         | num  | 作者认证状态 （0 未认证,1 个人认证, 2 企业认证, -1 认证未通过, 3 申请个人认证, 4 申请企业认证 ） |
| user.grade        | num  | 作者等级（目前 1 - 39）                                                                          |
| user.score        | num  | 作者积分                                                                                         |
| user.recommend    | num  | 作者是否推荐（ 0 否，1 是）                                                                      |
| user.status       | num  | 作者状态（ -2 删除, -1 黑名单, 0 暂停使用, 1 可用）                                              |
| user.articleCount | num  | 作者文章数                                                                                       |
| user.pageViewSum  | num  | 作者浏览数                                                                                       |
| user.fensSum      | num  | 作者粉丝数                                                                                       |
| user.isFollowed   | boo  | 登录用户是否关注（true 已关注, false 未关注）                                                    |

- 备注
  - 暂无

## 6.项目

### 6.1.推荐项目/项目动态/项目库（？？？）

- 描述

  - 根据分类 id 分别获取推荐项目/项目动态/项目库文章列表

- 请求 URL

  - `api/v2/item/type/article?page=1&pagesize=10`

- 请求方式

  - `GET`

- 参数

| 参数名   | 必须 | 类型 | 说明     |
| -------- | ---- | ---- | -------- |
| type     | 是   | num  | 类型     |
| page     | 是   | num  | 第几页   |
| pagesize | 是   | num  | 每页条数 |

- 返回示例

```javascript
{
  "success": true,
  "message": "ok",
  "data": {
    "total": 23,
    "list": [
      {
        "id": 40,
        "title": "贝住，社区型分红",
        "banner": "http://cdn.juliancj.com/FqUkuWzJoOrlXSkLHU13e-Nx8ybe",
        "introduction": "带你理解贝住的成长红利。",
        "pageView": 16131,
        "source": 1,
        "recommend": 0,
        "likeNumber": 0,
        "collection": 3374,
        "status": 1,
        "createTime": 1546594306355,
        "updateTime": 1546594306355,
        "product": {
          // ...
        }
      },
      // ...
    ]
  }
}
```

- 返回参数说明

| 参数名       | 类型 | 说明                                                              |
| ------------ | ---- | ----------------------------------------------------------------- |
| id           | num  | 文章 id                                                           |
| title        | str  | 文章标题                                                          |
| banner       | str  | 文章封面                                                          |
| introduction | str  | 文章简介                                                          |
| pageView     | num  | 文章浏览量                                                        |
| source       | num  | 文章来源（1 原创; 2 转载）                                        |
| recommend    | num  | 文章推荐（0 不推荐; 1 推荐）                                      |
| likeNumber   | num  | 文章点赞量                                                        |
| collection   | num  | 文章收藏量                                                        |
| status       | num  | 文章状态（-3 下线; -2 审核未通过; -1 草稿; 0 待审核; 1 审核通过） |
| createTime   | str  | 创建时间                                                          |
| updateTime   | str  | 修改时间                                                          |
| product      | obj  | 待定                                                              |

- 备注
  - 暂无

### 6.2.获取项目文章详情（是否分类？）

- 描述

  - 根据 id 获取项目文章详情

- 请求 URL

  - `api/v2/item/id`

- 请求方式

  - `GET`

- 参数

| 参数名 | 必须 | 类型 | 说明    |
| ------ | ---- | ---- | ------- |
| id     | 是   | num  | 文章 id |

- 返回示例

```javascript
{
  "success": true,
  "message": "ok",
  "data": {
    "id": 5685,
    "title": "Themis CEO 孟宏伟：区块链有待与实体产业深度融合",
    "banner": "https://img.jinse.com/1533395_image1.png",
    "introduction": "2019年新春将至，万象更新。金色财经推出《区块链行业大咖共话新春》系列专题，诚邀区块链大咖们总结过去、畅想新年。Themis CEO 孟宏伟接受金色财经专访并回顾2018、展望2019。",
    "content": "<p>2019年新春将至，万象更新。值此佳节之际，金色财经特推出《区块链行业大咖共话新春》系列专题，诚邀区块链大咖们总结过去、畅想新年。</p>。。。<p>“2019年，希望我们都能在这崭新的起点上发展、落地、走向实体。Themis再次祝大家新年快乐”。</p><p>来源：<a href=\"https://www.jinse.com/news/bitcoin/310826.html\" target=\"_blank\">金色财经</a></p>",
    "pageView": 4800,
    "source": 2,
    "recommend": 0,
    "likeNumber": 3374,
    "collection": 3374,
    "status": 1,
    "createTime": 1548328453750,
    "updateTime": 1548328453750,
    "user": {
      "id": 80,
      "name": "巨链财经",
      "avatar": "http://cdn.juliancj.com/1545979231118.png",
      "sex": 1,
      "introduction": "最专业的媒体平台",
      "feature": "专业，精准传输区块链价值",
      "auth": 2,
      "grade": 1,
      "score": 0,
      "recommend": null,
      "status": 1,
      "articleCount": 1431,
      "pageViewSum": 26137722,
      "fensSum":1665,
      "isFollowed": null
    },
    "keywords": [
      null
    ],
    "isCollected": false
}
```

- 返回参数说明

| 参数名            | 类型 | 说明                                                                                             |
| ----------------- | ---- | ------------------------------------------------------------------------------------------------ |
| id                | num  | 文章 id                                                                                          |
| title             | str  | 文章标题                                                                                         |
| banner            | str  | 文章封面                                                                                         |
| introduction      | str  | 文章简介                                                                                         |
| content           | str  | 文章内容（富文本）                                                                               |
| pageView          | num  | 文章浏览量                                                                                       |
| source            | num  | 文章来源（1 原创; 2 转载）                                                                       |
| recommend         | num  | 文章推荐（0 不推荐; 1 推荐）                                                                     |
| likeNumber        | num  | 文章点赞量                                                                                       |
| collection        | num  | 文章收藏量                                                                                       |
| status            | num  | 文章状态（-3 下线; -2 审核未通过; -1 草稿; 0 待审核; 1 审核通过）                                |
| createTime        | num  | 创建时间                                                                                         |
| updateTime        | num  | 最后修改时间                                                                                     |
| user              | obj  | 作者信息                                                                                         |
| user.id           | num  | 作者 id                                                                                          |
| user.name         | str  | 作者名称                                                                                         |
| user.avatar       | str  | 作者头像                                                                                         |
| user.sex          | num  | 作者性别（1 女性 ,2 男性）                                                                       |
| user.introduction | str  | 作者简介                                                                                         |
| user.feature      | str  | 作者特点                                                                                         |
| user.auth         | num  | 作者认证状态 （0 未认证,1 个人认证, 2 企业认证, -1 认证未通过, 3 申请个人认证, 4 申请企业认证 ） |
| user.grade        | num  | 作者等级（目前 1 - 39）                                                                          |
| user.score        | num  | 作者积分                                                                                         |
| user.recommend    | num  | 作者是否推荐（ 0 否，1 是）                                                                      |
| user.status       | num  | 作者状态（ -2 删除, -1 黑名单, 0 暂停使用, 1 可用）                                              |
| user.articleCount | num  | 作者文章数                                                                                       |
| user.pageViewSum  | num  | 作者浏览数                                                                                       |
| user.fensSum      | num  | 作者粉丝数                                                                                       |
| user.isFollowed   | boo  | 登录用户是否关注（true 已关注, false 未关注）                                                    |
| keywords          | ary  | 文章关键字                                                                                       |
| isCollected       | boo  | 文章是否收藏（true 收藏, false 未收藏）                                                          |

- 备注
  - 暂无

## 7.福利

### 7.1.推荐文章/糖库文章（是否分类？）

- 描述

  - 根据类型获取福利推荐文章或糖库库文章

- 请求 URL

  - `api/v2/material/type/article?page=1&pagesize=10`

- 请求方式

  - `GET`

- 参数

| 参数名   | 必须 | 类型 | 说明                           |
| -------- | ---- | ---- | ------------------------------ |
| type     | 是   | num  | 类型（1 推荐文章; 2 糖库文章） |
| page     | 是   | num  | 第几页                         |
| pagesize | 是   | num  | 每页条数                       |

- 返回示例

```javascript
{
  "success": true,
  "message": "ok",
  "data": {
    "total":426,
    "list":[
      {
        "id": 6400,
        "title": "币江南：1.28比特币行情解读之江南说年（一）",
        "banner": "http://cdn.juliancj.com/Fj79bTYiIF9EhOkhnrrkbjV7drJs",
        "introduction": "财富不应当是生命的目的，它只是生活的工具。挡不住今天的诱惑，就会失去明天的幸福!",
        "pageView": 3374,
        "source": 1,
        "recommend": 1,
        "likeNumber": 3374,
        "collection": 3374,
        "status": 1,
        "createTime": 1548647116433,
        "updateTime": 1548647116433,
        "user": {
          "id": 80,
          "name": "巨链财经",
          "avatar": "http://cdn.juliancj.com/1545979231118.png",
          "sex": 1,
          "introduction": "最专业的媒体平台",
          "feature": "专业，精准传输区块链价值",
          "auth": 2,
          "grade": 1,
          "score": 0,
          "recommend": null,
          "status": 1,
          "articleCount": 1431,
          "pageViewSum": 26137722,
          "fensSum":1665,
          "isFollowed": null
        }
      },
      // ...
    ]
  }
}
```

- 返回参数说明

| 参数名            | 类型 | 说明                                                                                             |
| ----------------- | ---- | ------------------------------------------------------------------------------------------------ |
| id                | num  | 文章 id                                                                                          |
| title             | str  | 文章标题                                                                                         |
| banner            | str  | 文章封面                                                                                         |
| introduction      | str  | 文章简介                                                                                         |
| pageView          | num  | 文章浏览量                                                                                       |
| source            | num  | 文章来源（1 原创; 2 转载）                                                                       |
| recommend         | num  | 文章推荐（0 不推荐; 1 推荐）                                                                     |
| likeNumber        | num  | 文章点赞量                                                                                       |
| collection        | num  | 文章收藏量                                                                                       |
| status            | num  | 文章状态（-3 下线; -2 审核未通过; -1 草稿; 0 待审核; 1 审核通过）                                |
| createTime        | num  | 创建时间                                                                                         |
| updateTime        | num  | 最后修改时间                                                                                     |
| user              | obj  | 待定                                                                                             |
| user.id           | num  | 作者 id                                                                                          |
| user.name         | str  | 作者名称                                                                                         |
| user.avatar       | str  | 作者头像                                                                                         |
| user.sex          | num  | 作者性别（1 女性 ,2 男性）                                                                       |
| user.introduction | str  | 作者简介                                                                                         |
| user.feature      | str  | 作者特点                                                                                         |
| user.auth         | num  | 作者认证状态 （0 未认证,1 个人认证, 2 企业认证, -1 认证未通过, 3 申请个人认证, 4 申请企业认证 ） |
| user.grade        | num  | 作者等级（目前 1 - 39）                                                                          |
| user.score        | num  | 作者积分                                                                                         |
| user.recommend    | num  | 作者是否推荐（ 0 否，1 是）                                                                      |
| user.status       | num  | 作者状态（ -2 删除, -1 黑名单, 0 暂停使用, 1 可用）                                              |
| user.articleCount | num  | 作者文章数                                                                                       |
| user.pageViewSum  | num  | 作者浏览数                                                                                       |
| user.fensSum      | num  | 作者粉丝数                                                                                       |
| user.isFollowed   | boo  | 登录用户是否关注（true 已关注, false 未关注）                                                    |

- 备注
  - 暂无

### 7.2.小白资料

- 描述

  - 获取小白资料列表

- 请求 URL

  - `api/v2/material/data`

- 请求方式

  - `GET`

- 参数

| 参数名 | 必须 | 类型 | 说明 |
| ------ | ---- | ---- | ---- |
|        |      |      |      |

- 返回示例

```javascript
{
  "success":true,
  "message":"ok",
  "data":[
    {
      "id":1,
      "name":"巨链财经300份区块链白皮书",
      "tag":"[百度云盘]",
      "url":"https://pan.baidu.com/s/1yY_sV46DKVnADsDgkAf2Dg",
      "code":"s9p1",
      "status":1
    }
  ]
}
```

- 返回参数说明

| 参数名 | 类型 | 说明                           |
| ------ | ---- | ------------------------------ |
| id     | num  | 小白资料 id                    |
| name   | str  | 小白资料名称                   |
| tag    | str  | 资料标签                       |
| url    | str  | 资料下载地址                   |
| code   | str  | 提取码                         |
| status | num  | 小白资料状态（1 上线; 2 下线） |

- 备注
  - 有可能并入 推荐/糖库 模块

### 7.3.获取福利文章详情

- 描述

  - 根据 id 获取福利文章详情

- 请求 URL

  - `api/v2/material/id`

- 请求方式

  - `GET`

- 参数

| 参数名 | 必须 | 类型 | 说明    |
| ------ | ---- | ---- | ------- |
| id     | 是   | num  | 文章 id |

- 返回示例

```javascript
{
  "success": true,
  "message": "ok",
  "data": {
    "id": 5685,
    "title": "Themis CEO 孟宏伟：区块链有待与实体产业深度融合",
    "banner": "https://img.jinse.com/1533395_image1.png",
    "introduction": "2019年新春将至，万象更新。金色财经推出《区块链行业大咖共话新春》系列专题，诚邀区块链大咖们总结过去、畅想新年。Themis CEO 孟宏伟接受金色财经专访并回顾2018、展望2019。",
    "content": "<p>2019年新春将至，万象更新。值此佳节之际，金色财经特推出《区块链行业大咖共话新春》系列专题，诚邀区块链大咖们总结过去、畅想新年。</p>。。。<p>“2019年，希望我们都能在这崭新的起点上发展、落地、走向实体。Themis再次祝大家新年快乐”。</p><p>来源：<a href=\"https://www.jinse.com/news/bitcoin/310826.html\" target=\"_blank\">金色财经</a></p>",
    "pageView": 4800,
    "source": 2,
    "recommend": 0,
    "likeNumber": 3374,
    "collection": 3374,
    "status": 1,
    "createTime": 1548328453750,
    "updateTime": 1548328453750,
    "user": {
      "id": 80,
      "name": "巨链财经",
      "avatar": "http://cdn.juliancj.com/1545979231118.png",
      "sex": 1,
      "introduction": "最专业的媒体平台",
      "feature": "专业，精准传输区块链价值",
      "auth": 2,
      "grade": 1,
      "score": 0,
      "recommend": null,
      "status": 1,
      "articleCount": 1431,
      "pageViewSum": 26137722,
      "fensSum":1665,
      "isFollowed": null
    },
    "keywords": [
      null
    ],
    "isCollected": false
}
```

- 返回参数说明

| 参数名            | 类型 | 说明                                                                                             |
| ----------------- | ---- | ------------------------------------------------------------------------------------------------ |
| id                | num  | 文章 id                                                                                          |
| title             | str  | 文章标题                                                                                         |
| banner            | str  | 文章封面                                                                                         |
| introduction      | str  | 文章简介                                                                                         |
| content           | str  | 文章内容（富文本）                                                                               |
| pageView          | num  | 文章浏览量                                                                                       |
| source            | num  | 文章来源（1 原创; 2 转载）                                                                       |
| recommend         | num  | 文章推荐（0 不推荐; 1 推荐）                                                                     |
| likeNumber        | num  | 文章点赞量                                                                                       |
| collection        | num  | 文章收藏量                                                                                       |
| status            | num  | 文章状态（-3 下线; -2 审核未通过; -1 草稿; 0 待审核; 1 审核通过）                                |
| createTime        | num  | 创建时间                                                                                         |
| updateTime        | num  | 最后修改时间                                                                                     |
| user              | obj  | 作者信息                                                                                         |
| user.id           | num  | 作者 id                                                                                          |
| user.name         | str  | 作者名称                                                                                         |
| user.avatar       | str  | 作者头像                                                                                         |
| user.sex          | num  | 作者性别（1 女性 ,2 男性）                                                                       |
| user.introduction | str  | 作者简介                                                                                         |
| user.feature      | str  | 作者特点                                                                                         |
| user.auth         | num  | 作者认证状态 （0 未认证,1 个人认证, 2 企业认证, -1 认证未通过, 3 申请个人认证, 4 申请企业认证 ） |
| user.grade        | num  | 作者等级（目前 1 - 39）                                                                          |
| user.score        | num  | 作者积分                                                                                         |
| user.recommend    | num  | 作者是否推荐（ 0 否，1 是）                                                                      |
| user.status       | num  | 作者状态（ -2 删除, -1 黑名单, 0 暂停使用, 1 可用）                                              |
| user.articleCount | num  | 作者文章数                                                                                       |
| user.pageViewSum  | num  | 作者浏览数                                                                                       |
| user.fensSum      | num  | 作者粉丝数                                                                                       |
| user.isFollowed   | boo  | 登录用户是否关注（true 已关注, false 未关注）                                                    |
| keywords          | ary  | 文章关键字                                                                                       |
| isCollected       | boo  | 文章是否收藏（true 收藏, false 未收藏）                                                          |

- 备注
  - 暂无

## 8.搜索

### 8.1.搜索资讯文章

- 描述

  - 根据搜索关键字获取资讯文章列表

- 请求 URL

  - `api/v2/article/search?searchWord=text&page=1&pagesize=10`

- 请求方式

  - `GET`

- 参数

| 参数名   | 必须 | 类型 | 说明       |
| -------- | ---- | ---- | ---------- |
| text     | 是   | str  | 搜索关键字 |
| page     | 是   | num  | 第几页     |
| pagesize | 是   | num  | 每页条数   |

- 返回示例

```javascript
{
  "success": true,
  "message": "ok",
  "data": {
    "total":426,
    "list":[
      {
        "id": 6400,
        "title": "币江南：1.28比特币行情解读之江南说年（一）",
        "banner": "http://cdn.juliancj.com/Fj79bTYiIF9EhOkhnrrkbjV7drJs",
        "introduction": "财富不应当是生命的目的，它只是生活的工具。挡不住今天的诱惑，就会失去明天的幸福!",
        "pageView": 3374,
        "source": 1,
        "recommend": 1,
        "likeNumber": 3374,
        "collection": 3374,
        "status": 1,
        "createTime": 1548647116433,
        "updateTime": 1548647116433,
        "category": {
          "id": 2,
          "name": "深度",
          "articles": null
        },
        "user": {
          "id": 80,
          "name": "巨链财经",
          "avatar": "http://cdn.juliancj.com/1545979231118.png",
          "sex": 1,
          "introduction": "最专业的媒体平台",
          "feature": "专业，精准传输区块链价值",
          "auth": 2,
          "grade": 1,
          "score": 0,
          "recommend": null,
          "status": 1,
          "articleCount": 1431,
          "pageViewSum": 26137722,
          "fensSum":1665,
          "isFollowed": null
        }
      },
      // ...
    ]
  }
}
```

- 返回参数说明

| 参数名            | 类型 | 说明                                                                                             |
| ----------------- | ---- | ------------------------------------------------------------------------------------------------ |
| id                | num  | 文章 id                                                                                          |
| title             | str  | 文章标题                                                                                         |
| banner            | str  | 文章封面                                                                                         |
| introduction      | str  | 文章简介                                                                                         |
| pageView          | num  | 文章浏览量                                                                                       |
| source            | num  | 文章来源（1 原创; 2 转载）                                                                       |
| recommend         | num  | 文章推荐（0 不推荐; 1 推荐）                                                                     |
| likeNumber        | num  | 文章点赞量                                                                                       |
| collection        | num  | 文章收藏量                                                                                       |
| status            | num  | 文章状态（-3 下线; -2 审核未通过; -1 草稿; 0 待审核; 1 审核通过）                                |
| createTime        | num  | 创建时间                                                                                         |
| updateTime        | num  | 最后修改时间                                                                                     |
| category          | obj  | 文章分类信息                                                                                     |
| category.id       | num  | 文章分类 id                                                                                      |
| category.name     | str  | 文章分类名称                                                                                     |
| user              | obj  | 作者信息                                                                                         |
| user.id           | num  | 作者 id                                                                                          |
| user.name         | str  | 作者名称                                                                                         |
| user.avatar       | str  | 作者头像                                                                                         |
| user.sex          | num  | 作者性别（1 女性 ,2 男性）                                                                       |
| user.introduction | str  | 作者简介                                                                                         |
| user.feature      | str  | 作者特点                                                                                         |
| user.auth         | num  | 作者认证状态 （0 未认证,1 个人认证, 2 企业认证, -1 认证未通过, 3 申请个人认证, 4 申请企业认证 ） |
| user.grade        | num  | 作者等级（目前 1 - 39）                                                                          |
| user.score        | num  | 作者积分                                                                                         |
| user.recommend    | num  | 作者是否推荐（ 0 否，1 是）                                                                      |
| user.status       | num  | 作者状态（ -2 删除, -1 黑名单, 0 暂停使用, 1 可用）                                              |
| user.articleCount | num  | 作者文章数                                                                                       |
| user.pageViewSum  | num  | 作者浏览数                                                                                       |
| user.fensSum      | num  | 作者粉丝数                                                                                       |
| user.isFollowed   | boo  | 登录用户是否关注（true 已关注, false 未关注）                                                    |

- 备注
  - 暂无

### 8.2.搜索项目文章

- 描述

  - 根据搜索关键字获取项目文章列表

- 请求 URL

  - `api/v2/item/search?searchWord=text&page=1&pagesize=10`

- 请求方式

  - `GET`

- 参数

| 参数名   | 必须 | 类型 | 说明       |
| -------- | ---- | ---- | ---------- |
| text     | 是   | str  | 搜索关键字 |
| page     | 是   | num  | 第几页     |
| pagesize | 是   | num  | 每页条数   |

- 返回示例

```javascript
{
  "success": true,
  "message": "ok",
  "data": {
    "total":426,
    "list":[
      {
        "id": 6400,
        "title": "币江南：1.28比特币行情解读之江南说年（一）",
        "banner": "http://cdn.juliancj.com/Fj79bTYiIF9EhOkhnrrkbjV7drJs",
        "introduction": "财富不应当是生命的目的，它只是生活的工具。挡不住今天的诱惑，就会失去明天的幸福!",
        "pageView": 3374,
        "source": 1,
        "recommend": 1,
        "likeNumber": 3374,
        "collection": 3374,
        "status": 1,
        "createTime": 1548647116433,
        "updateTime": 1548647116433,
        "user": {
          "id": 80,
          "name": "巨链财经",
          "avatar": "http://cdn.juliancj.com/1545979231118.png",
          "sex": 1,
          "introduction": "最专业的媒体平台",
          "feature": "专业，精准传输区块链价值",
          "auth": 2,
          "grade": 1,
          "score": 0,
          "recommend": null,
          "status": 1,
          "articleCount": 1431,
          "pageViewSum": 26137722,
          "fensSum":1665,
          "isFollowed": null
        }
      },
      // ...
    ]
  }
}
```

- 返回参数说明

| 参数名            | 类型 | 说明                                                                                             |
| ----------------- | ---- | ------------------------------------------------------------------------------------------------ |
| id                | num  | 文章 id                                                                                          |
| title             | str  | 文章标题                                                                                         |
| banner            | str  | 文章封面                                                                                         |
| introduction      | str  | 文章简介                                                                                         |
| pageView          | num  | 文章浏览量                                                                                       |
| source            | num  | 文章来源（1 原创; 2 转载）                                                                       |
| recommend         | num  | 文章推荐（0 不推荐; 1 推荐）                                                                     |
| likeNumber        | num  | 文章点赞量                                                                                       |
| collection        | num  | 文章收藏量                                                                                       |
| status            | num  | 文章状态（-3 下线; -2 审核未通过; -1 草稿; 0 待审核; 1 审核通过）                                |
| createTime        | num  | 创建时间                                                                                         |
| updateTime        | num  | 最后修改时间                                                                                     |
| user              | obj  | 作者信息                                                                                         |
| user.id           | num  | 作者 id                                                                                          |
| user.name         | str  | 作者名称                                                                                         |
| user.avatar       | str  | 作者头像                                                                                         |
| user.sex          | num  | 作者性别（1 女性 ,2 男性）                                                                       |
| user.introduction | str  | 作者简介                                                                                         |
| user.feature      | str  | 作者特点                                                                                         |
| user.auth         | num  | 作者认证状态 （0 未认证,1 个人认证, 2 企业认证, -1 认证未通过, 3 申请个人认证, 4 申请企业认证 ） |
| user.grade        | num  | 作者等级（目前 1 - 39）                                                                          |
| user.score        | num  | 作者积分                                                                                         |
| user.recommend    | num  | 作者是否推荐（ 0 否，1 是）                                                                      |
| user.status       | num  | 作者状态（ -2 删除, -1 黑名单, 0 暂停使用, 1 可用）                                              |
| user.articleCount | num  | 作者文章数                                                                                       |
| user.pageViewSum  | num  | 作者浏览数                                                                                       |
| user.fensSum      | num  | 作者粉丝数                                                                                       |
| user.isFollowed   | boo  | 登录用户是否关注（true 已关注, false 未关注）                                                    |

- 备注
  - 暂无

### 8.3.搜索福利文章

- 描述

  - 根据搜索关键字获取福利文章列表

- 请求 URL

  - `api/v2/material/search?searchWord=text&page=1&pagesize=10`

- 请求方式

  - `GET`

- 参数

| 参数名   | 必须 | 类型 | 说明       |
| -------- | ---- | ---- | ---------- |
| text     | 是   | str  | 搜索关键字 |
| page     | 是   | num  | 第几页     |
| pagesize | 是   | num  | 每页条数   |

- 返回示例

```javascript
{
  "success": true,
  "message": "ok",
  "data": {
    "total":426,
    "list":[
      {
        "id": 6400,
        "title": "币江南：1.28比特币行情解读之江南说年（一）",
        "banner": "http://cdn.juliancj.com/Fj79bTYiIF9EhOkhnrrkbjV7drJs",
        "introduction": "财富不应当是生命的目的，它只是生活的工具。挡不住今天的诱惑，就会失去明天的幸福!",
        "pageView": 3374,
        "source": 1,
        "recommend": 1,
        "likeNumber": 3374,
        "collection": 3374,
        "status": 1,
        "createTime": 1548647116433,
        "updateTime": 1548647116433,
        "user": {
          "id": 80,
          "name": "巨链财经",
          "avatar": "http://cdn.juliancj.com/1545979231118.png",
          "sex": 1,
          "introduction": "最专业的媒体平台",
          "feature": "专业，精准传输区块链价值",
          "auth": 2,
          "grade": 1,
          "score": 0,
          "recommend": null,
          "status": 1,
          "articleCount": 1431,
          "pageViewSum": 26137722,
          "fensSum":1665,
          "isFollowed": null
        }
      },
      // ...
    ]
  }
}
```

- 返回参数说明

| 参数名            | 类型 | 说明                                                                                             |
| ----------------- | ---- | ------------------------------------------------------------------------------------------------ |
| id                | num  | 文章 id                                                                                          |
| title             | str  | 文章标题                                                                                         |
| banner            | str  | 文章封面                                                                                         |
| introduction      | str  | 文章简介                                                                                         |
| pageView          | num  | 文章浏览量                                                                                       |
| source            | num  | 文章来源（1 原创; 2 转载）                                                                       |
| recommend         | num  | 文章推荐（0 不推荐; 1 推荐）                                                                     |
| likeNumber        | num  | 文章点赞量                                                                                       |
| collection        | num  | 文章收藏量                                                                                       |
| status            | num  | 文章状态（-3 下线; -2 审核未通过; -1 草稿; 0 待审核; 1 审核通过）                                |
| createTime        | num  | 创建时间                                                                                         |
| updateTime        | num  | 最后修改时间                                                                                     |
| user              | obj  | 作者信息                                                                                         |
| user.id           | num  | 作者 id                                                                                          |
| user.name         | str  | 作者名称                                                                                         |
| user.avatar       | str  | 作者头像                                                                                         |
| user.sex          | num  | 作者性别（1 女性 ,2 男性）                                                                       |
| user.introduction | str  | 作者简介                                                                                         |
| user.feature      | str  | 作者特点                                                                                         |
| user.auth         | num  | 作者认证状态 （0 未认证,1 个人认证, 2 企业认证, -1 认证未通过, 3 申请个人认证, 4 申请企业认证 ） |
| user.grade        | num  | 作者等级（目前 1 - 39）                                                                          |
| user.score        | num  | 作者积分                                                                                         |
| user.recommend    | num  | 作者是否推荐（ 0 否，1 是）                                                                      |
| user.status       | num  | 作者状态（ -2 删除, -1 黑名单, 0 暂停使用, 1 可用）                                              |
| user.articleCount | num  | 作者文章数                                                                                       |
| user.pageViewSum  | num  | 作者浏览数                                                                                       |
| user.fensSum      | num  | 作者粉丝数                                                                                       |
| user.isFollowed   | boo  | 登录用户是否关注（true 已关注, false 未关注）                                                    |

- 备注
  - 暂无

### 8.4.搜索专栏用户

- 描述

  - 根据搜索关键字获取专栏用户列表

- 请求 URL

  - `api/v2/column/search?searchWord=text&page=1&pagesize=10`

- 请求方式

  - `GET`

- 参数

| 参数名   | 必须 | 类型 | 说明       |
| -------- | ---- | ---- | ---------- |
| text     | 是   | str  | 搜索关键字 |
| page     | 是   | num  | 第几页     |
| pagesize | 是   | num  | 每页条数   |

- 返回示例

```javascript
{
  "success": true,
  "message": "ok",
  "data": {
    "total":26,
    "list":[
      {
        "id": 80,
        "name": "巨链财经",
        "avatar": "http://cdn.juliancj.com/1545979231118.png",
        "sex": 1,
        "introduction": "最专业的媒体平台",
        "feature": "专业，精准传输区块链价值",
        "auth": 2,
        "grade": 1,
        "score": 0,
        "recommend": null,
        "status": 1,
        "articleCount": 1431,
        "pageViewSum": 26137722,
        "fensSum":1665,
        "isFollowed": null
      },
      // ...
    ]
  }
}
```

- 返回参数说明

| 参数名            | 类型 | 说明                                                                                             |
| ----------------- | ---- | ------------------------------------------------------------------------------------------------ |
| user.id           | num  | 作者 id                                                                                          |
| user.name         | str  | 作者名称                                                                                         |
| user.avatar       | str  | 作者头像                                                                                         |
| user.sex          | num  | 作者性别（1 女性 ,2 男性）                                                                       |
| user.introduction | str  | 作者简介                                                                                         |
| user.feature      | str  | 作者特点                                                                                         |
| user.auth         | num  | 作者认证状态 （0 未认证,1 个人认证, 2 企业认证, -1 认证未通过, 3 申请个人认证, 4 申请企业认证 ） |
| user.grade        | num  | 作者等级（目前 1 - 39）                                                                          |
| user.score        | num  | 作者积分                                                                                         |
| user.recommend    | num  | 作者是否推荐（ 0 否，1 是）                                                                      |
| user.status       | num  | 作者状态（ -2 删除, -1 黑名单, 0 暂停使用, 1 可用）                                              |
| user.articleCount | num  | 作者文章数                                                                                       |
| user.pageViewSum  | num  | 作者浏览数                                                                                       |
| user.fensSum      | num  | 作者粉丝数                                                                                       |
| user.isFollowed   | boo  | 登录用户是否关注（true 已关注, false 未关注）                                                    |

- 备注
  - 暂无

## 9.登录-注册

### 9.1.获取验证码

- 描述

  - 获取验证码

- 请求 URL

  - `api/v2/getCode?mobile=18661772012`

- 请求方式

  - `GET`

- 参数

| 参数名 | 必须 | 类型 | 说明   |
| ------ | ---- | ---- | ------ |
| mobile | 是   | num  | 手机号 |

- 返回示例

```javascript
{
  "success": true,
  "message": "ok",
  "data": "512326"
}
```

- 返回参数说明

| 参数名 | 类型 | 说明   |
| ------ | ---- | ------ |
| data   | str  | 验证码 |

- 备注
  - 暂无

### 9.2.注册

- 描述

  - 注册

- 请求 URL

  - `api/v2/register`

- 请求方式

  - `POST`

- 参数

| 参数名          | 必须 | 类型 | 说明     |
| --------------- | ---- | ---- | -------- |
| mobile          | 是   | str  | 手机号   |
| code            | 是   | str  | 验证码   |
| password        | 是   | str  | 登录密码 |
| confirmPassword | 是   | str  | 确认密码 |

- 返回示例

```javascript
{
  "success": true,
  "message": "ok",
  "data": {
    "id": 80,
    "name": "巨链财经",
    "password": null,
    "mobile": "18810946802",
    "avatar": "http://cdn.juliancj.com/1545979231118.png",
    "sex": 1,
    "introduction": "最专业的媒体平台",
    "feature": "专业，精准传输区块链价值",
    "auth": 2,
    "grade": 1,
    "score": 0,
    "recommend": null,
    "status": 1,
    "articleCount": 1431,
    "pageViewSum": 26137722,
    "fensSum": 1665,
    "token": null,
  }
}
```

- 返回参数说明

| 参数名       | 类型 | 说明                                                                                          |
| ------------ | ---- | --------------------------------------------------------------------------------------------- |
| id           | num  | 用户 id                                                                                       |
| name         | str  | 用户名                                                                                        |
| password     | str  | 用户密码                                                                                      |
| mobile       | str  | 用户手机号                                                                                    |
| avatar       | str  | 用户头像                                                                                      |
| sex          | str  | 用户性别（1 女性 ,2 男性）                                                                    |
| introduction | str  | 用户简介                                                                                      |
| feature      | str  | 用户特点                                                                                      |
| auth         | num  | 用户认证状态 （0 未认证,1 个人认证, 2 企业认证, -1 认证未通过, 3 申请个人认证, 4 申请企业认证 |
| grade        | num  | 用户等级（目前 1 - 39）                                                                       |
| score        | num  | 用户积分                                                                                      |
| recommend    | num  | 用户是否推荐（ 0 否，1 是）                                                                   |
| status       | num  | 用户状态（ -2 删除, -1 黑名单, 0 暂停使用, 1 可用）                                           |
| articleCount | num  | 用户文章数                                                                                    |
| pageViewSum  | num  | 用户浏览数                                                                                    |
| fensSum      | num  | 用户粉丝数                                                                                    |
| token        | num  | 用户 token                                                                                    |

- 备注
  - 暂无

### 9.3.忘记密码/重设密码

- 描述

  - 忘记密码/重设密码

- 请求 URL

  - `api/v2/forgetPassword`

- 请求方式

  - `POST`

- 参数

| 参数名          | 必须 | 类型 | 说明     |
| --------------- | ---- | ---- | -------- |
| mobile          | 是   | str  | 手机号   |
| code            | 是   | str  | 验证码   |
| password        | 是   | str  | 新密码   |
| confirmPassword | 是   | str  | 确认密码 |

- 返回示例

```javascript
{
  "success": true,
  "message": "ok",
  "data": {
    "id": 80,
    "name": "巨链财经",
    "password": null,
    "mobile": "18810946802",
    "avatar": "http://cdn.juliancj.com/1545979231118.png",
    "sex": 1,
    "introduction": "最专业的媒体平台",
    "feature": "专业，精准传输区块链价值",
    "auth": 2,
    "grade": 1,
    "score": 0,
    "recommend": null,
    "status": 1,
    "articleCount": 1431,
    "pageViewSum": 26137722,
    "fensSum": 1665,
    "token": null,
  }
}
```

- 返回参数说明

| 参数名       | 类型 | 说明                                                                                          |
| ------------ | ---- | --------------------------------------------------------------------------------------------- |
| id           | num  | 用户 id                                                                                       |
| name         | str  | 用户名                                                                                        |
| password     | str  | 用户密码                                                                                      |
| mobile       | str  | 用户手机号                                                                                    |
| avatar       | str  | 用户头像                                                                                      |
| sex          | str  | 用户性别（1 女性 ,2 男性）                                                                    |
| introduction | str  | 用户简介                                                                                      |
| feature      | str  | 用户特点                                                                                      |
| auth         | num  | 用户认证状态 （0 未认证,1 个人认证, 2 企业认证, -1 认证未通过, 3 申请个人认证, 4 申请企业认证 |
| grade        | num  | 用户等级（目前 1 - 39）                                                                       |
| score        | num  | 用户积分                                                                                      |
| recommend    | num  | 用户是否推荐（ 0 否，1 是）                                                                   |
| status       | num  | 用户状态（ -2 删除, -1 黑名单, 0 暂停使用, 1 可用）                                           |
| articleCount | num  | 用户文章数                                                                                    |
| pageViewSum  | num  | 用户浏览数                                                                                    |
| fensSum      | num  | 用户粉丝数                                                                                    |
| token        | num  | 用户 token                                                                                    |

- 备注
  - 暂无

### 9.4.登录

- 描述

  - 手机号登录或密码登录

- 请求 URL

  - `api/v2/login?type=1`

- 请求方式

  - `POST`

- 参数

| 参数名   | 必须 | 类型 | 说明                       |
| -------- | ---- | ---- | -------------------------- |
| mobile   | 是   | str  | 手机号                     |
| code     | 是   | str  | 手机登录验证码（`type=1`） |
| password | 是   | str  | 密码登录密码(`type=2`)     |

- 返回示例

```javascript
{
  "success": true,
  "message": "ok",
  "data": {
    "id": 80,
    "name": "巨链财经",
    "password": null,
    "mobile": "18810946802",
    "avatar": "http://cdn.juliancj.com/1545979231118.png",
    "sex": 1,
    "introduction": "最专业的媒体平台",
    "feature": "专业，精准传输区块链价值",
    "auth": 2,
    "grade": 1,
    "score": 0,
    "recommend": null,
    "status": 1,
    "articleCount": 1431,
    "pageViewSum": 26137722,
    "fensSum": 1665,
    "token": null,
  }
}
```

- 返回参数说明

| 参数名       | 类型 | 说明                                                                                          |
| ------------ | ---- | --------------------------------------------------------------------------------------------- |
| id           | num  | 用户 id                                                                                       |
| name         | str  | 用户名                                                                                        |
| password     | str  | 用户密码                                                                                      |
| mobile       | str  | 用户手机号                                                                                    |
| avatar       | str  | 用户头像                                                                                      |
| sex          | str  | 用户性别（1 女性 ,2 男性）                                                                    |
| introduction | str  | 用户简介                                                                                      |
| feature      | str  | 用户特点                                                                                      |
| auth         | num  | 用户认证状态 （0 未认证,1 个人认证, 2 企业认证, -1 认证未通过, 3 申请个人认证, 4 申请企业认证 |
| grade        | num  | 用户等级（目前 1 - 39）                                                                       |
| score        | num  | 用户积分                                                                                      |
| recommend    | num  | 用户是否推荐（ 0 否，1 是）                                                                   |
| status       | num  | 用户状态（ -2 删除, -1 黑名单, 0 暂停使用, 1 可用）                                           |
| articleCount | num  | 用户文章数                                                                                    |
| pageViewSum  | num  | 用户浏览数                                                                                    |
| fensSum      | num  | 用户粉丝数                                                                                    |
| token        | str  | 用户 token                                                                                    |

- 备注
  - 暂无

## 10.个人中心

### 10.1.个人中心

#### 10.1.1.修改个人信息

- 描述

  - 修改个人信息

- 请求 URL

  - `api/v2/user/id`

- 请求方式

  - `PUT`

- 参数

| 参数名       | 必须 | 类型 | 说明     |
| ------------ | ---- | ---- | -------- |
| id           | 是   | num  | 用户 id  |
| avatar       | 是   | str  | 用户头像 |
| name         | 是   | str  | 用户名   |
| sex          | 是   | num  | 用户性别 |
| feature      | 是   | str  | 用户特点 |
| introduction | 是   | str  | 用户介绍 |

- 返回示例

```javascript
{
  "success": true,
  "message": "ok",
  "data": 1
}
```

- 返回参数说明

| 参数名 | 类型 | 说明           |
| ------ | ---- | -------------- |
| data   | num  | 1 成功，2 失败 |

- 备注
  - 暂无

#### 10.1.2.修改手机号

- 描述

  - 修改手机号

- 请求 URL

  - `api/v2/user/changeMobile`

- 请求方式

  - `PUT`

- 参数

| 参数名 | 必须 | 类型 | 说明     |
| ------ | ---- | ---- | -------- |
| userId | 是   | num  | 用户 id  |
| mobile | 是   | str  | 新手机号 |
| code   | 是   | str  | 验证码   |

- 返回示例

```javascript
{
  "success": true,
  "message": "ok",
  "data": 1
}
```

- 返回参数说明

| 参数名 | 类型 | 说明           |
| ------ | ---- | -------------- |
| data   | num  | 1 成功，2 失败 |

- 备注
  - 暂无

#### 10.1.3.个人用户认证

- 描述

  - 个人用户认证(用身份证和军人证)

- 请求 URL

  - `api/v2/user/authPerson/auth`

- 请求方式

  - `POST`

- 参数

| 参数名   | 必须 | 类型 | 说明                           |
| -------- | ---- | ---- | ------------------------------ |
| userId   | 是   | num  | 用户 id                        |
| type     | 是   | num  | 证件类型（1 身份证, 2 军人证） |
| code     | 是   | str  | 证件号码                       |
| frontPic | 是   | str  | 证件正面照                     |
| backPic  | 是   | str  | 证件背面照                     |
| status   | 是   | num  | 状态（0 不可用，1 可用）       |

- 返回示例

```javascript
{
  "success": true,
  "message": "ok",
  "data": 1
}
```

- 返回参数说明

| 参数名 | 类型 | 说明           |
| ------ | ---- | -------------- |
| data   | num  | 1 成功，2 失败 |

- 备注
  - 暂无

#### 10.1.4.企业用户认证

- 描述

  - 企业用户认证

- 请求 URL

  - `api/v2/user/authCompany/auth`

- 请求方式

  - `POST`

- 参数

| 参数名  | 必须 | 类型 | 说明                     |
| ------- | ---- | ---- | ------------------------ |
| userId  | 是   | num  | 用户 id                  |
| name    | 是   | str  | 公司名                   |
| uscc    | 是   | str  | 统一社会信用代码         |
| license | 是   | str  | 营业执照照片             |
| status  | 是   | num  | 状态（0 不可用，1 可用） |

- 返回示例

```javascript
{
  "success": true,
  "message": "ok",
  "data": 1
}
```

- 返回参数说明

| 参数名 | 类型 | 说明           |
| ------ | ---- | -------------- |
| data   | num  | 1 成功，2 失败 |

- 备注
  - 暂无

#### 10.1.5.获取用户信息

- 描述

  - 根据用户 id 获取用户信息

- 请求 URL

  - `api/v2/user/id`

- 请求方式

  - `GET`

- 参数

| 参数名 | 必须 | 类型 | 说明    |
| ------ | ---- | ---- | ------- |
| id     | 是   | num  | 用户 id |

- 返回示例

```javascript
{
  "success": true,
  "message": "ok",
  "data": {
    "id": 80,
    "name": "巨链财经",
    "mobile": "18810946802",
    "avatar": "http://cdn.juliancj.com/1545979231118.png",
    "sex": 1,
    "introduction": "最专业的媒体平台",
    "feature": "专业，精准传输区块链价值",
    "auth": 2,
    "grade": 1,
    "score": 0,
    "recommend": null,
    "status": 1,
    "articleCount": 1431,
    "pageViewSum": 26137722,
    "fensSum": 1665,
  }
}
```

- 返回参数说明

| 参数名       | 类型 | 说明                                                                                          |
| ------------ | ---- | --------------------------------------------------------------------------------------------- |
| id           | num  | 用户 id                                                                                       |
| name         | str  | 用户名                                                                                        |
| mobile       | str  | 用户手机号                                                                                    |
| avatar       | str  | 用户头像                                                                                      |
| sex          | str  | 用户性别（1 女性 ,2 男性）                                                                    |
| introduction | str  | 用户简介                                                                                      |
| feature      | str  | 用户特点                                                                                      |
| auth         | num  | 用户认证状态 （0 未认证,1 个人认证, 2 企业认证, -1 认证未通过, 3 申请个人认证, 4 申请企业认证 |
| grade        | num  | 用户等级（目前 1 - 39）                                                                       |
| score        | num  | 用户积分                                                                                      |
| recommend    | num  | 用户是否推荐（ 0 否，1 是）                                                                   |
| status       | num  | 用户状态（ -2 删除, -1 黑名单, 0 暂停使用, 1 可用）                                           |
| articleCount | num  | 用户文章数                                                                                    |
| pageViewSum  | num  | 用户浏览数                                                                                    |
| fensSum      | num  | 用户粉丝数                                                                                     |

- 备注
  - 暂无

### 10.2.我的文章

#### 10.2.1.获取资讯文章

- 描述

  - 获取用户资讯类不同状态文章

- 请求 URL

  - `api/v2/user/id/article?status=2&page=1&pagesize=10`

- 请求方式

  - `GET`

- 参数

| 参数名   | 必须 | 类型 | 说明                                                          |
| -------- | ---- | ---- | ------------------------------------------------------------- |
| id       | 是   | num  | 用户 id                                                       |
| status   | 是   | num  | 文章状态（-3 下线，-2，未通过，-1 草稿，0 待审核 1 审核通过） |
| page     | 是   | num  | 第几页                                                        |
| pagesize | 是   | num  | 每页条数                                                      |

- 返回示例

```javascript
{
  "success": true,
  "message": "ok",
  "data": {
    "total":426,
    "list":[
      {
        "id": 6400,
        "title": "币江南：1.28比特币行情解读之江南说年（一）",
        "banner": "http://cdn.juliancj.com/Fj79bTYiIF9EhOkhnrrkbjV7drJs",
        "introduction": "财富不应当是生命的目的，它只是生活的工具。挡不住今天的诱惑，就会失去明天的幸福!",
        "pageView": 3374,
        "source": 1,
        "recommend": 1,
        "likeNumber": 3374,
        "collection": 3374,
        "status": 1,
        "createTime": 1548647116433,
        "updateTime": 1548647116433,
        "category": {
          "id": 2,
          "name": "深度",
          "articles": null
        },
      },
      // ...
    ]
  }
}
```

- 返回参数说明

| 参数名        | 类型 | 说明                                                              |
| ------------- | ---- | ----------------------------------------------------------------- |
| id            | num  | 文章 id                                                           |
| title         | str  | 文章标题                                                          |
| banner        | str  | 文章封面                                                          |
| introduction  | str  | 文章简介                                                          |
| pageView      | num  | 文章浏览量                                                        |
| source        | num  | 文章来源（1 原创; 2 转载）                                        |
| recommend     | num  | 文章推荐（0 不推荐; 1 推荐）                                      |
| likeNumber    | num  | 文章点赞量                                                        |
| collection    | num  | 文章收藏量                                                        |
| status        | num  | 文章状态（-3 下线; -2 审核未通过; -1 草稿; 0 待审核; 1 审核通过） |
| createTime    | num  | 创建时间                                                          |
| updateTime    | num  | 最后修改时间                                                      |
| category      | obj  | 文章分类信息                                                      |
| category.id   | num  | 文章分类 id                                                       |
| category.name | str  | 文章分类名称                                                         |

- 备注
  - 暂无

#### 10.2.2.获取项目文章

- 描述

  - 获取用户项目类不同状态文章

- 请求 URL

  - `api/v2/user/id/item?status=2&page=1&pagesize=10`

- 请求方式

  - `GET`

- 参数

| 参数名   | 必须 | 类型 | 说明                                                          |
| -------- | ---- | ---- | ------------------------------------------------------------- |
| id       | 是   | num  | 用户 id                                                       |
| status   | 是   | num  | 文章状态（-3 下线，-2，未通过，-1 草稿，0 待审核 1 审核通过） |
| page     | 是   | num  | 第几页                                                        |
| pagesize | 是   | num  | 每页条数                                                      |

- 返回示例

```javascript
{
  "success": true,
  "message": "ok",
  "data": {
    "total":426,
    "list":[
      {
        "id": 6400,
        "title": "币江南：1.28比特币行情解读之江南说年（一）",
        "banner": "http://cdn.juliancj.com/Fj79bTYiIF9EhOkhnrrkbjV7drJs",
        "introduction": "财富不应当是生命的目的，它只是生活的工具。挡不住今天的诱惑，就会失去明天的幸福!",
        "pageView": 3374,
        "source": 1,
        "recommend": 1,
        "likeNumber": 3374,
        "collection": 3374,
        "status": 1,
        "createTime": 1548647116433,
        "updateTime": 1548647116433,
      },
      // ...
    ]
  }
}
```

- 返回参数说明

| 参数名        | 类型 | 说明                                                              |
| ------------- | ---- | ----------------------------------------------------------------- |
| id            | num  | 文章 id                                                           |
| title         | str  | 文章标题                                                          |
| banner        | str  | 文章封面                                                          |
| introduction  | str  | 文章简介                                                          |
| pageView      | num  | 文章浏览量                                                        |
| source        | num  | 文章来源（1 原创; 2 转载）                                        |
| recommend     | num  | 文章推荐（0 不推荐; 1 推荐）                                      |
| likeNumber    | num  | 文章点赞量                                                        |
| collection    | num  | 文章收藏量                                                        |
| status        | num  | 文章状态（-3 下线; -2 审核未通过; -1 草稿; 0 待审核; 1 审核通过） |
| createTime    | num  | 创建时间                                                          |
| updateTime    | num  | 最后修改时间                                                              |

- 备注
  - 暂无

#### 10.2.3.获取福利文章

- 描述

  - 获取用户福利类不同状态文章

- 请求 URL

  - `api/v2/user/id/material?status=2&page=1&pagesize=10`

- 请求方式

  - `GET`

- 参数

| 参数名   | 必须 | 类型 | 说明                                                          |
| -------- | ---- | ---- | ------------------------------------------------------------- |
| id       | 是   | num  | 用户 id                                                       |
| status   | 是   | num  | 文章状态（-3 下线，-2，未通过，-1 草稿，0 待审核 1 审核通过） |
| page     | 是   | num  | 第几页                                                        |
| pagesize | 是   | num  | 每页条数                                                      |

- 返回示例

```javascript
{
  "success": true,
  "message": "ok",
  "data": {
    "total":426,
    "list":[
      {
        "id": 6400,
        "title": "币江南：1.28比特币行情解读之江南说年（一）",
        "banner": "http://cdn.juliancj.com/Fj79bTYiIF9EhOkhnrrkbjV7drJs",
        "introduction": "财富不应当是生命的目的，它只是生活的工具。挡不住今天的诱惑，就会失去明天的幸福!",
        "pageView": 3374,
        "source": 1,
        "recommend": 1,
        "likeNumber": 3374,
        "collection": 3374,
        "status": 1,
        "createTime": 1548647116433,
        "updateTime": 1548647116433,
      },
      // ...
    ]
  }
}
```

- 返回参数说明

| 参数名        | 类型 | 说明                                                              |
| ------------- | ---- | ----------------------------------------------------------------- |
| id            | num  | 文章 id                                                           |
| title         | str  | 文章标题                                                          |
| banner        | str  | 文章封面                                                          |
| introduction  | str  | 文章简介                                                          |
| pageView      | num  | 文章浏览量                                                        |
| source        | num  | 文章来源（1 原创; 2 转载）                                        |
| recommend     | num  | 文章推荐（0 不推荐; 1 推荐）                                      |
| likeNumber    | num  | 文章点赞量                                                        |
| collection    | num  | 文章收藏量                                                        |
| status        | num  | 文章状态（-3 下线; -2 审核未通过; -1 草稿; 0 待审核; 1 审核通过） |
| createTime    | num  | 创建时间                                                          |
| updateTime    | num  | 最后修改时间                                                               |

- 备注
  - 暂无

#### 10.2.4.修改资讯文章

- 描述

  - 修改资讯文章

- 请求 URL

  - `api/v2/user/article/id`

- 请求方式

  - `PUT`

- 参数

| 参数名       | 必须 | 类型 | 说明                      |
| ------------ | ---- | ---- | ------------------------- |
| id           | 是   | num  | 文章 id                   |
| userId       | 是   | num  | 用户 id                   |
| categoryId   | 是   | num  | 文章分类                  |
| title        | 是   | str  | 文章标题                  |
| banner       | 是   | str  | 文章封面                  |
| introduction | 是   | str  | 文章简介                  |
| content      | 是   | str  | 文章内容                  |
| source       | 是   | num  | 文章来源                  |
| keywordIds   | 是   | str  | 关键词 id，以半角逗号隔开 |

- 返回示例

```javascript
{
  "success": true,
  "message": "ok",
  "data": 1
}
```

- 返回参数说明

| 参数名 | 类型 | 说明           |
| ------ | ---- | -------------- |
| data   | num  | 1 成功，2 失败 |

- 备注
  - 暂无

#### 10.2.5.修改项目文章

- 描述

  - 修改项目文章

- 请求 URL

  - `api/v2/user/item/id`

- 请求方式

  - `PUT`

- 参数

| 参数名       | 必须 | 类型 | 说明                      |
| ------------ | ---- | ---- | ------------------------- |
| id           | 是   | num  | 文章 id                   |
| userId       | 是   | num  | 用户 id                   |
| categoryId   | 是   | num  | 文章分类                  |
| title        | 是   | str  | 文章标题                  |
| banner       | 是   | str  | 文章封面                  |
| introduction | 是   | str  | 文章简介                  |
| content      | 是   | str  | 文章内容                  |
| source       | 是   | num  | 文章来源                  |
| keywordIds   | 是   | str  | 关键词 id，以半角逗号隔开 |

- 返回示例

```javascript
{
  "success": true,
  "message": "ok",
  "data": 1
}
```

- 返回参数说明

| 参数名 | 类型 | 说明           |
| ------ | ---- | -------------- |
| data   | num  | 1 成功，2 失败 |

- 备注
  - 暂无

#### 10.2.6.修改福利文章

- 描述

  - 修改福利文章

- 请求 URL

  - `api/v2/user/material/id`

- 请求方式

  - `PUT`

- 参数

| 参数名       | 必须 | 类型 | 说明                      |
| ------------ | ---- | ---- | ------------------------- |
| id           | 是   | num  | 文章 id                   |
| userId       | 是   | num  | 用户 id                   |
| categoryId   | 是   | num  | 文章分类                  |
| title        | 是   | str  | 文章标题                  |
| banner       | 是   | str  | 文章封面                  |
| introduction | 是   | str  | 文章简介                  |
| content      | 是   | str  | 文章内容                  |
| source       | 是   | num  | 文章来源                  |
| keywordIds   | 是   | str  | 关键词 id，以半角逗号隔开 |

- 返回示例

```javascript
{
  "success": true,
  "message": "ok",
  "data": 1
}
```

- 返回参数说明

| 参数名 | 类型 | 说明           |
| ------ | ---- | -------------- |
| data   | num  | 1 成功，2 失败 |

- 备注
  - 暂无

#### 10.2.7.发布资讯文章

- 描述

  - 无

- 请求 URL

  - `api/v2/user/article`

- 请求方式

  - `POST`

- 参数

| 参数名       | 必须 | 类型 | 说明                      |
| ------------ | ---- | ---- | ------------------------- |
| userId       | 是   | num  | 用户 id                   |
| categoryId   | 是   | num  | 文章分类 id               |
| title        | 是   | str  | 文章标题                  |
| banner       | 是   | str  | 文章封面                  |
| introduction | 是   | str  | 文章简介                  |
| content      | 是   | str  | 文章内容                  |
| source       | 是   | num  | 文章来源                  |
| keywordIds   | 是   | str  | 关键词 id，以半角逗号隔开 |

- 返回示例

```javascript
{
  "success": true,
  "message": "ok",
  "data": 1
}
```

- 返回参数说明

| 参数名 | 类型 | 说明           |
| ------ | ---- | -------------- |
| data   | num  | 1 成功，2 失败 |

- 备注
  - 暂无

#### 10.2.8.发布项目文章

- 描述

  - 发布项目文章

- 请求 URL

  - `api/v2/user/item`

- 请求方式

  - `POST`

- 参数

| 参数名       | 必须 | 类型 | 说明                      |
| ------------ | ---- | ---- | ------------------------- |
| userId       | 是   | num  | 用户 id                   |
| categoryId   | 是   | num  | 文章分类 id               |
| title        | 是   | str  | 文章标题                  |
| banner       | 是   | str  | 文章封面                  |
| introduction | 是   | str  | 文章简介                  |
| content      | 是   | str  | 文章内容                  |
| source       | 是   | num  | 文章来源                  |
| keywordIds   | 是   | str  | 关键词 id，以半角逗号隔开 |

- 返回示例

```javascript
{
  "success": true,
  "message": "ok",
  "data": 1
}
```

- 返回参数说明

| 参数名 | 类型 | 说明           |
| ------ | ---- | -------------- |
| data   | num  | 1 成功，2 失败 |

- 备注
  - 暂无

#### 10.2.9.发布福利文章

- 描述

  - 发布福利文章

- 请求 URL

  - `api/v2/user/material`

- 请求方式

  - `POST`

- 参数

| 参数名       | 必须 | 类型 | 说明                      |
| ------------ | ---- | ---- | ------------------------- |
| userId       | 是   | num  | 用户 id                   |
| categoryId   | 是   | num  | 文章分类 id               |
| title        | 是   | str  | 文章标题                  |
| banner       | 是   | str  | 文章封面                  |
| introduction | 是   | str  | 文章简介                  |
| content      | 是   | str  | 文章内容                  |
| source       | 是   | num  | 文章来源                  |
| keywordIds   | 是   | str  | 关键词 id，以半角逗号隔开 |

- 返回示例

```javascript
{
  "success": true,
  "message": "ok",
  "data": 1
}
```

- 返回参数说明

| 参数名 | 类型 | 说明           |
| ------ | ---- | -------------- |
| data   | num  | 1 成功，2 失败 |

- 备注
  - 暂无

#### 10.2.10.删除资讯文章

- 描述

  - 删除资讯文章

- 请求 URL

  - `api/v2/user/article`

- 请求方式

  - `DELETE`

- 参数

| 参数名 | 必须 | 类型 | 说明    |
| ------ | ---- | ---- | ------- |
| userId | 是   | num  | 用户 id |
| cid    | 是   | num  | 文章 id |

- 返回示例

```javascript
{
  "success": true,
  "message": "ok",
  "data": 1
}
```

- 返回参数说明

| 参数名 | 类型 | 说明           |
| ------ | ---- | -------------- |
| data   | num  | 1 成功，2 失败 |

- 备注
  - 暂无

#### 10.2.11.删除项目文章

- 描述

  - 删除项目文章

- 请求 URL

  - `api/v2/user/item`

- 请求方式

  - `DELETE`

- 参数

| 参数名 | 必须 | 类型 | 说明    |
| ------ | ---- | ---- | ------- |
| userId | 是   | num  | 用户 id |
| cid    | 是   | num  | 文章 id |

- 返回示例

```javascript
{
  "success": true,
  "message": "ok",
  "data": 1
}
```

- 返回参数说明

| 参数名 | 类型 | 说明           |
| ------ | ---- | -------------- |
| data   | num  | 1 成功，2 失败 |

- 备注
  - 暂无

#### 10.2.12.删除福利文章

- 描述

  - 删除福利文章

- 请求 URL

  - `api/v2/user/material`

- 请求方式

  - `DELETE`

- 参数

| 参数名 | 必须 | 类型 | 说明    |
| ------ | ---- | ---- | ------- |
| userId | 是   | num  | 用户 id |
| cid    | 是   | num  | 文章 id |

- 返回示例

```javascript
{
  "success": true,
  "message": "ok",
  "data": 1
}
```

- 返回参数说明

| 参数名 | 类型 | 说明           |
| ------ | ---- | -------------- |
| data   | num  | 1 成功，2 失败 |

- 备注
  - 暂无

#### 10.2.13.获取文章关键词列表

- 描述

  - 获取资讯文章关键词列表（项目和福利文章？？？福利文章区不区分小白资料）

- 请求 URL

  - `api/v2/user/keyword`

- 请求方式

  - `GET`

- 参数

| 参数名 | 必须 | 类型 | 说明 |
| ------ | ---- | ---- | ---- |
|        |      |      |      |

- 返回示例

```javascript
{
   "success": true,
    "message": "ok",
    "data":[
      {
        "id": 1,
        "name": "BTC",
        "userId": 1,
        "ref": 0,
        "status": 1,
        "createTime": 1535704661148,
        "updateTime": 1535704764450
      },
      // ...
    ]
}
```

- 返回参数说明

| 参数名 | 类型 | 说明                  |
| ------ | ---- | --------------------- |
| id     | num  | 关键词 id             |
| name   | str  | 关键词                |
| status | num  | 状态(0 不可用 1 可用) |

- 备注
  - 暂无

### 10.3.我的收藏

#### 10.3.1.用户收藏文章

- 描述

  - 获取用户收藏文章

- 请求 URL

  - `api/v2/user/id/collection?type=2&page=1&pagesize=10`

- 请求方式

  - `GET`

- 参数

| 参数名   | 必须 | 类型 | 说明                             |
| -------- | ---- | ---- | -------------------------------- |
| id       | 是   | num  | 用户 id                          |
| type     | 是   | num  | 文章类型（1 咨询 2 项目 3 福利） |
| page     | 是   | num  | 第几页                           |
| pagesize | 是   | num  | 每页条数                         |

- 返回示例

```javascript
{
  "success": true,
  "message": "ok",
  "data": {
    "total":426,
    "list":[
      {
        "id": 6400,
        "title": "币江南：1.28比特币行情解读之江南说年（一）",
        "banner": "http://cdn.juliancj.com/Fj79bTYiIF9EhOkhnrrkbjV7drJs",
        "introduction": "财富不应当是生命的目的，它只是生活的工具。挡不住今天的诱惑，就会失去明天的幸福!",
        "pageView": 3374,
        "source": 1,
        "recommend": 1,
        "likeNumber": 3374,
        "collection": 3374,
        "status": 1,
        "createTime": 1548647116433,
        "updateTime": 1548647116433,
        "category": {
          "id": 2,
          "name": "深度",
          "articles": null
        },
        "user": {
          // ...
        }
      },
      // ...
    ]
  }
}
```

- 返回参数说明

| 参数名        | 类型 | 说明                                                              |
| ------------- | ---- | ----------------------------------------------------------------- |
| id            | num  | 文章 id                                                           |
| title         | str  | 文章标题                                                          |
| banner        | str  | 文章封面                                                          |
| introduction  | str  | 文章简介                                                          |
| pageView      | num  | 文章浏览量                                                        |
| source        | num  | 文章来源（1 原创; 2 转载）                                        |
| recommend     | num  | 文章推荐（0 不推荐; 1 推荐）                                      |
| likeNumber    | num  | 文章点赞量                                                        |
| collection    | num  | 文章收藏量                                                        |
| status        | num  | 文章状态（-3 下线; -2 审核未通过; -1 草稿; 0 待审核; 1 审核通过） |
| createTime    | num  | 创建时间                                                          |
| updateTime    | num  | 最后修改时间                                                      |
| category      | obj  | 文章分类信息                                                      |
| category.id   | num  | 文章分类 id                                                       |
| category.name | str  | 文章分类名称                                                      |
| user          | obj  | 作者信息                                                              |

- 备注
  - 暂无

#### 10.3.2.收藏文章

- 描述

  - 用户收藏文章

- 请求 URL

  - `api/v2/user/collection`

- 请求方式

  - `POST`

- 参数

| 参数名 | 必须 | 类型 | 说明                             |
| ------ | ---- | ---- | -------------------------------- |
| userId | 是   | num  | 用户 id                          |
| type   | 是   | num  | 文章类型（1 咨询 2 项目 3 福利） |
| cid    | 是   | num  | 文章 id                          |

- 返回示例

```javascript
{
  "success": true,
  "message": "ok",
  "data": 1
}
```

- 返回参数说明

| 参数名 | 类型 | 说明           |
| ------ | ---- | -------------- |
| data   | num  | 1 成功，2 失败 |

- 备注
  - 暂无

#### 10.3.3.删除收藏文章

- 描述

  - 根据 id 删除用户收藏文章

- 请求 URL

  - `api/v2/user/collection`
    <!-- - `api/v2/user/collection/delete` -->

- 请求方式

  - `DELETE`
    <!-- - `POST` -->

- 参数

| 参数名 | 必须 | 类型 | 说明                             |
| ------ | ---- | ---- | -------------------------------- |
| userId | 是   | num  | 用户 id                          |
| type   | 是   | num  | 文章类型（1 咨询 2 项目 3 福利） |
| cid    | 是   | num  | 文章 id                          |

- 返回示例

```javascript
{
  "success": true,
  "message": "ok",
  "data": 1
}
```

- 返回参数说明

| 参数名 | 类型 | 说明           |
| ------ | ---- | -------------- |
| data   | num  | 1 成功，2 失败 |

- 备注
  - 暂无

### 10.4.我的关注

#### 10.4.1.获取关注列表

- 描述

  - 获取用户关注列表

- 请求 URL

  - `api/v2/user/id/follow?page=1&pagesize=10`

- 请求方式

  - `GET`

- 参数

| 参数名   | 必须 | 类型 | 说明     |
| -------- | ---- | ---- | -------- |
| id       | 是   | num  | 用户 id  |
| page     | 是   | num  | 第几页   |
| pagesize | 是   | num  | 每页条数 |

- 返回示例

```javascript
{
  "success": true,
  "message": "ok",
  "data":{
    "total": 59,
    "list": [
      {
        "id": 111,
        "name": "一诺",
        "avatar": "http://cdn.juliancj.com/1544510612386.jpg",
        "sex": 1,
        "introduction": "区块链信仰者",
        "feature": "",
        "auth": 1,
        "grade": 1,
        "score": 0,
        "recommend": 1,
        "status": 1,
        "articleCount": 1431,
        "pageViewSum": 26137722,
        "fensSum":1665,
        "isFollowed": null
      },
      // ...
    ]
  }
}
```

- 返回参数说明

| 参数名       | 类型 | 说明                                                                                             |
| ------------ | ---- | ------------------------------------------------------------------------------------------------ |
| id           | num  | 作者 id                                                                                          |
| name         | str  | 作者名称                                                                                        |
| avatar       | str  | 作者头像                                                                                         |
| sex          | num  | 作者性别（1 女性 ,2 男性）                                                                       |
| introduction | str  | 作者简介                                                                                         |
| feature      | str  | 作者特点                                                                                         |
| auth         | num  | 作者认证状态 （0 未认证,1 个人认证, 2 企业认证, -1 认证未通过, 3 申请个人认证, 4 申请企业认证 ） |
| user.grade   | num  | 作者等级（目前 1 - 39）                                                                          |
| score        | num  | 作者积分                                                                                         |
| recommend    | num  | 作者是否推荐（ 0 否，1 是）                                                                      |
| status       | num  | 作者状态（ -2 删除, -1 黑名单, 0 暂停使用, 1 可用）                                              |
| articleCount | num  | 作者文章数                                                                                       |
| pageViewSum  | num  | 作者浏览数                                                                                       |
| fensSum      | num  | 作者粉丝数                                                                                        |
| isFollowed   | boo  | 登录用户是否关注（true 已关注, false 未关注）                                                    |

- 备注
  - 暂无

#### 10.4.2.粉丝列表

- 描述

  - 获取用户粉丝列表

- 请求 URL

  - `api/v2/user/id/fens?page=1&pagesize=10`

- 请求方式

  - `GET`

- 参数

| 参数名   | 必须 | 类型 | 说明     |
| -------- | ---- | ---- | -------- |
| id       | 是   | num  | 用户 id  |
| page     | 是   | num  | 第几页   |
| pagesize | 是   | num  | 每页条数 |

- 返回示例

```javascript
{
  "success": true,
  "message": "ok",
  "data":{
    "total": 59,
    "list": [
      {
        "id": 111,
        "name": "一诺",
        "avatar": "http://cdn.juliancj.com/1544510612386.jpg",
        "sex": 1,
        "introduction": "区块链信仰者",
        "feature": "",
        "auth": 1,
        "grade": 1,
        "score": 0,
        "recommend": 1,
        "status": 1,
        "articleCount": 1431,
        "pageViewSum": 26137722,
        "fensSum":1665,
        "isFollowed": null
      },
      // ...
    ]
  }
}
```

- 返回参数说明

| 参数名       | 类型 | 说明                                                                                             |
| ------------ | ---- | ------------------------------------------------------------------------------------------------ |
| id           | num  | 作者 id                                                                                          |
| name         | str  | 作者名称                                                                                        |
| avatar       | str  | 作者头像                                                                                         |
| sex          | num  | 作者性别（1 女性 ,2 男性）                                                                       |
| introduction | str  | 作者简介                                                                                         |
| feature      | str  | 作者特点                                                                                         |
| auth         | num  | 作者认证状态 （0 未认证,1 个人认证, 2 企业认证, -1 认证未通过, 3 申请个人认证, 4 申请企业认证 ） |
| user.grade   | num  | 作者等级（目前 1 - 39）                                                                          |
| score        | num  | 作者积分                                                                                         |
| recommend    | num  | 作者是否推荐（ 0 否，1 是）                                                                      |
| status       | num  | 作者状态（ -2 删除, -1 黑名单, 0 暂停使用, 1 可用）                                              |
| articleCount | num  | 作者文章数                                                                                       |
| pageViewSum  | num  | 作者浏览数                                                                                       |
| fensSum      | num  | 作者粉丝数                                                                                        |
| isFollowed   | boo  | 登录用户是否关注（true 已关注, false 未关注）                                                    |

- 备注
  - 暂无

#### 10.4.3.关注用户

- 描述

  - 关注用户

- 请求 URL

  - `api/v2/user/follow`

- 请求方式

  - `POST`

- 参数

| 参数名 | 必须 | 类型 | 说明          |
| ------ | ---- | ---- | ------------- |
| fromId | 是   | num  | 用户 id       |
| toId   | 是   | num  | 被关注用户 id |

- 返回示例

```javascript
{
  "success": true,
  "message": "ok",
  "data": 1
}
```

- 返回参数说明

| 参数名 | 类型 | 说明           |
| ------ | ---- | -------------- |
| data   | num  | 1 成功，2 失败 |

- 备注
  - 暂无

#### 10.4.4.删除关注用户

- 描述

  - 删除关注用户

- 请求 URL

  - `api/v2/user/follow`
    <!-- - `api/v2/user/follow/delete` -->

- 请求方式

  - `DELETE`
    <!-- - `POST` -->

- 参数

| 参数名 | 必须 | 类型 | 说明          |
| ------ | ---- | ---- | ------------- |
| fromId | 是   | num  | 用户 id       |
| toId   | 是   | num  | 被关注用户 id |

- 返回示例

```javascript
{
  "success": true,
  "message": "ok",
  "data": 1
}
```

- 返回参数说明

| 参数名 | 类型 | 说明           |
| ------ | ---- | -------------- |
| data   | num  | 1 成功，2 失败 |

- 备注
  - 暂无

### 10.5.点赞

- 描述

  - 用户点赞或取赞

- 请求 URL

  - `api/v2/likeDislike`

- 请求方式

  - `POST`

- 参数

| 参数名    | 必须 | 类型 | 说明                                                               |
| --------- | ---- | ---- | ------------------------------------------------------------------ |
| userId    | 是   | num  | 用户 id                                                            |
| topicId   | 是   | num  | 点赞对象 id                                                        |
| topicType | 是   | num  | 点赞对象类型（1 咨询文章 2 项目文章 3 福利文章 4 评论 5 评论回复） |
| type      | 是   | num  | 类型（1 点赞 2 点踩）                                              |
| status    | 是   | num  | 状态（0 不可用 1 可用）                                            |

- 返回示例

```javascript
{
  "success": true,
  "message": "ok",
  "data": 1
}
```

- 返回参数说明

| 参数名 | 类型 | 说明           |
| ------ | ---- | -------------- |
| data   | num  | 1 成功，2 失败 |

- 备注
  - 暂无

### 10.6.我的草稿箱

#### 10.6.1.获取草稿

- 描述

  - 根据分类 id 获取不同类型文章草稿

- 请求 URL

  - `api/v2/user/id/draft?type=1&page=1&pagesize=10`

- 请求方式

  - `GET`

- 参数

| 参数名   | 必须 | 类型 | 说明                             |
| -------- | ---- | ---- | -------------------------------- |
| id       | 是   | num  | 用户 id                          |
| type     | 是   | num  | 文章类型（1 咨询 2 项目 3 福利） |
| page     | 是   | num  | 第几页                           |
| pagesize | 是   | num  | 每页条数                         |

- 返回示例

```javascript
{
  "success": true,
  "message": "ok",
  "data": {
    "total":426,
    "list":[
      {
        "id": 6400,
        "title": "币江南：1.28比特币行情解读之江南说年（一）",
        "banner": "http://cdn.juliancj.com/Fj79bTYiIF9EhOkhnrrkbjV7drJs",
        "introduction": "财富不应当是生命的目的，它只是生活的工具。挡不住今天的诱惑，就会失去明天的幸福!",
        "pageView": 3374,
        "source": 1,
        "recommend": 1,
        "likeNumber": 3374,
        "collection": 3374,
        "status": 1,
        "createTime": 1548647116433,
        "updateTime": 1548647116433,
        "category": {
          "id": 2,
          "name": "深度",
          "articles": null
        },
      },
      // ...
    ]
  }
}
```

- 返回参数说明

| 参数名        | 类型 | 说明                                                              |
| ------------- | ---- | ----------------------------------------------------------------- |
| id            | num  | 文章 id                                                           |
| title         | str  | 文章标题                                                          |
| banner        | str  | 文章封面                                                          |
| introduction  | str  | 文章简介                                                          |
| pageView      | num  | 文章浏览量                                                        |
| source        | num  | 文章来源（1 原创; 2 转载）                                        |
| recommend     | num  | 文章推荐（0 不推荐; 1 推荐）                                      |
| likeNumber    | num  | 文章点赞量                                                        |
| collection    | num  | 文章收藏量                                                        |
| status        | num  | 文章状态（-3 下线; -2 审核未通过; -1 草稿; 0 待审核; 1 审核通过） |
| createTime    | num  | 创建时间                                                          |
| updateTime    | num  | 最后修改时间                                                      |
| category      | obj  | 文章分类信息                                                      |
| category.id   | num  | 文章分类 id                                                       |
| category.name | str  | 文章分类名称                                                           |

- 备注
  - 暂无

#### 10.6.2.存草稿

- 描述

  - 用户存草稿

- 请求 URL

  - `api/v2/user/draft`

- 请求方式

  - `POST`

- 参数

| 参数名       | 必须 | 类型 | 说明                             |
| ------------ | ---- | ---- | -------------------------------- |
| userId       | 是   | num  | 用户 id                          |
| type         | 是   | num  | 文章类型（1 咨询 2 项目 3 福利） |
| cid          | 是   | num  | 文章 id                          |
| categoryId   | 是   | num  | 文章分类 id                      |
| title        | 是   | str  | 文章标题                         |
| banner       | 是   | str  | 文章封面                         |
| introduction | 是   | str  | 文章简介                         |
| content      | 是   | str  | 文章内容                         |
| source       | 是   | num  | 文章来源                         |
| keywordIds   | 是   | str  | 关键词 id，以半角逗号隔开        |

- 返回示例

```javascript
{
  "success": true,
  "message": "ok",
  "data": 1
}
```

- 返回参数说明

| 参数名 | 类型 | 说明           |
| ------ | ---- | -------------- |
| data   | num  | 1 成功，2 失败 |

- 备注
  - 暂无

#### 10.6.2.删除草稿

- 描述

  - 删除用户草稿(批量删除？？？)

- 请求 URL

  - `api/v2/user/draft`

- 请求方式

  - `DELETE`

- 参数

| 参数名 | 必须 | 类型 | 说明                             |
| ------ | ---- | ---- | -------------------------------- |
| userId | 是   | num  | 用户 id                          |
| type   | 是   | num  | 文章类型（1 咨询 2 项目 3 福利） |
| cid    | 是   | num  | 文章 id                          |

- 返回示例

```javascript
{
  "success": true,
  "message": "ok",
  "data": 1
}
```

- 返回参数说明

| 参数名 | 类型 | 说明           |
| ------ | ---- | -------------- |
| data   | num  | 1 成功，2 失败 |

- 备注
  - 暂无

## 11.消息

### 11.1.获取消息列表

- 描述

  - 获取不同类型消息列表

- 请求 URL

  - `api/v2/message?type=1&page=1&pagesize=10`

- 请求方式

  - `GET`

- 参数

| 参数名   | 必须 | 类型 | 说明                                           |
| -------- | ---- | ---- | ---------------------------------------------- |
| type     | 是   | num  | 消息类型（1 审核消息, 2 积分消息, 3 推送消息） |
| page     | 是   | num  | 第几页                                         |
| pagesize | 是   | num  | 每页条数                                       |

- 返回示例

```javascript
{
  "success":true,
  "message":"ok",
  "data":{
    "total":12,
    "list":[
      {
        "id": 1,
        "content": "亲爱的'会笑的韭菜'：您的实名审核已通过，将于12月28日生效，请尽快查看并及时处理。",
        "status": 1
      },
      // ...
    ]
  }
}
```

- 返回参数说明

| 参数名  | 类型 | 说明                       |
| ------- | ---- | -------------------------- |
| id      | num  | 消息 id                    |
| content | str  | 消息内容                   |
| status  | num  | 状态（1 未阅读, 2 已阅读） |

- 备注
  - 暂无

### 11.2.消息设置

- 描述

  - 设置消息提示

- 请求 URL

  - `api/v2/message?type=1`

- 请求方式

  - `PUT`

- 参数

| 参数名 | 必须 | 类型 | 说明                                           |
| ------ | ---- | ---- | ---------------------------------------------- |
| type   | 是   | num  | 消息类型（1 审核消息, 2 积分消息, 3 推送消息） |
| push   | 是   | boo  | 是否开启(true 开启消息, false 关闭消息)        |

- 返回示例

```javascript
{
  "success": true,
  "message": "ok",
  "data": 1
}
```

- 返回参数说明

| 参数名 | 类型 | 说明           |
| ------ | ---- | -------------- |
| data   | num  | 1 成功，2 失败 |

- 备注
  - 暂无
