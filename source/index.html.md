---
title: API Reference

language_tabs: # must be one of https://git.io/vQNgJ
  - shell
  - dart
  - java
  - javascript
  - csharp

toc_footers:
  - <a href='#'>Sign Up for a Developer Key</a>
  - <a href='https://github.com/lord/slate'>Documentation Powered by Slate</a>

includes:
  - errors

search: true
---

# Introduction

Sample API documentation.

# Authentication

> To authorize, use this code:

```ruby
require 'kittn'

api = Kittn::APIClient.authorize!('meowmeowmeow')
```

```python
import kittn

api = kittn.authorize('meowmeowmeow')
```

```shell
# With shell, you can just pass the correct header with each request
curl "api_endpoint_here"
  -H "Authorization: meowmeowmeow"
```

```javascript
const kittn = require('kittn');

let api = kittn.authorize('meowmeowmeow');
```

> Make sure to replace `meowmeowmeow` with your API key.

Kittn uses API keys to allow access to the API. You can register a new Kittn API key at our [developer portal](http://example.com/developers).

Kittn expects for the API key to be included in all API requests to the server in a header that looks like the following:

`Authorization: meowmeowmeow`

<aside class="notice">
You must replace <code>meowmeowmeow</code> with your personal API key.
</aside>


# Advertisement
# Business User

URLs relateive to ___________, unless otherwise noted

## Profile

Method | HTTP request | Description
-------| ------------ | -----------
getProfile | GET user/{user-id}/profile | Get the profile of the user including name, photo, and description
changeUserName | PUT user/{user-id}/name | Change the name of the user
changeUserPhoto | PUT user/{user-id}/photo | Change the profile photo of the user
changeUserDesc | PUT user/{user-id}/description | Change the description of the user

## Send activities

Method | HTTP request | Description
-------| ------------ | -----------
sendActivity | POST user/{user-id}/activity | Send an activity
deleteActivity | DELTE user/{user-id}/activity/{id} | delete an activity

# Client User

URLs relateive to ___________, unless otherwise noted

## Profile

Method | HTTP request | Description
-------| ------------ | -----------
getProfile | GET user/{user-id}/profile | Get the profile of the user including name, photo, and status
changeUserName | PUT user/{user-id}/name | Change the name of the user
changeUserPhoto | PUT user/{user-id}/photo | Change the profile photo of the user
changeUserStatus | PUT user/{user-id}/status | Change the status of the user

## Collection

Method | HTTP request | Description
-------| ------------ | -----------
getCollection | GET user/{user-id}/collection | Get the collection of the user
createCollection | POST user/{user-id}/collection | Create a new collection
editCollection | PUT user/{user-id}/collection/{collection-id} | Change the name of the collection
deleteCollection | DELTE user/{user-id}/collection/{collection-id} | Delete a collection
addToCollection | PUT user/{user-id}/collection/{collection-id}/entity/{entity-id} | Add an entity into a collection
removeFromCollection | DELETE user/{user-id}/collection/{collecition-id} | Delete an entity from a collection

## Sharing

Method | HTTP request | Description
-------| ------------ | -----------
shareEntity | POST user/{user-id}/share/{platform-id}/entity/{entity-id} | Share an entity to a platform
shareDiscount | POST user/{user-id}/share/{platform-id}/discount/{discount-id} | Share a discount to a platform
shareRequest | POST user/{user-id}/share/{platform-id}/request/{request-id} | Share a request to a platform

# Device ID
# Discount

URLs relateive to ___________, unless otherwise noted

Method | HTTP request | Description
-------| ------------ | -----------
getDiscountStatus | GET user/{user-id}/discout-status/{discount-id} | Get the information of discount distributed 

# Geo-Service
# Help
# Login / Signu
# Membership

URLs relateive to ___________, unless otherwise noted

## For Business Users

Method | HTTP request | Description
-------| ------------ | -----------
getMembers | GET user/{user-id}/members | Get the member information
setMemberCriteria | POST user/{user-id}/member-criteria | Set member criteria


# Notification
# Order
# Reward
# Search
# Settings
# Tagging

## Get All Kittens

```ruby
require 'kittn'

api = Kittn::APIClient.authorize!('meowmeowmeow')
api.kittens.get
```

```python
import kittn

api = kittn.authorize('meowmeowmeow')
api.kittens.get()
```

```shell
curl "http://example.com/api/kittens"
  -H "Authorization: meowmeowmeow"
```

```javascript
const kittn = require('kittn');

let api = kittn.authorize('meowmeowmeow');
let kittens = api.kittens.get();
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

This endpoint retrieves all kittens.

### HTTP Request

`GET http://example.com/api/kittens`

### Query Parameters

Parameter | Default | Description
--------- | ------- | -----------
include_cats | false | If set to true, the result will also include cats.
available | true | If set to false, the result will include kittens that have already been adopted.

<aside class="success">
Remember — a happy kitten is an authenticated kitten!
</aside>

## Get a Specific Kitten

```ruby
require 'kittn'

api = Kittn::APIClient.authorize!('meowmeowmeow')
api.kittens.get(2)
```

```python
import kittn

api = kittn.authorize('meowmeowmeow')
api.kittens.get(2)
```

```shell
curl "http://example.com/api/kittens/2"
  -H "Authorization: meowmeowmeow"
```

```javascript
const kittn = require('kittn');

let api = kittn.authorize('meowmeowmeow');
let max = api.kittens.get(2);
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

This endpoint retrieves a specific kitten.

<aside class="warning">Inside HTML code blocks like this one, you can't use Markdown, so use <code>&lt;code&gt;</code> blocks to denote code.</aside>

### HTTP Request

`GET http://example.com/kittens/<ID>`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the kitten to retrieve

## Delete a Specific Kitten

```ruby
require 'kittn'

api = Kittn::APIClient.authorize!('meowmeowmeow')
api.kittens.delete(2)
```

```python
import kittn

api = kittn.authorize('meowmeowmeow')
api.kittens.delete(2)
```

```shell
curl "http://example.com/api/kittens/2"
  -X DELETE
  -H "Authorization: meowmeowmeow"
```

```javascript
const kittn = require('kittn');

let api = kittn.authorize('meowmeowmeow');
let max = api.kittens.delete(2);
```

> The above command returns JSON structured like this:

```json
{
  "id": 2,
  "deleted" : ":("
}
```

This endpoint deletes a specific kitten.

### HTTP Request

`DELETE http://example.com/kittens/<ID>`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the kitten to delete

