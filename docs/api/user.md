---
# markdownlint-disable
# vale off
layout: default
title: User resource
description: Information about the user resource
topic_type: reference
tags: api
categories: api-reference
ai_relevance: high
# importance: 8
prerequisites: []
related_pages: /tutorials/users-add-user
examples: []
api_endpoints: /users
version: "v1.1"
last_updated: "2026-06-24"
# vale  on
# markdownlint-enable
---

<!-- markdownlint-disable MD025 -->

# User resource

<!-- markdownlint-enable MD025 -->

Base endpoint:

```shell
{base_url}/users
```

Contains information about the users of the service.

A `user` resource describes the owners of the blogs, posts, and/or comments in
the service. Before you can create a `blog` resource in the service, you must
create a `user` resource to assign to the blog.

Learn more about the [`blog` resource](blog.md).

## Resource properties

Example `user` resource

```json
{
    "id": 2,
    "userName": "foodie",
    "lastName": "Millikan",
    "firstName": "Amelia"
}
```

| Property name | Type | Description |
| ------------- | ----------- | ----------- |
| `id` | number | The user's unique record ID |
| `userName` | string | The user's identification name in the service |
| `lastName` | string | The user's last name |
| `firstName` | string | The user's first name |

## Tutorials

* [Add a user](../tutorials/users-add-user.md)

<!-- markdownlint-disable MD033 -->

<div style="text-align: right;">| <a href="https://fishavore.github.io/blogging-service/">Home</a> | <a href="https://fishavore.github.io/blogging-service/api/reference.html">Reference</a> | <a href="https://fishavore.github.io/blogging-service/tutorials/tutorial.html">Tutorials</a> |</div>
