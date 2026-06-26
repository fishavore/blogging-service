---
# markdownlint-disable
# vale off
layout: default
title: Blog resource
description: Information about the blog resource
topic_type: reference
tags: api
categories: api-reference
ai_relevance: high
# importance: 8
prerequisites: []
related_pages: []
examples: []
api_endpoints: /blogs
version: "v1.1"
last_updated: "2026-06-24"
# vale on
# markdownlint-enable
---

<!-- markdownlint-disable MD025 -->

# Blog resource

<!-- markdownlint-enable MD025 -->

Base endpoint:

```shell
{base_url}/blogs
```

Contains information about blogs stored for the users of the service. A blog is
a collection of posts.

To have a blog in the service, the user must be in the service first.

Learn more about the [`user` resource](user.md).

## Resource properties

Example `blog` resource

```json
{
    "id": 2,
    "title": "Adventures in food",
    "userId": 2
}
```

| Property name | Type | Description |
| ------------- | ----------- | ----------- |
| `id` | number | The blog's unique record ID |
| `title` | string | The title or short description of the blog |
| `userId` | number | The ID of the `user` resource for this blog |

## Read operations

* [Get all blogs](blogs-get-all-blogs.md)

## Write operations

* [Create a blog](blogs-create-blog.md)

<!-- markdownlint-disable MD033 -->

<div style="text-align: right;">| <a href="https://fishavore.github.io/blogging-service/">Home</a> | <a href="https://fishavore.github.io/blogging-service/api/reference.html">Reference</a> | <a href="https://fishavore.github.io/blogging-service/tutorials/tutorial.html">Tutorials</a> |</div>
