---
title: "Waline"
subtitle: "How you can add Waline to your web page"
date: 2025-07-26T19:27:33+03:00
lastmod: 2025-07-26T19:27:33+03:00
draft: false
authors: []
description: ""

tags: []
categories: []
series: []

hiddenFromHomePage: false
hiddenFromSearch: false

featuredImage: ""
featuredImagePreview: ""

toc:
  enable: true
math:
  enable: false
lightgallery: false
license: ""
---

<!--more-->

## Importing in HTML (Client)

Here is how you can add Waline to your web page or website:

1. Import the stylesheet https://unpkg.com/@waline/client@v3/dist/waline.css in the `<head>`.

2. Create a `<script>` tag and initialize with `init()` from https://unpkg.com/@waline/client@v3/dist/waline.js while passing in the necessary `el` and `serverURL` options.

- The `el` option is the element used for Waline rendering. You can set a CSS selector in the form of a string or an HTMLElement object.
- `serverURL` is the link to your deployment server, which you just created in Vercel.
- For more options, visit the [Component Props page](https://waline.js.org/en/reference/client/props.html)

Here is an example:

```html
<head>
  <!-- ... -->
  <link
    rel="stylesheet"
    href="https://unpkg.com/@waline/client@v3/dist/waline.css"
  />
</head>
<body>
  <!-- ... -->
  <div id="waline"></div>
  <script type="module">
    import { init } from 'https://unpkg.com/@waline/client@v3/dist/waline.js';

    init({
      el: '#waline',
      serverURL: 'https://your-domain.vercel.app',
      lang: 'en',
    });
  </script>
</body>
```

## Comment Management (Management)

1. After the deployment is complete, please visit <serverURL>/ui/register to register. The first person to register will be set as an administrator.

2. After you log in as administrator, you'll be able to access the comment management dashboard. You can edit, mark or delete comments here.

3. Users can also register for an account via the comment box, and will be redirected to their profile page after logging in.

