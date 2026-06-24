---
# markdownlint-disable
# vale off
layout: default
title: Before you start a tutorial
description: Describes how to set up your system to run a local instance of the service
topic_type: tutorial
tags: introduction
categories: tutorial
ai_relevance: high
# importance: 9
prerequisites: []
related_pages: 
    - /tutorials/users-add-user.md
examples: []
api_endpoints: []
version: "v1.0"
last_updated: "2026-06-23"
# vale  on
# markdownlint-enable
---

<!-- markdownlint-disable MD025 -->

# Before you start a tutorial

<!-- markdownlint-enable MD025 -->

Do you have JSON-Server and `curl` on your system? If so, download the
[Blogging Service database file](https://github.com/fishavore/blogging-service/blob/main/api/blogging-service.json) and jump to [Test your system](#test-your-system).

Otherwise, move on to prepare for the tutorials. This should take about 20
minutes.

## Preparing for the tutorials

You need the following software to successfully run the tutorials.

- [node.js](https://nodejs.org/en/download)
- Version 0.17.4 of [json-server](https://www.npmjs.com/package/json-server/v/0.17.4)
- [curl](https://curl.se/download.html)
- [Blogging Service database file](https://github.com/fishavore/blogging-service/blob/main/api/blogging-service.json)

## Test your system

Follow these steps:

1. In a terminal, run JSON-Server from the same folder as the **Blogging Service**
database file.

    ```shell
    json-server -w blogging-service.json
    ```

    You should see this when the service starts:

    ```shell
    Resources
    http://localhost:3000/users
    http://localhost:3000/blogs
    http://localhost:3000/posts
    http://localhost:3000/comments

    Home
    http://localhost:3000
    ```

2. In another terminal on the same system, run the following command to get the
[user resource](api/user.md):

    ```shell
    curl http://localhost:3000/users
    ```

3. You should see this list of users:

    ```json
    [
        {
            "id": 1,
            "userName": "connoisseur",
            "lastName": "Smith",
            "firstName": "Ferdinand"
        },
        {
            "id": 2,
            "userName": "foodie",
            "lastName": "Millikan",
            "firstName": "Amelia"
        }
    ]
    ```

Now, you are ready for the [Tutorials](tutorials/tutorial.md).
