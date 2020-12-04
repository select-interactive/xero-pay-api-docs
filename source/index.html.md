---
title: Xero Pay API Reference

language_tabs: # must be one of https://git.io/vQNgJ
  - javascript

toc_footers:
  - <a href='#'>Sign Up for a Developer Key</a>
  - <a href='https://github.com/slatedocs/slate'>Documentation Powered by Slate</a>

includes:
  - customer
  - errors

search: true

code_clipboard: true
---


# Introduction

Xero Pay API can be used to connect your app to the Xero Pay API for state of the art transaction processing...

# Authentication

<!-- > You will need to get a key from us.  More coming.

```javascript
const Puppy = require('Puppy');
let api = Puppy.authorize('meowmeowmeow');
```

> Make sure to replace `meowmeowmeow` with your API key. -->

The Xero Pay API uses API keys to allow access to the API. You can register a new Puppy API key at our [developer portal](http://example.com/developers).

The API key to be included in all API requests to the server in a header that looks like the following:

`Authorization: Basic {{JSON_WEB_TOKEN}}`

<aside class="notice">
You must replace <code>{{JSON_WEB_TOKEN}}</code> with your personal API key.
</aside>

