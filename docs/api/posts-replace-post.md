---
# markdownlint-disable
# vale off
layout: default
title: Replace a post
description: Replace a post resource in the service
topic_type: reference
tags: api
categories: api-reference
ai_relevance: high
# importance: 7
prerequisites: /api/post
related_pages: []
examples: PUT /posts/{id}
test:
    test_apps: json-server@0.17.4
    server_url: localhost:3000
    local_database: /api/blogging-service.json
    testable: PUT example / 201
api_endpoints: /posts
version: "v1.0"
last_updated: "2026-06-19"
# vale  on
# markdownlint-enable
---

<!-- markdownlint-disable MD025 -->

# Replace a post

<!-- markdownlint-enable MD025 -->

Sends a [`post`](post.md) object to replace the details of the post resource in
the service. The post task is for a registered user of the service.

[Jump to examples](#examples)

## Endpoint

```shell
{server_url}/posts/{id}
```

## Parameters

None

## Request headers

| Header | Value | Required |
| ------ | ----- | -------- |
| `content-type` | `application/json` | Yes |

## Request body

```json
{
    "id": 1,
    "title": "Nikka whiskey 2026 review",
    "content": "Coffey Malt: Good, 8 out of 10",
    "postedDate": "2026-06-03T17:00",
    "private": false,
    "blogId": 1,
    "category": "drink",
    "commentIds": []
}
```

## Response body

Returns a [`post` resource](post.md)

## Examples

### `PUT` example request

```bash
curl -X PUT -H 'content-type: application/json' \
    --url http://localhost:3000/posts/1 \
    -d '{
            "title": "Nikka whiskey 2026 review",
            "content": "Coffey Malt: Good, 8 out of 10",
            "postedDate": "2026-06-03T17:00",
            "private": false,
            "blogId": 1,
            "category": "drink",
            "commentIds": []
        }'
```

#### `PUT` example response

```json
{
    "title": "Nikka whiskey 2026 review",
    "content": "Coffey Malt: Good, 8 out of 10",
    "postedDate": "2026-06-03T17:00",
    "private": false,
    "blogId": 1,
    "category": "drink",
    "commentIds": [],
    "id": 1
  }
```

## Response status

| HTTP status value | Description |
| ------------- | ----------- |
| 201 | **Success:** Task resource created successfully |
| 400 | **Error:** Malformed request not processed. Verify syntax and try again. |
| 500 | **Error:** Server rejected the data. Verify data and try again. |
| 000 | **not**: Done yet |
