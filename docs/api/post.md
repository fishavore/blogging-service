---
# markdownlint-disable
# vale off
layout: default
title: Post resource
description: Information about the post resource
topic_type: reference
tags: api
categories: api-reference
ai_relevance: high
# importance: 8
prerequisites: []
related_pages: /tutorials/posts-update-post
examples: []
api_endpoints: /posts
version: "v1.1"
last_updated: "2026-06-24"
# vale  on
# markdownlint-enable
---

<!-- markdownlint-disable MD025 -->

# Post resource

<!-- markdownlint-enable MD025 -->

Base endpoint:

```shell
{base_url}/posts
```

Contains information about posts stored for the users of the service.

To have a post in the service, the user must be in the service and have created
their blog first.

Learn more about the [`user` resource](user.md) and [`blog` resource](blog.md).

## Resource properties

Example `post` resource

```json
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
```

<!-- vale Google.Acronyms = NO -->

| Property name | Type | Description |
| ------------- | ----------- | ----------- |
| `id` | number | The ID of the `post` resource |
| `title` | string | The title or short description of the post |
| `content` | string | The content of this post |
| `postedDate` | string | The [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601) format of the post's date and time |
| `private` | boolean | The visibility of the post content. Set this to false to make the post public. |
| `blogId` | number | The blog's unique record ID |
| `category` | string | The label to categorize the post |
| `commentIds` | array of numbers | The IDs of the `comment` resources associated with this post |

## Read operations

* [Get posts by blog ID](posts-get-posts-by-blogId.md)

## Write operations

* [Create a post](posts-create-post.md)
* [Replace a post](posts-replace-post.md)

<!-- markdownlint-disable MD033 -->

<div style="text-align: right;">| <a href="https://fishavore.github.io/blogging-service/">Home</a> | <a href="https://fishavore.github.io/blogging-service/api/reference.html">Reference</a> | <a href="https://fishavore.github.io/blogging-service/tutorials/tutorial.html">Tutorials</a> |</div>
