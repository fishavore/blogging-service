---
# markdownlint-disable
# vale off
layout: default
title: Create a blog
description: Post a blog resource to the service
topic_type: reference
tags: api
categories: api-reference
ai_relevance: high
# importance: 7
prerequisites: /api/blog
related_pages: []
examples: POST /blog
test:
    test_apps: json-server@0.17.4
    server_url: localhost:3000
    local_database: /api/blogging-service.json
    testable: POST example / 201
api_endpoints: /blogs
version: "v1.0"
last_updated: "2026-06-19"
# vale  on
# markdownlint-enable
---

<!-- markdownlint-disable MD025 -->

# Create a blog

<!-- markdownlint-enable MD025 -->

Sends a [`blog`](blog.md) object to store the details of the new blog resource
in the service. The new blog is for a registered user of the service.

[Jump to examples](#examples)

## Endpoint

```shell
{server_url}/blogs
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
    "title": "Adventures in food 2",
    "userId": 2
}
```

## Response body

Returns a [`blog` resource](blog.md)

## Examples

### `POST` example request

```shell
curl -H 'content-type: application/json' \
    --url http://localhost:3000/blogs \
    -d '{
            "title": "Adventures in food 2",
            "userId": 2
        }'
```

#### `POST` example response

```json
{
    "title": "Adventures in food 2",
    "userId": 2,
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
