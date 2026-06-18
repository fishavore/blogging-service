---
# markdownlint-disable
# vale off
layout: default
description: Information about the `blog` resource
topic_type: reference
tags: api
categories: api-reference
ai_relevance: high
# importance: 8
prerequisites: []
related_pages: []
#    - /tutorials/add-a-new-task
examples: []
api_endpoints: /blogs
version: "v1.0"
last_updated: "2026-06-16"
# vale on
# markdownlint-enable
---

# `blog` resource

Base endpoint:

```shell
{server_url}/blogs
```

<!-- vale write-good = NO -->
<!-- vale Google.Passive = NO -->

Contains information about blogs stored for the users of the service. A blog is
a collection of posts.

To have a blog in the service, the user must be added to the service first. Learn
more about the [user resource](user.md).

## Resource properties

Sample `blog` resource

```json
{
    "blogId": 2,
    "title": "Adventures in food",
    "userId": 2
}
```

| Property name | Type | Description |
| ------------- | ----------- | ----------- |
| `blogId` | number | The blog's unique record ID |
| `title` | string | The title or short description of the blog |
| `userId` | number | The ID of the user resource to which this blog is assigned |

## Read operations

<!-- vale Google.Parens = NO -->

* [Get all tasks _(coming soon)_](#resource-properties)
* [Get task by ID _(coming soon)_](#resource-properties)
* [Get task by user ID _(coming soon)_](#resource-properties)
