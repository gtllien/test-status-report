## Status.zesty.io

 This is Zesty.io platform's status report page hosted on GitHub Pages using a Jekyll theme. 
 
 The page's HTML dynamically checks the status of our services by making requests to their respective health endpoints.

| Service      | Health Endpoint |
|:-------------|:------------------|
| Accounts API | https://accounts.api.zesty.io/ |
| Instances API | https://instances.api.zesty.io/ |
| Media API | https://svc.zesty.io/media-manager-service/ |
| Auth API | https://svc.zesty.io/auth/ |
| Accounts UI | https://accounts.zesty.io/login |
| Manager UI | https://8-aaeffee09b-7w6v22.manager.zesty.io/ |
| WebEngine | https://zdrflzfm-dev.webengine.zesty.io/__healthz__ |

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
tags: [WebEngine]
---

```
**Field Description:**

* `layout`: Specifies the Liquid template to use for rendering the page. Use the value `post` for the page layout.

* `title`: The title of the incident report. This is what will be displayed on the page. If title is not added, its value will be derived from the incident filename. Otherwise, it will default to the site's page title.

* `date`: The date and time the report is created. The format is `YYYY-MM-DD HH:MM:SS +/-TTTT`. The time zone offset (`-0700` in the example) is optional but recommended.

* `collection`: The name of the directory in which the reports are stored. Use the value `incidents`

* `tags`: A list of keywords related to the post. Useful for searchability and creating related content links. The value should be the service(s) affected. Please refer to the below list of pre-defined tags to use (should be case-sensitive).
  - AccountsAPI
  - InstancesAPI
  - MediaAPI
  - AuthAPI
  - AccountsUI
  - ManagerUI
  - WebEngine
  - GCP

### Step 4: Write the Incident Report Content

The content should be in markdown format. You can use standard markdown syntax for headings, lists, bold text, code blocks, and more.

**Example Incident report:**

> A critical security vulnerability was discovered in our authentication system on September 10, 2025. This vulnerability could have allowed unauthorized access to user accounts.
>
> Our team successfully patched the vulnerability within 2 hours of its discovery, and no user data was compromised.
> A full report will be provided once ready.







