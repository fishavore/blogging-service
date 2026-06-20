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
related_pages: []
#    - /tutorials/add-a-new-task
examples: []
api_endpoints: /comments
version: "v1.0"
last_updated: "2026-06-17"
# vale  on
# markdownlint-enable
---

<!-- markdownlint-disable MD025 -->

# Comment resource

<!-- markdownlint-enable MD025 -->

Base endpoint:

```shell
{server_url}/comments
```
<!-- vale write-good = NO -->
<!-- vale Google.Passive = NO -->

Contains information about comments stored for the users of the service and
anonymous commenters.

Anybody can add a comment in the service. To have a comment that's associated
with a user in the service, the user must be added to the service first.
Learn more about the [user resource](user.md).

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
| `postedDate` | string | The [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601) format of the date and time the comment is posted |
| `postId` | number | The ID of the `post` resource associated with this comment |
| `userName` | string | The user's identification name in the service. `Anonymous` is used if the commenter isn't a user of the service |

## Read operations

* [Get comments by post ID](comments-get-comments-by-postId.md)
