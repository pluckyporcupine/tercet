# Tercet

A bare minimum blogging platform utilizing Markdown for basically everything.

You can find a working sample website [here](http://mattchuranu.xyz/tercet/).

## Usage

Using Tercet is simple. It doesn't require a database or any external resources. As long as you have a webserver that runs PHP, you can run Tercet.

To post content, simply upload Markdown files to the /blog and /pages folders. The following metadata is recommended:

```Markdown
---
title: Test Post
author: Matt Chelen
date: February 18th, 2019
last-updated: February 19th, 2019
comments: yes
---
```

The _last-updated_ and _comments_ metadata options are optional. If last-updated does not exist, it simply will not show a last updated date. If _comments_ is set to anything other than "yes" or otherwise does not exist, comments will not be available for that post.

Posts that are in /blog are automatically listed on the homepage. Posts that are in /pages have to be manually linked to.

## Settings

You can set several settings using the /res/settings.md file.

**Root URL** - you must set your root URL to the folder that index.php resides in.
**Favicon** - can be either "on" or "off". File must be named "favicon.png".
**Header image** - can be either "off" or a file type. File must be named "headerimg.<file type>".
**Post preview text length** - the length of each of the post previews shown on the homepage. Please note that, at this time, uploading a file that has main content (h1 and img elements are automatically removed from the preview text) that is shorter than the length specified will break your blog.

The copyright notice and "Email me" hyperlink, as well as an email hyperlink that shows up during certain errors, are set automatically using the the **admin name** and **admin email** data specified in the settings file.

## Known issues

This has only been in development since February 18th, so it has a few issues.

- The aforementioned issue with post preview text length.
- Posts are in order of most recently updated, rather than most recently created. This is a Linux limitation and I am currently trying to come up with a user-friendly solution that doesn't involve writing an interface for writing posts.
- Comments aren't in chronological order. I am planning to fix that.

If you have any questions or run into problems, email me at matt@mattchuranu.xyz.
