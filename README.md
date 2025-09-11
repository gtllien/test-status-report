## Status.zesty.io

Simple html file that requests our service health endpoints to gives user feedback. Simple javascript, and uses CSS from extensions.zesty.io

Files are stored in a google cloud bucket:
https://console.cloud.google.com/storage/browser/status.zesty.io?project=zesty-prod

DNS managed on cloudflare with HTTPS on to SSL on the cloud bucket.

## Creating an Incident Report

### Step 1: Navigate to the `_incidents` Directory

All incident reports are stored in the _incidents directory. Open the project folder and locate this directory.

### Step 2: Create a New File

Create a new Markdown file (`.md`) inside the `_incidents` directory. The file name must follow a specific format:

`YYYY-MM-DD-your-title.md`
* `YYYY-MM-DD`: The date of the post.
* `your-title`: A slug-friendly title for the post (use hyphens instead of spaces).

**Example:**
`2025-09-11-incident-report-database-outage.md`

### Step 3: Add the Front Matter

The "front matter" is a block of YAML at the top of your Markdown file, enclosed by triple-dashed lines (`---`). It provides metadata about the incident post, such as the title, date, tags, and collection.
Refer to the below example template.

```yaml
---
layout: post
title: Platform Outage
date: 2025-09-11 10:30:00 -0700
collection: incidents
tags: [incident, outage, database, report, critical]
---

```
**Field Description:**

* `layout`: Specifies the Liquid template to use for rendering the page. Use the value `post` for the page layout.

* `title`: The title of the incident report. This is what will be displayed on the page.

* `date`: The date and time the report is created. The format is `YYYY-MM-DD HH:MM:SS +/-TTTT`. The time zone offset (`-0700` in the example) is optional but recommended.

* `collection`: The name of the directory in which the reports are stored. Use the value `incidents`

* `tags`: A list of keywords related to the post. Useful for searchability and creating related content links. 

### Step 4: Write the Incident Report Content

The content should be in markdown format. You can use standard markdown syntax for headings, lists, bold text, code blocks, and more.

**Example Incident report:**

> A critical security vulnerability was discovered in our authentication system on September 10, 2025. This vulnerability could have allowed unauthorized access to user accounts.
>
> Our team successfully patched the vulnerability within 2 hours of its discovery, and no user data was compromised.
> A full report will be provided once ready.




