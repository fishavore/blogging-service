---
# markdownlint-disable
# vale off
layout: default
title: Get comments by post ID
description: Get the comment resources with the specified post ID from the service
topic_type: reference
tags: api
categories: api-reference
ai_relevance: high
# importance: 7
prerequisites:
    - /api/comment
    - /api/post
related_pages: []
examples: GET /comments/?postId={postId}
test:
    test_apps: json-server@0.17.4
    server_url: localhost:3000
    local_database: /api/blogging-service.json
    testable: GET example / 200
api_endpoints: GET /comments
version: "v1.1"
last_updated: "2026-06-24"
# vale  on
# markdownlint-enable
---

<!-- markdownlint-disable MD025 -->

# Get comments by post ID

<!-- markdownlint-enable MD025 -->

Returns an array of  [`comment`](comment.md) objects that contains only the
user specified by the `postId` parameter, if it exists.

Jump to [examples](#examples)

## Endpoint

```shell
{base_url}/comments/?postId={postId}
```

## Parameters

| Name | Type | Value | Description |
| ----- | ------ | ------ | ------------ |
| `postId` | URL | number | The record ID of the `post` resource to return @??@ |

## Request headers

| Header | Value | Required |
| ------ | ----- | -------- |
| `Accept` | `application/json` | No |

## Request body

None

## Response body

Returns a [`comment` resource](comment.md).

## Examples

### `GET` example request

```shell
curl -G -H "Accept: application/json" \
    --url "http://localhost:3000/comments/?postId=2"
```

#### `GET` example response

```json
[
    {
        "id": 1,
        "content": "Mine tasted great",
        "postedDate": "2026-06-04T17:00",
        "postId": 2,
        "userName": "Anonymous"
    },
    {
        "id": 2,
        "content": "Where did you find them?",
        "postedDate": "2026-06-05T14:00",
        "postId": 2,
        "userName": "connoisseur"
    }
]
```

## Response status

| HTTP status value | Description |
| ------------- | ----------- |
| 200 | **OK:** Resource found and returned |
| 404 | **Not Found**: Resource doesn't exist |
