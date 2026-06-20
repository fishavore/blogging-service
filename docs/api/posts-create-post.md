---
# markdownlint-disable
# vale off
layout: default
title: Create a post
description: POST a post resource to the service
topic_type: reference
tags: api
categories: api-reference
ai_relevance: high
# importance: 7
prerequisites:
    - /api/post
    - /api/blog
related_pages: []
examples: POST /post
test:
    test_apps: json-server@0.17.4
    server_url: localhost:3000
    local_database: /api/blogging-service.json
    testable: POST example / 201
api_endpoints: /posts
version: "v1.0"
last_updated: "2026-06-19"
# vale  on
# markdownlint-enable
---

<!-- markdownlint-disable MD025 -->

# Create a post

<!-- markdownlint-enable MD025 -->

Sends a [`post`](post.md) object to store the details of the new post resource
in the service. The new post is for a registered user of the service.

[Jump to examples](#examples)

## Endpoint

```shell
{server_url}/posts
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
    "title": "Fruit",
    "content": "Cotton Candy grapes tasted like soy sauce",
    "postedDate": "2026-06-02T14:00",
    "private": true,
    "blogId": 2,
    "category": "food",
    "commentIds": []
}
```

## Response body

Returns a [`post` resource](post.md)

## Examples

### `POST` example request

```bash
curl -H 'content-type: application/json' \
    --url http://localhost:3000/posts \
    -d '{
            "title": "Fruit",
            "content": "Cotton Candy grapes tasted like soy sauce",
            "postedDate": "2026-06-02T14:00",
            "private": true,
            "blogId": 2,
            "category": "food",
            "commentIds": []
        }'
```

#### `POST` example response

```json
{
    "title": "Fruit",
    "content": "Cotton Candy grapes tasted like soy sauce",
    "postedDate": "2026-06-02T14:00",
    "private": true,
    "blogId": 2,
    "category": "food",
    "commentIds": [],
    "id": 3
}
```

## Response status

| HTTP status value | Description |
| ------------- | ----------- |
| 201 | **Success:** Task resource created successfully |
| 400 | **Error:** Malformed request not processed. Verify syntax and try again. |
| 500 | **Error:** Server rejected the data. Verify data and try again. |
| 000 | **not**: Done yet |
