---
# markdownlint-disable
# vale off
layout: default
description: Information about the `post` resource
topic_type: reference
tags: api
categories: api-reference
ai_relevance: high
# importance: 8
prerequisites: []
related_pages: []
#    - /tutorials/add-a-new-task
examples: []
api_endpoints: /posts
version: "v1.0"
last_updated: "2026-06-16"
# vale  on
# markdownlint-enable
---

# `post` resource

Base endpoint:

```shell
{server_url}/posts
```

<!-- vale write-good = NO -->
<!-- vale Google.Passive = NO -->

Contains information about posts stored for the users of the service.

To have a post in the service, the user must be added to the service and have
created their blog first. Learn more about the [user resource](user.md) and
[blog resource](blog.md).

## Resource properties

Sample `post` resource

```json
{
    "postId": 2,
    "title": "Fruit",
    "content": "Cotton Candy grapes tasted like soy sauce",
    "postedDate": "2026-06-02T14:00",
    "private": true,
    "blogId": 2,
    "category": "food",
    "commentIds": [1, 2]
}
```

<!-- vale Google.Acronyms = NO -->

| Property name | Type | Description |
| ------------- | ----------- | ----------- |
| `postId` | number | The ID of the post resource to which this post is assigned |
| `title` | string | The title or short description of the post |
| `content` | string | The content of this post |
| `postedDate` | string | The [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601) format of the date and time the post is posted |
| `private` | boolean | The visibility of the post content. Set this to false to make the post public. |
| `blogId` | number | The blog's unique record ID |
| `category` | string | The label to categorize the post |
| `commentIds` | array of numbers | The IDs of the comment resources associated with this post |

## Read operations

<!-- vale Google.Parens = NO -->

* [Get all tasks _(coming soon)_](#resource-properties)
* [Get task by ID _(coming soon)_](#resource-properties)
* [Get task by user ID _(coming soon)_](#resource-properties)
