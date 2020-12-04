# Customers

## Get All Customers

```javascript
// Comming soon
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

This endpoint retrieves all customers.

### HTTP Request

`GET ${urlAPI}/api/v1/customers`

### Query Parameters

Parameter | Default | Description
--------- | ------- | -----------

<aside class="success">

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

