---
# markdownlint-disable
# vale off
layout: default
title: Reference
description: Lists the references available in the documentation
topic_type: reference
tags: api
categories: api-reference
ai_relevance: high
# importance: 8
prerequisites: []
related_pages: []
examples: []
api_endpoints: []
version: "v1.1"
last_updated: "2026-06-27"
# vale  on
# markdownlint-enable
---

<!-- markdownlint-disable MD025 -->

# Reference

<!-- markdownlint-enable MD025 -->

Below, you can find documentation with detailed descriptions of each
**Blogging Service** resource.

The `{base_url}` in the documentation is a placeholder for the URL of a
resource, and it varies depending on the installation of the service.

Generally, use `http://localhost:3000` to run tests on your system. The steps
to set up and test your system are in [Before you start a tutorial](../before-you-start-a-tutorial.md).

## User resource

* [`user`](user.md)

## Blog resource

To have a blog in the service, the user must be in the service first.

* [`blog`](blog.md)
* [Create a blog](blogs-create-blog.md)
* [Get all blogs](blogs-get-all-blogs.md)

## Post resource

To have a post in the service, the user must be in the service and have created
their blog first.

* [`post`](post.md)
* [Create a post](posts-create-post.md)
* [Get posts by blog ID](posts-get-posts-by-blogId.md)
* [Replace a post](posts-replace-post.md)

## Comment resource

To add a comment in the service, the blog and post must already be in the
service.

Anybody can add a comment in the service. To have a comment that's associated
with a user in the service, the user must be in the service first. Use
`Anonymous` for the `userName` property when the new comment isn't associated
with any user in the service.

* [`comment`](comment.md)
* [Get comments by post ID](comments-get-comments-by-postId.md)

<!-- markdownlint-disable MD033 -->

<div style="text-align: right;">| <a href="https://fishavore.github.io/blogging-service/">Home</a> | <a href="https://fishavore.github.io/blogging-service/api/reference.html">Reference</a> | <a href="https://fishavore.github.io/blogging-service/tutorials/tutorial.html">Tutorials</a> |</div>
