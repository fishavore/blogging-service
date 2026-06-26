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
    base_url: localhost:3000
    local_database: /api/blogging-service.json
    testable: GET example / 200
api_endpoints: GET /posts
version: "v1.1"
last_updated: "2026-06-24"
# vale  on
# markdownlint-enable
---

<!-- markdownlint-disable MD025 -->

# Get posts by blog ID

<!-- markdownlint-enable MD025 -->

Returns an array of [`post`](post.md) objects that belong to the blog specified
by the `blogId` parameter, if it exists.

Jump to [examples](#examples)

## Endpoint

```shell
{base_url}/posts/?blogId={blogId}
```

## Parameters

| Name | Type | Value | Description |
| ----- | ------ | ------ | ------------ |
| `blogId` | URL | number | The record ID of the `blog` resource |

## Request headers

| Header | Value | Required |
| ------ | ----- | -------- |
| `Accept` | `application/json` | No |

## Request body

None

## Response body

Returns an array of [`post` resources](post.md).

## Examples

### `GET` example request

```shell
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
| 200 | **OK:** Resource found and returned |
| 404 | **Not Found**: Resource doesn't exist |

<!-- markdownlint-disable MD033 -->

<div style="text-align: right;">| <a href="https://fishavore.github.io/blogging-service/">Home</a> | <a href="https://fishavore.github.io/blogging-service/api/reference.html">Reference</a> | <a href="https://fishavore.github.io/blogging-service/tutorials/tutorial.html">Tutorials</a> |</div>
