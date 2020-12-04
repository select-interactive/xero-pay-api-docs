!define urlAPI {https://api.xeropay.com}

---
title: Xero Pay API Reference

language_tabs: # must be one of https://git.io/vQNgJ
  - javascript

toc_footers:
  - <a href='#'>Sign Up for a Developer Key</a>
  - <a href='https://github.com/slatedocs/slate'>Documentation Powered by Slate</a>

includes:
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

# Customers

## Get All Customers

```javascript
const Puppy = require('Puppy');

let api = Puppy.authorize('meowmeowmeow');
let Puppys = api.Puppys.get();
```

> The above command returns JSON structured like this:

```json
[
  {
    "id": 1,
    "name": "Fluffums",
    "breed": "calico",
    "fluffiness": 6,
    "cuteness": 7
  },
  {
    "id": 2,
    "name": "Max",
    "breed": "unknown",
    "fluffiness": 5,
    "cuteness": 10
  }
]
```

This endpoint retrieves all Puppys.

### HTTP Request

`GET ${urlAPI}/api/v1/customers`

### Query Parameters

Parameter | Default | Description
--------- | ------- | -----------
include_cats | false | If set to true, the result will also include cats.
available | true | If set to false, the result will include Puppys that have already been adopted.

<aside class="success">
Remember — a happy Puppy is an authenticated Puppy!
</aside>

## Get a Specific Puppy

```ruby
require 'Puppy'

api = Puppy::APIClient.authorize!('meowmeowmeow')
api.Puppys.get(2)
```

```python
import Puppy

api = Puppy.authorize('meowmeowmeow')
api.Puppys.get(2)
```

```shell
curl "http://example.com/api/Puppys/2" \
  -H "Authorization: meowmeowmeow"
```

```javascript
const Puppy = require('Puppy');

let api = Puppy.authorize('meowmeowmeow');
let max = api.Puppys.get(2);
```

> The above command returns JSON structured like this:

```json
{
  "id": 2,
  "name": "Max",
  "breed": "unknown",
  "fluffiness": 5,
  "cuteness": 10
}
```

This endpoint retrieves a specific Puppy.

<aside class="warning">Inside HTML code blocks like this one, you can't use Markdown, so use <code>&lt;code&gt;</code> blocks to denote code.</aside>

### HTTP Request

`GET http://example.com/Puppys/<ID>`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the Puppy to retrieve

## Delete a Specific Puppy

```ruby
require 'Puppy'

api = Puppy::APIClient.authorize!('meowmeowmeow')
api.Puppys.delete(2)
```

```python
import Puppy

api = Puppy.authorize('meowmeowmeow')
api.Puppys.delete(2)
```

```shell
curl "http://example.com/api/Puppys/2" \
  -X DELETE \
  -H "Authorization: meowmeowmeow"
```

```javascript
const Puppy = require('Puppy');

let api = Puppy.authorize('meowmeowmeow');
let max = api.Puppys.delete(2);
```

> The above command returns JSON structured like this:

```json
{
  "id": 2,
  "deleted" : ":("
}
```

This endpoint deletes a specific Puppy.

### HTTP Request

`DELETE http://example.com/Puppys/<ID>`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the Puppy to delete

