---
# markdownlint-disable
# vale off
layout: default
title: Delete a comment
description: Delete a comment resource in the service
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
api_endpoints: DELETE /comments/{id}
version: "v1.0"
last_updated: "2026-06-27"
# vale  on
# markdownlint-enable
---

<!-- markdownlint-disable MD025 -->
<!-- vale Google.Headings = NO -->

# Tutorial - Delete a comment

<!-- markdownlint-enable MD025 -->
<!-- vale Google.Headings = YES -->

Are you ready to learn how to delete a comment in the service? It's so easy
that you can finish in about 10 minutes.

## Before you start

First, check [Before you start a tutorial](../before-you-start-a-tutorial.md) to make sure your system is ready.

Each comment belongs to a post in the service.

Learn more about the [`post` resource](../api/post.md).

## Delete a comment

You are going to use the `DELETE` method to delete a [`comment` resource](../api/comment.md) in
the service.

1. In a terminal, run JSON Server from the same folder as the **Blogging Service**
database file.

    ```shell
    json-server -w blogging-service.json
    ```

2. In another terminal on the same system, run the following command to delete
a [`comment` resource](../api/comment.md).

    ```shell
    curl -X DELETE -H 'content-type: application/json' \
        --url http://localhost:3000/comments/3
    ```

3. After successfully deleting the comment, you get an empty response body.

    ```json
    {}
    ```

After deleting a comment, don't forget to update the [`post` resource](../api/post.md).

This tutorial deletes the [`comment` resource](../api/comment.md) `id` of `3`. A [`post` resource](../api/post.md)
may have `commentIds` of `3`, which you should remove. You can learn how to do
that using the [Update a post](posts-update-post.md) tutorial.

<!-- markdownlint-disable MD033 -->

<div style="text-align: right;">| <a href="https://fishavore.github.io/blogging-service/">Home</a> | <a href="https://fishavore.github.io/blogging-service/api/reference.html">Reference</a> | <a href="https://fishavore.github.io/blogging-service/tutorials/tutorial.html">Tutorials</a> |</div>
