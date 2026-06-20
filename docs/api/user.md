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
related_pages: []
#    - /tutorials/enroll-a-new-user
examples: []
api_endpoints: /users
version: "v1.0"
last_updated: "2026-06-16"
# vale  on
# markdownlint-enable
---

<!-- markdownlint-disable MD025 -->

# User resource

<!-- markdownlint-enable MD025 -->

Base endpoint:

```shell
{server_url}/users
```

Contains information about the users of the service.

A `user` resource describes the owners of the blogs, posts, and/or comments in
the service. Before you can create a `blog` resource in the service, you must
create a `user` resource to assign to the `blog`.

Learn more about the [blog resource](blog.md).

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

* [Get all users _(coming soon)_](users-get-all-users.md)
* [Get users by ID _(coming soon)_](users-get-user-by-id.md)
