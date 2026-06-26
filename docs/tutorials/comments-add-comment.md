---
# markdownlint-disable
# vale off
layout: default
title: Add a comment
description: Add a comment resource to the service
topic_type: tutorial
tags: api
categories: tutorial
ai_relevance: high
# importance: 6
prerequisites:
    - /before-you-start-a-tutorial
    - /api/blog
    - /api/post
related_pages: []
examples: []
api_endpoints: POST /comments
version: "v1.0"
last_updated: "2026-06-25"
# vale  on
# markdownlint-enable
---

<!-- markdownlint-disable MD025 -->
<!-- vale Google.Headings = NO -->

# Tutorial - Add a comment

<!-- markdownlint-enable MD025 -->
<!-- vale Google.Headings = YES -->

Are you ready to add a comment in the service? It's so easy that you can finish
in about 10 minutes.

## Before you start

First, check [Before you start a tutorial](../before-you-start-a-tutorial.md) to make sure your system is ready.

To add a comment in the service, the blog and post must already be in the
service.

Anybody can add a comment in the service. To have a comment that's associated
with a user in the service, the user must be in the service first. Use
`Anonymous` for the `userName` property when the new comment isn't associated
with any user in the service.

Learn more about the [`user` resource](user.md), [`blog` resource](blog.md), and
[`post` resource](post.md).

## Add a comment

You are going to use the `POST` method to add a [`comment`](../api/comments.md) resource in the
service.

This tutorial adds a new comment by `adventurer`. The [Add a user](users-add-user.md) tutorial
adds the `adventurer` user to the **Blogging Service** database.

1. In a terminal, run JSON-Server from the same folder as the **Blogging Service**
database file.

    ```shell
    json-server -w blogging-service.json
    ```

2. In another terminal on the same system, run the following command to update
a [`comment` resource](api/comment.md). Note that you can change the value of each property in
the request body, but you shouldn't change any propery names, such as `postId`,
in the example below.

    ```shell
    curl -H 'content-type: application/json' \
        --url http://localhost:3000/comments \
        -d '{
                "content": "That must be the one to try!",
                "postedDate": "2026-06-06T09:00",
                "postId": 1,
                "userName": "adventurer"
            }'
    ```

3. After successfully adding the comment, you get a response body with the
values that you specified. `id` is the new comment's unique record ID.

    ```json
    {
        "content": "That must be the one to try!",
        "postedDate": "2026-06-06T09:00",
        "postId": 1,
        "userName": "adventurer",
        "id": 3
    }
    ```

Don't forget to update the [`post` resource](../api/post.md) `id` of `1` with the new comment's
 id, `3`. The [Update a post](posts-update-post.md) tutorial walks you through that.

<!-- markdownlint-disable MD033 -->

<div style="text-align: right;">| <a href="https://fishavore.github.io/blogging-service/">Home</a> | <a href="https://fishavore.github.io/blogging-service/api/reference.html">Reference</a> | <a href="https://fishavore.github.io/blogging-service/tutorials/tutorial.html">Tutorials</a> |</div>
