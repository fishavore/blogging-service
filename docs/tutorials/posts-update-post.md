---
# markdownlint-disable
# vale off
layout: default
title: Update a post
description: Update a post resource in the service
topic_type: tutorial
tags: api
categories: tutorial
ai_relevance: high
# importance: 6
prerequisites: /before-you-start-a-tutorial
related_pages:
    - /api/blog
    - /api/post
examples: []
api_endpoints: PATCH /posts/{id}
version: "v1.1"
last_updated: "2026-06-27"
# vale on
# markdownlint-enable
---

<!-- markdownlint-disable MD025 -->
<!-- vale Google.Headings = NO -->

# Tutorial - Update a post

<!-- markdownlint-enable MD025 -->
<!-- vale Google.Headings = YES -->

Are you ready to learn how to update a post in the service? It's so easy that
you can finish in about 10 minutes.

## Before you start

First, check [Before you start a tutorial](../before-you-start-a-tutorial.md) to make sure your system is ready.

To have a post in the service, the user must be in the service and have created
their blog first.

Learn more about the [`user` resource](../api/user.md) and [`blog` resource](../api/blog.md).

## Update a post

You are going to use the `PATCH` method to update one or more properties of the
[`post` resource](../api/post.md) in the service.

This tutorial updates a post to add a comment with `id` of `3`. The
[Add a comment](comments-add-comment.md) tutorial adds that comment to the **Blogging Service** database.

1. In a terminal, run JSON Server from the same folder as the **Blogging Service**
database file.

    ```shell
    json-server -w blogging-service.json
    ```

2. In another terminal on the same system, run the following command to update
a [`post` resource](api/post.md). Note that you can change the value of each property in the
request body, but you shouldn't change any property names, such as
`commentIds`, in the example below.

    ```shell
    curl -X PATCH -H 'content-type: application/json' \
        --url http://localhost:3000/posts/1 \
        -d '{
                "commentIds": [3]
            }'
    ```

3. After successfully updating the post, you get a response body showing your
updates. Note that the `commentIds` property now has `3`.

    ```json
    {
        "id": 1,
        "title": "Nikka whiskey review",
        "content": "Good 8 out of 10",
        "postedDate": "2026-06-03T17:00",
        "private": false,
        "blogId": 1,
        "category": "drink",
        "commentIds": [
            3
        ]
    }
    ```

<!-- markdownlint-disable MD033 -->

<div style="text-align: right;">| <a href="https://fishavore.github.io/blogging-service/">Home</a> | <a href="https://fishavore.github.io/blogging-service/api/reference.html">Reference</a> | <a href="https://fishavore.github.io/blogging-service/tutorials/tutorial.html">Tutorials</a> |</div>
