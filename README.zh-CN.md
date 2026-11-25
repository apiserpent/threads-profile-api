[English](README.md) | **简体中文**

# Threads 主页 API

获取公开的 Threads 主页及其最新帖子，以 JSON 返回点赞、回复、转发和媒体信息。

由 [Serpent API](https://apiserpent.com) 提供。完整文档：**[Threads Profile API 文档](https://apiserpent.com/threads-api)**。

## 快速开始

1. 在 [apiserpent.com](https://apiserpent.com) 注册并获取 API Key，每个账号赠送 10 次免费调用。
2. 在请求头 `X-API-Key` 中带上你的 Key 调用接口：

```bash
curl -G "https://apiserpent.com/api/threads/profile" \
  --data-urlencode "username=nasa" \
  -H "X-API-Key: $SERPENT_API_KEY"
```

## 接口

`GET https://apiserpent.com/api/threads/profile`

| 参数 | 必填 | 说明 |
| --- | --- | --- |
| `username` | 是 | 公开的 Threads 用户名，可带或不带 `@`，也可以是 threads.com 链接 |

## 返回结果

顶层字段：`success`、`username`、`full_name`、`biography`、`followers`、`is_verified`、`profile_pic_url`、`bio_links[]`、`profile_url`、`posts[]`。每条帖子包含 `id`、`url`、`date`、`text`、`likes`、`replies`、`reposts`、`quotes`、`is_pinned`、`images[]`、`videos[]`。

完整字段列表和响应示例请参阅[文档](https://apiserpent.com/threads-api)。

## 示例代码

| 文件 | 语言 | 运行方式 |
| --- | --- | --- |
| [`example.py`](example.py) | Python 3（`pip install requests`） | `SERPENT_API_KEY=sk_live_... python example.py` |
| [`example.mjs`](example.mjs) | Node.js 18+（无需依赖） | `SERPENT_API_KEY=sk_live_... node example.mjs` |

## 应用场景

- 达人与品牌监控
- 社交媒体数据看板
- 互动数据对标分析

## Serpent API 的更多能力

- [Serpent API 文档](https://apiserpent.com/docs)：Google、Bing、Yahoo、DuckDuckGo 和 Brave 搜索结果，以及 AI 引用排名跟踪
- [GitHub 上的全部 SDK 与工具](https://github.com/apiserpent)

## 许可证

MIT
