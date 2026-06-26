---
# markdownlint-disable
# vale off
layout: default
title: Get all blogs
description: Get all blog resources from the service
topic_type: reference
tags: api
categories: api-reference
ai_relevance: high
# importance: 7
prerequisites: /api/blog
related_pages: []
examples: GET /blogs
test:
    test_apps: json-server@0.17.4
    base_url: localhost:3000
    local_database: /api/blogging-service.json
    testable: GET example
api_endpoints: /blogs
version: "v1.1"
last_updated: "2026-06-24"
# vale  on
# markdownlint-enable
---

<!-- markdownlint-disable MD025 -->

# Get all blogs

<!-- markdownlint-enable MD025 -->

Returns an array of [`blog`](blog.md) objects that contains all blogs that have
created with the service.

Jump to [examples](#examples)

## Endpoint

```shell
{base_url}/blogs
```

## Parameters

None

## Request headers

| Header | Value | Required |
| ------ | ----- | -------- |
| `Accept` | `application/json` | No |

## Request body

None

## Response body

```json
[
    {
        "id": 1,
        "title": "Peated whiskey",
        "userId": 1
    },
    {
        "id": 2,
        "title": "Adventures in food",
        "userId": 2
    }
]
```

## Examples

### `GET` example request

```shell
curl -G -H "Accept: application/json" --url "http://localhost:3000/blogs"
```

#### `GET` example response

```json
[
    {
        "id": 1,
        "title": "Peated whiskey",
        "userId": 1
    },
    {
        "id": 2,
        "title": "Adventures in food",
        "userId": 2
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
