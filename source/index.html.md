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

# Advertisement

URLs relateive to ___________, unless otherwise noted

## For Business Users
Method | HTTP request | Description
-------| ------------ | -----------
submitAds | POST user/{user-id}/ads | Submit a new advertisement
editAds | PUT user/{user-id}/ads/{ads-id} | Edit an advertisement
deleteAds | DELETE user/{user-id}/ads/{ads-id} | Delete an advertisement

## For Client Users
Method | HTTP request | Description
-------| ------------ | -----------
clickAds | POST user/{user-id}/ads/{ads-id} | Submit advertisement click information

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

URLs relateive to ___________, unless otherwise noted

Method | HTTP request | Description
-------| ------------ | -----------
getDeviceNameAndMac | GET user/{user-id}/device | Get the list of names and MAC address of the devices of the user


# Discount

URLs relateive to ___________, unless otherwise noted

## For Business Users

Method | HTTP request | Description
-------| ------------ | -----------
getDiscountSummary | GET user/{user-id}/discount | Get the summary of all hosting discounts of the user
getDiscountStatus | GET user/{user-id}/discount/{discount-id} | Get the information of discount distributed
addDiscount | POST user/{user-id}/discount | Add a new discount
editDiscount | PATCH user/{user-id}/discount/{discount-id} | Edit a discount
removeDiscount | DELETE user/{user-id}/discount/{discount-id} | Delete a discount
addDiscountRequest | POST user/{requester-user-id}/request/discount/{discount-id} | Submit a request of a discount
removeDiscountRequest | DELETE user/{requester-user-id}/request/discount/{discount-id} | Delete a request of a discount 
approveDiscount | POST user/{approver-user-id}/approve/discount/{discount-id} | Approve a discount request from another user
rejectDiscount | DELETE user/{approver-user-id}/approve/discount/{discount-id} | Delete a discount request from another user

## For Client Users

Method | HTTP request | Description
-------| ------------ | -----------
showDiscount | GET user/{client-user-id}/user/{business-user-id}/discount | Show discount information
collectDiscount | POST user/{user-id}/discount/{discount-id} | Add a discount to the user's account
applyDiscount | POST user/{user-id}/discount/{discount-id}/apply | Apply a discount
removeDiscount | DELETE user/{user-id}/discount/{discount-id} | Remove a discount from the user's account

# Geo-Service

URLs relateive to ___________, unless otherwise noted

Method | HTTP request | Description
-------| ------------ | -----------
getGeoLoc | GET user/{user-id}/geoloc | Get the latitude and longtitude of the user
getDrivingStatus | GET user/{user-id}/driving | Get the driving time and distance from user's current location
getMap | GET user/{user-id}/map | Get the map with direction of the user's current location to the destination

# Help

URLs relateive to ___________, unless otherwise noted

Method | HTTP request | Description
-------| ------------ | -----------
submitFeedback | POST user/{user-id}/feedback | Submit a feedback

# Login / Signup / Password
URLs relateive to ___________, unless otherwise noted

Method | HTTP request | Description
-------| ------------ | -----------
signup | POST signup | Submit a signup request
login | POST login | Submit a login request
verifyUser | POST verify-user | Verify the user's information in a forget password event
changePassword | POST change-password | Change the password of the user


# Membership

URLs relateive to ___________, unless otherwise noted

## For Business Users

Method | HTTP request | Description
-------| ------------ | -----------
getMember | GET user/{user-id}/member | Get the member information
addMember | POST user/{user-id}/member/{user-id} | Add a user as member
removeMember | DELTE user/{user-id}/member/{user-id} | Delete a user from membership
setMemberCriteriaEmail | POST user/{user-id}/member-criteria-email | Set member email criteria
setMemberCriteriaAge | POST user/{user-id}/member-criteria-age | Set member age criteria
...

## For Client Users


Method | HTTP request | Description
-------| ------------ | -----------
joinMembership | POST user/{user-id}/membership/{membership-id} | Join a membership
quitMembership | DELTE user/{user-id}/membership/{membership-id} | Quit a membership

# Notification

Method | HTTP request | Description
-------| ------------ | -----------
setNotificationFrequency | PUT user/{user-id}/notification-frequency | Set the frequency of the nofitication

# Order

## For Business Users
Method | HTTP request | Description
-------| ------------ | -----------
getProduct | GET user/{user-id}/product | Get all products and their categories
setProduct | POST user/{user-id}/product | Submit a product
editProduct | PUT user/{user-id}/product/{product-id} | Edit a product
deleteProduct | DELETE user/{user-id}/product/{product-id} | Delete a product
addProductCategory | POST user/{user-id}/product-category | Add a new product category
editProductCategory | PUT user/{user-id}/product-category/{product-category-id} | Edit a product category
deleteProductCategory | DELTE user/{user-id}/product-category/{product-category-id} | Delete a product category

## For Client Users
Method | HTTP request | Description
-------| ------------ | -----------
getProduct | GET user/{user-id}/product | Get all products and their categories

# Reward

URLs relateive to ___________, unless otherwise noted

## Display Reward Points
Method | HTTP request | Description
-------| ------------ | -----------
getRewardPoints | GET user/{user-id}/reward-points | Get the current reward points of the user
getRewardHistory | Get user/{user-id}/reward-history | Get the reward history of the user

## Add Reward Points
Each type of reward addition operation must be recorded and saved to history, a transaction id should be assigned to each reward addition operation. 

Method | HTTP request | Description
-------| ------------ | -----------
addCheckInReward | POST user/{user-id}/check-in-reward | Add check-in reward towards the user
addDiscountReward | POST user/{user-id}/discout-reward | Add discount usage reward towards the user
addSharingReward | POST user/{user-id}/sharing-reward | Add sharing reward towards the user
addBindingAccountReward | POST user/{user-id}/bind-acct-reward | Add binding account reward towards the user
addOrderInfoReward | POST user/{user-id}/order-info-reward | Add order information submittal reward towards the user
addSurveyReward | POST user/{user-id}/survey-reward | Add survey submittal reward towards the user

## Deduct Reward Points
Each type of reward deduction operation must be recorded and saved to history, a transaction id should be assigned to each reward deduction operation. 

Method | HTTP request | Description
-------| ------------ | -----------
deductDiscountReward | POST user/{user-id}/discount-reward/{discount-id} | Deduct discount reward points towards the user
deductInactiveReward | POST user/{uesr-id}/inactive | Deduct inactive reward points towards the user

# Search

URLs relateive to ___________, unless otherwise noted

Method | HTTP request | Description
-------| ------------ | -----------
generalSearch | POST user/{user-id}/search | General search which includes name of business / organization, location of business / organization, type of business / organization, type of product, and product category.
discountSearch | POST user/{user-id}/search/discount | Discount search which limited search scope within discounts
membershipSearch | POST user/{user-id}/search/membership | Membership search which limited search scope within memberships

# Settings

URLs relateive to ___________, unless otherwise noted

## General Settings
Method | HTTP request | Description
-------| ------------ | -----------
settingsConfig | POST user/{user-id}/setting-config | Submit settings configuration of the user

## Personal Settings
Method | HTTP request | Description
-------| ------------ | -----------

## Other Settings

# Tagging


=============================================================================
# Other Samples

# Sample Authentication

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

