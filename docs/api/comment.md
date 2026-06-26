---
# markdownlint-disable
# vale off
layout: default
title: Comment resource
description: Information about the comment resource
topic_type: reference
tags: api
categories: api-reference
ai_relevance: high
# importance: 8
prerequisites: []
related_pages:
    - /tutorials/comments-add-comment
    - /tutorials/comments-delete-comment
examples: []
api_endpoints: /comments
version: "v1.1"
last_updated: "2026-06-24"
# vale  on
# markdownlint-enable
---

<!-- markdownlint-disable MD025 -->

# Comment resource

<!-- markdownlint-enable MD025 -->

Base endpoint:

```shell
{base_url}/comments
```

Contains information about comments stored for the users of the service and
anonymous commenters.

To add a comment in the service, the blog and post must already be in the
service.

Anybody can add a comment in the service. To have a comment that's associated
with a user in the service, the user must be in the service first. Use
`Anonymous` for the `userName` property when the new comment isn't associated
with any user in the service.

Learn more about the [`user` resource](user.md), [`blog` resource](blog.md), and
[`post` resource](post.md).

## Resource properties

Example `comment` resource

```json
{
    "id": 2,
    "content": "Where did you find them?",
    "postedDate": "2026-06-05T14:00",
    "postId": 2,
    "userName": "connoisseur"
}
```

<!-- vale Google.Acronyms = NO -->

| Property name | Type | Description |
| ------------- | ----------- | ----------- |
| `id` | number | The ID of the `comment` resource |
| `content` | string | The content of this comment |
| `postedDate` | string | The [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601) format of the comment's date and time |
| `postId` | number | The ID of the `post` resource associated with this comment |
| `userName` | string | The user's identification name in the service. `Anonymous` means that the commenter isn't a user of the service |

## Read operations

* [Get comments by post ID](comments-get-comments-by-postId.md)

<!-- markdownlint-disable MD033 -->

<div style="text-align: right;">| <a href="https://fishavore.github.io/blogging-service/">Home</a> | <a href="https://fishavore.github.io/blogging-service/api/reference.html">Reference</a> | <a href="https://fishavore.github.io/blogging-service/tutorials/tutorial.html">Tutorials</a> |</div>
