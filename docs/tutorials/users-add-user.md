---
# markdownlint-disable
# vale off
layout: default
title: Add a user
description: Add a user resource to the service
topic_type: tutorial
tags: api
categories: tutorial
ai_relevance: high
# importance: 6
prerequisites:
    - /before-you-start-a-tutorial
    - /api/user
related_pages: []
examples: []
api_endpoints: POST /users
version: "v1.1"
last_updated: "2026-06-27"
# vale  on
# markdownlint-enable
---

<!-- markdownlint-disable MD025 -->
<!-- vale Google.Headings = NO -->

# Tutorial - Add a user

<!-- markdownlint-enable MD025 -->
<!-- vale Google.Headings = YES -->

Are you ready to learn how to add a user to the service? It's so easy that you
can finish in about 15 minutes.

## Before you start

First, check [Before you start a tutorial](../before-you-start-a-tutorial.md) to make sure your system is ready.

## Add a user

You are going to use the `POST` method to store the details of the new [`user`](../api/user.md)
resource in the service.

1. In a terminal, run JSON Server from the same folder as the **Blogging Service**
database file.

    ```shell
    json-server -w blogging-service.json
    ```

2. In another terminal on the same system, run the following command to add a
[`user` resource](../api/user.md). Note that you can change the value of each property in the
request body, but you shouldn't change any property names, such as `userName`,
in the example below.

    ```shell
    curl -H 'content-type: application/json' \
        --url http://localhost:3000/users \
        -d '{
                "userName": "adventurer",
                "lastName": "Parvani",
                "firstName": "Everett"
            }'
    ```

3. After successfully adding the user, you get a response body with the
values that you specified. `id` is the new user's unique record ID.

    ```json
    {
        "userName": "adventurer",
        "lastName": "Parvani",
        "firstName": "Everett",
        "id": 3
    }
    ```

<!-- markdownlint-disable MD033 -->

<div style="text-align: right;">| <a href="https://fishavore.github.io/blogging-service/">Home</a> | <a href="https://fishavore.github.io/blogging-service/api/reference.html">Reference</a> | <a href="https://fishavore.github.io/blogging-service/tutorials/tutorial.html">Tutorials</a> |</div>
