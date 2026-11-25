# Threads Profile API

Fetch a public Threads profile and its latest posts with likes, replies, reposts and media as JSON.

Powered by [Serpent API](https://apiserpent.com). Full reference: **[Threads Profile API docs](https://apiserpent.com/threads-api)**.

## Quick start

1. Get an API key at [apiserpent.com](https://apiserpent.com). Every account starts with 10 free API calls.
2. Call the endpoint with your key in the `X-API-Key` header:

```bash
curl -G "https://apiserpent.com/api/threads/profile" \
  --data-urlencode "username=nasa" \
  -H "X-API-Key: $SERPENT_API_KEY"
```

## Endpoint

`GET https://apiserpent.com/api/threads/profile`

| Parameter | Required | Description |
| --- | --- | --- |
| `username` | Yes | Public Threads username, with or without `@`, or a threads.com link |

## Response

`success`, `username`, `full_name`, `biography`, `followers`, `is_verified`, `profile_pic_url`, `bio_links[]`, `profile_url`, `posts[]`. Each post has `id`, `url`, `date`, `text`, `likes`, `replies`, `reposts`, `quotes`, `is_pinned`, `images[]`, `videos[]`.

See the [docs](https://apiserpent.com/threads-api) for the complete field list and sample responses.

## Examples

| File | Language | Run |
| --- | --- | --- |
| [`example.py`](example.py) | Python 3 (`pip install requests`) | `SERPENT_API_KEY=sk_live_... python example.py` |
| [`example.mjs`](example.mjs) | Node.js 18+ (no dependencies) | `SERPENT_API_KEY=sk_live_... node example.mjs` |

## Use cases

- Influencer and brand monitoring
- Social analytics dashboards
- Engagement benchmarking

## More from Serpent API

- [Serpent API docs](https://apiserpent.com/docs) - Google, Bing, Yahoo, DuckDuckGo and Brave search, plus AI rank tracking
- [All SDKs and tools on GitHub](https://github.com/apiserpent)

## License

MIT
