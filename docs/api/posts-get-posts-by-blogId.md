---
# markdownlint-disable
# vale off
layout: default
title: Get posts by blog ID
description: Get the post resources with the specified blog ID from the service
topic_type: reference
tags: api
categories: api-reference
ai_relevance: high
# importance: 7
prerequisites:
    - /api/post
    - /api/blog
related_pages: []
examples: GET /posts/?blogId={blogId}
test:
    test_apps: json-server@0.17.4
    server_url: localhost:3000
    local_database: /api/blogging-service.json
    testable: GET example / 200
api_endpoints: GET /posts
version: "v1.0"
last_updated: "2026-06-19"
# vale  on
# markdownlint-enable
---

<!-- markdownlint-disable MD025 -->

# Get posts by blog ID

<!-- markdownlint-enable MD025 -->

Returns an array of  [`post`](post.md) objects that contains only the blog
specified by the `blogId` parameter, if it exists.

[Jump to examples](#examples)

## Endpoint

```shell
{server_url}/posts/?blogId={blogId}
```

## Parameters

| Name | Type | Value | Description |
| ----- | ------ | ------ | ------------ |
| `blogId` | URL | number | The record ID of the `blog` resource to return @??@ |

## Request headers

| Header | Value | Required |
| ------ | ----- | -------- |
| `Accept` | `application/json` | No |

## Request body

None

## Response body

Returns a [`post` resource](post.md)

## Examples

### `GET` example request

```bash
curl -G -H "Accept: application/json" \
    --url "http://localhost:3000/posts/?blogId=2"
```

#### `GET` example response

```json
[
    {
        "id": 2,
        "title": "Fruit",
        "content": "Cotton Candy grapes tasted like soy sauce",
        "postedDate": "2026-06-02T14:00",
        "private": true,
        "blogId": 2,
        "category": "food",
        "commentIds": [
            1,
            2
        ]
  }
]
```

## Response status

| HTTP status value | Description |
| ------------- | ----------- |
| 200 | **Success**: Requested data returned successfully |
| 404 | **Error**: Specified user record not found |
| 000 | **not**: Done yet |
