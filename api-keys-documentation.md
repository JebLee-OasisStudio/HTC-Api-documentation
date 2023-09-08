[domain]: https://www.domain/.uk
[token]: your-api-key


## Introduction

**NOTE:** Please put your API key into request header

If you encounter any issues, please do not hesitate to create an issue in our [GitHub repository](https://github.com/JebLee-OasisStudio/HTC-Api-documentation/blob/main/api-keys-documentation.md) or to contact the maintainer for further assistance.

#### !Notice: If the customer_input_price is null or negative value(e.g -1), it will display the default price.

## **Get All Houses**

**Endpoint:** `/api/v1/houses`

**Description:** Get all houses

**Method:** `GET`

**Path parameters:** None

**Query parameters:** None

**Body parameters:** None

**Example request:**

```javascript
GET https://htc.eyesiteview.uk/htcpublic/api/v1/houses
Host: [domain](https://htc.eyesiteview.uk/htcpublic)
Content-Type: application/json
Authorization: your-api-key
```

**Example response:**

RESPONSE: 200 OK

```json
{
    "valid": true,
    "houses": [
        {
            "id": 37,
            "name": "Wiltshire_brid",
            "pdf_generation": 0,
            "client_id": 1,
            "public": 1,
            "overwrite_prices_url": null,
            "created_at": "2022-05-11T14:32:07.000000Z",
            "updated_at": "2023-01-27T10:16:44.000000Z"
        },
        {
            "id": 39,
            "name": "Master",
            "pdf_generation": 0,
            "client_id": 1,
            "public": 1,
            "overwrite_prices_url": null,
            "created_at": "2022-05-12T08:50:25.000000Z",
            "updated_at": "2022-05-12T08:50:25.000000Z"
        },
        {
            "id": 44,
            "name": "Stratford_brid",
            "pdf_generation": 0,
            "client_id": 1,
            "public": 1,
            "overwrite_prices_url": null,
            "created_at": "2022-07-22T13:24:30.000000Z",
            "updated_at": "2023-01-20T09:09:18.000000Z"
        },
        {
            "id": 45,
            "name": "Heatherington_brid",
            "pdf_generation": 0,
            "client_id": 1,
            "public": 1,
            "overwrite_prices_url": null,
            "created_at": "2022-08-05T11:34:28.000000Z",
            "updated_at": "2023-01-31T15:03:38.000000Z"
        },
        {
            "id": 46,
            "name": "Wentworth_brid",
            "pdf_generation": 0,
            "client_id": 1,
            "public": 1,
            "overwrite_prices_url": null,
            "created_at": "2022-08-19T14:30:22.000000Z",
            "updated_at": "2023-02-01T08:53:16.000000Z"
        },
        {
            "id": 54,
            "name": "Beaumont_brid",
            "pdf_generation": 0,
            "client_id": 1,
            "public": 1,
            "overwrite_prices_url": null,
            "created_at": "2022-08-30T10:08:41.000000Z",
            "updated_at": "2023-01-20T15:41:24.000000Z"
        },
        {
            "id": 55,
            "name": "Alderton_brid",
            "pdf_generation": 0,
            "client_id": 1,
            "public": 1,
            "overwrite_prices_url": null,
            "created_at": "2022-09-17T17:06:37.000000Z",
            "updated_at": "2023-02-01T11:33:55.000000Z"
        },
        {
            "id": 56,
            "name": "Oakley_maes",
            "pdf_generation": 0,
            "client_id": 1,
            "public": 1,
            "overwrite_prices_url": null,
            "created_at": "2022-09-23T09:35:45.000000Z",
            "updated_at": "2023-01-23T10:00:47.000000Z"
        }
    ]
}
```
---
## **Get house info**

**Endpoint:** `/api/v1/house/{houseId}/itemChoices`

**Description:** Get all items that contain price

**Method:** `GET`

**Path parameters:**

| Name      | Type      | Description |
| --------- | --------- | ----------- |
| `houseId` | `interge` | House ID    |

**Query parameters:**

None

**Body parameters:**

None

**Example request:**

```javascript
GET https://htc.eyesiteview.uk/htcpublic/api/v1/house/109/itemChoices
Host: [domain](https://htc.eyesiteview.uk/htcpublic)
Content-Type: application/json
Authorization: your-api-key
```

**Example response:**

RESPONSE: 200 OK

```json
{
    "valid": true,
    "data": {
        "houseId": 109,
        "house_name": "Testing",
        "productBundles": [
            {
                "productBundleId": 72,
                "productBundle_name": "The AEG Convenience Package",
                "productBundle_description": "This convenience package upgrades your standard inclusive Zanussi appliances to the AEG equivalent. Items are not available individually for upgrade.",
                "price": 31392,
                "customer_input_price": null
            }
        ],
        "categories": [
            {
                "roomId": 638,
                "room_name": "Bathroom",
                "itemId": 3719,
                "item_name": "Tiles",
                "categoryCollectionId": 1705,
                "categoryCollection_name": "Tile Layout",
                "categoryId": 5640,
                "category_name": "Standard",
                "category_description": null,
                "price": 0,
                "customer_input_price": null
            },
            {
                "roomId": 638,
                "room_name": "Bathroom",
                "itemId": 3719,
                "item_name": "Tiles",
                "categoryCollectionId": 1705,
                "categoryCollection_name": "Tile Layout",
                "categoryId": 5641,
                "category_name": "Premium Half",
                "category_description": null,
                "price": 48748,
                "customer_input_price": null
            },
            {
                "roomId": 638,
                "room_name": "Bathroom",
                "itemId": 3719,
                "item_name": "Tiles",
                "categoryCollectionId": 1705,
                "categoryCollection_name": "Tile Layout",
                "categoryId": 5642,
                "category_name": "Premium Whole Bathroom",
                "category_description": null,
                "price": 97496,
                "customer_input_price": null
            },
            {
                "roomId": 639,
                "room_name": "En Suite",
                "itemId": 3728,
                "item_name": "Tiles",
                "categoryCollectionId": 1707,
                "categoryCollection_name": "Tile Layout",
                "categoryId": 5645,
                "category_name": "Standard",
                "category_description": null,
                "price": 0,
                "customer_input_price": null
            },
            {
                "roomId": 639,
                "room_name": "En Suite",
                "itemId": 3728,
                "item_name": "Tiles",
                "categoryCollectionId": 1707,
                "categoryCollection_name": "Tile Layout",
                "categoryId": 5646,
                "category_name": "Premium Half",
                "category_description": null,
                "price": 48748,
                "customer_input_price": null
            },
            {
                "roomId": 639,
                "room_name": "En Suite",
                "itemId": 3728,
                "item_name": "Tiles",
                "categoryCollectionId": 1707,
                "categoryCollection_name": "Tile Layout",
                "categoryId": 5647,
                "category_name": "Premium Whole Bathroom",
                "category_description": null,
                "price": 109683,
                "customer_input_price": null
            },
            {
                "roomId": 640,
                "room_name": "Cloaks",
                "itemId": 3735,
                "item_name": "Tiles",
                "categoryCollectionId": 1709,
                "categoryCollection_name": "Tile Layout",
                "categoryId": 5650,
                "category_name": "Standard",
                "category_description": null,
                "price": 0,
                "customer_input_price": null
            },
            {
                "roomId": 640,
                "room_name": "Cloaks",
                "itemId": 3735,
                "item_name": "Tiles",
                "categoryCollectionId": 1709,
                "categoryCollection_name": "Tile Layout",
                "categoryId": 5651,
                "category_name": "Premium Half",
                "category_description": null,
                "price": 24374,
                "customer_input_price": null
            },
            {
                "roomId": 640,
                "room_name": "Cloaks",
                "itemId": 3735,
                "item_name": "Tiles",
                "categoryCollectionId": 1709,
                "categoryCollection_name": "Tile Layout",
                "categoryId": 5652,
                "category_name": "Premium Whole Bathroom",
                "category_description": null,
                "price": 97496,
                "customer_input_price": null
            }
        ],
        "popupItems": [
            {
                "roomId": 637,
                "room_name": "Kitchen",
                "itemId": 3703,
                "item_name": "Cupboards",
                "multipleChoiceId": 128,
                "multipleChoice_name": "Wall Units",
                "popupItemId": 49,
                "popupItem_name": "Led Strip Lights",
                "popupItem_description": "Led Strip Lights for under wall units",
                "price": 49900,
                "customer_input_price": null
            }
        ],
        "multipleChoiceOptions": [
            {
                "roomId": 637,
                "room_name": "Kitchen",
                "itemId": 3703,
                "item_name": "Cupboards",
                "multipleChoiceId": 128,
                "multipleChoice_name": "Wall Units",
                "multipleChoiceOptionId": 243,
                "multipleChoiceOption_name": "Yes",
                "multipleChoiceOption_description": null,
                "price": 125232,
                "customer_input_price": null
            },
            {
                "roomId": 637,
                "room_name": "Kitchen",
                "itemId": 3703,
                "item_name": "Cupboards",
                "multipleChoiceId": 128,
                "multipleChoice_name": "Wall Units",
                "multipleChoiceOptionId": 244,
                "multipleChoiceOption_name": "No",
                "multipleChoiceOption_description": null,
                "price": null,
                "customer_input_price": null
            }
        ],
        "itemChoices": [
            {
                "roomId": 637,
                "room_name": "Kitchen",
                "itemId": 3704,
                "item_name": "Handles",
                "itemChoiceId": 82217,
                "itemChoice_name": "HC357",
                "itemChoice_description": "Flat chrome handle",
                "price": 0,
                "customer_input_price": null
            },
            {
                "roomId": 637,
                "room_name": "Kitchen",
                "itemId": 3704,
                "item_name": "Handles",
                "itemChoiceId": 82218,
                "itemChoice_name": "HC900 & HC905",
                "itemChoice_description": "Small Round Knob (Cupboards) & Brushed Cup (Drawers)",
                "price": 0,
                "customer_input_price": null
            },
            {
                "roomId": 637,
                "room_name": "Kitchen",
                "itemId": 3704,
                "item_name": "Handles",
                "itemChoiceId": 82219,
                "itemChoice_name": "HC120",
                "itemChoice_description": "Gold Long bar handle",
                "price": 0,
                "customer_input_price": null
            },
            {
                "roomId": 637,
                "room_name": "Kitchen",
                "itemId": 3704,
                "item_name": "Handles",
                "itemChoiceId": 82220,
                "itemChoice_name": "HC003",
                "itemChoice_description": "Silver curved handle",
                "price": 0,
                "customer_input_price": null
            }
        ]
    }
}
```

RESPONSE: House not found

```json
{
    "valide": false,
    "error": "We couldn't find house data."
}
```

RESPONSE: API Key Error

```json
{
    "message": "Unauthorized"
}
```

---

## **Update Product Bundle pricing**

**Endpoint:** `/api/v1/houses/{houseId}/productBundles/{productBundleId}/updatePrice`

**Description:** Update Product Bundle pricing

**Example image:**

<img src="https://raw.githubusercontent.com/JebLee-OasisStudio/HTC-Api-documentation/main/Product_bundle.PNG?raw=true" alt="product_bundle_pricing.png" style="zoom: 70%;" />

**Method:** `PUT`

**Path parameters:** 
| Name      | Type      | Description |
| --------- | --------- | ----------- |
| `houseId` | `interge` | House ID    |
| `productBundleId` | `interge` | Product Bundle Id|

**Query parameters:** None

**Body parameters:**

| Name              | Type      | Description       |
| ----------------- | --------- | ----------------- |
| `houseId`         | `integer` | Item price        |
| `productBundleId` | `integer` | Product Bundle ID |

**Example request:**

```javascript

PUT https://htc.eyesiteview.uk/htcpublic/api/v1/houses/109/productBundles/72/updatePrice
HOST: [domain](https://htc.eyesiteview.uk/htcpublic)
Content-Type: application/json
Authorization: your-api-key

{
    "customer_input_price": 100
}
```

**Example response:**

RESPONSE: 200 OK

```json
{
    "valid": true,
    "data": [
        {
            "id": 72,
            "name": "The AEG Convenience Package",
            "description": "This convenience package upgrades your standard inclusive Zanussi appliances to the AEG equivalent. Items are not available individually for upgrade.",
            "rrp": 8989898,
            "customer_input_price": 8989898,
            "discount": 0,
            "house_id": 109,
            "updated_at": "2023-04-06T13:05:52.000000Z",
            "created_at": "2023-04-06T08:57:29.000000Z"
        }
    ]
}
```

RESPONSE: 404 Not Found

```json
{
    "valid": false,
    "error": "No query results for model "
}
```

RESPONSE: API Key Error

```json
{
    "message": "Unauthorized"
}
```

---

## **Update Category pricing**

**Endpoint:** `/api/v1/houses/{houseId}/rooms/{roomId}/items/{itemId}/categoryCollections/{categoryCollectionId}/categories/{categoryId}/updatePrice`

**Description:** Update Category pricing (e.g. Premium Whole Bathroom), onec you updated the price of category, all the price of item choices belong to the category will also changed.

**Example image:**

<img src="https://github.com/JebLee-OasisStudio/HTC-Api-documentation/blob/main/category_pricing.PNG?raw=true" alt="category_pricing.png" style="zoom: 70%;" />

**Method:** `PUT`

**Path parameters:**

| Name                   | Type      | Description            |
| ---------------------- | --------- | ---------------------- |
| `houseId`              | `integer` | House ID               |
| `roomId`               | `integer` | Room ID                |
| `itemId`               | `integer` | Item ID                |
| `categoryCollectionId` | `integer` | Category Collection ID |
| `categoryId`           | `integer` | Category ID            |

**Query parameters:** None

**Body parameters:**

| Name    | Type      | Description |
| ------- | --------- | ----------- |
| `customer_input_price` | `integer` | Item price  |

**Example request:**

```javascript
PUT https://htc.eyesiteview.uk/htcpublic/api/v1/houses/109/rooms/638/items/3719/categoryCollections/1705/categories/5640/updatePrice
HOST: [domain](https://htc.eyesiteview.uk/htcpublic)
Content-Type: application/json
Authorization: your-api-key

{
    "customer_input_price": 100
}
```

**Example response:**

RESPONSE: 200 OK

```json
{
    "valid": true,
    "data": {
        "id": 5640,
        "name": "Standard",
        "description": null,
        "category_collection_id": 1705,
        "price": 333333,
        "customer_input_price": 333333,
        "created_at": "2023-04-06T08:57:30.000000Z",
        "updated_at": "2023-04-06T13:07:04.000000Z",
        "order_index": 0
    }
}
```

RESPONSE: 404 Not Found

```json
{
    "valid": false,
    "error": "No query results for model "
}
```

RESPONSE: API Key Error

```json
{
    "message": "Unauthorized"
}
```
---

## **Update wardrobe pricing**

**Endpoint:** `/api/v1/houses/{houseId}/rooms/{roomId}/items/{itemId}/categories/{categoryId}/updatePrice`

**Description:** Update wardrobe pricing

**Example image:**

<img src="https://github.com/JebLee-OasisStudio/HTC-Api-documentation/blob/abc1e84b31d6716aab60fbaec60bdcf7f3e91cce/wardrobe.PNG" style="zoom: 70%;" />

**Method:** `PUT`

**Path parameters:**

| Name                   | Type      | Description            |
| ---------------------- | --------- | ---------------------- |
| `houseId`              | `integer` | House ID               |
| `roomId`               | `integer` | Room ID                |
| `itemId`               | `integer` | Item ID                |
| `categoryId`           | `integer` | Category ID            |

**Query parameters:** None

**Body parameters:**

| Name    | Type      | Description |
| ------- | --------- | ----------- |
| `customer_input_price` | `integer` | Item price  |

**Example request:**

```javascript
PUT https://htc.eyesiteview.uk/htcpublic/api/v1/houses/37/rooms/122/items/6081/categories/8967/updatePrice
HOST: [domain](https://htc.eyesiteview.uk/htcpublic)
Content-Type: application/json
Authorization: your-api-key

{
    "customer_input_price": 333333
}
```

**Example response:**

RESPONSE: 200 OK

```json
{
    "valid": true,
    "data": {
        "id": 8967,
        "name": "Kensington",
        "description": null,
        "category_collection_id": null,
        "price": 333333,
        "customer_input_price": 333333,
        "reference": null,
        "primary": 1,
        "option": 1,
        "default": 0,
        "created_at": "2023-09-06T10:26:35.000000Z",
        "updated_at": "2023-09-08T10:38:07.000000Z",
        "order_index": 0,
        "pivot": {
            "item_id": 6081,
            "category_id": 8967
        }
    }
}
```

RESPONSE: 404 Not Found

```json
{
    "valid": false,
    "error": "No query results for model "
}
```

RESPONSE: API Key Error

```json
{
    "message": "Unauthorized"
}
```
---

## **Update multiple choice options pricing**

**Endpoint:** `/api/v1/houses/{houseId}/rooms/{roomId}/items/{itemId}/multipleChoices/{multipleChoiceId}/multipleChoiceOptions/{multipleChoiceOptionId}/updatePrice`

**Description:** Update multiple choice options pricing (e.g Wall Unit)

**Example image:**

<img src="https://github.com/JebLee-OasisStudio/HTC-Api-documentation/blob/main/multiple_choice_options_pricing.PNG?raw=true" alt="multiple_choice_options.png" style="zoom: 70%;" />

**Method:** `PUT`

**Path parameters:**

| Name                   | Type      | Description            |
| ---------------------- | --------- | ---------------------- |
| `houseId`              | `integer` | House ID               |
| `roomId`               | `integer` | Room ID                |
| `itemId`               | `integer` | Item ID                |
| `multipleChoiceId`     | `integer` | Multiple Choice ID     |
| `multipleChoiceOption` | `integer` | Multiple Choice Option |

**Query parameters:** None

**Body parameters:**

| Name    | Type      | Description |
| ------- | --------- | ----------- |
| `customer_input_price` | `integer` | Item price  |

**Example request:**

```javascript
PUT https://htc.eyesiteview.uk/htcpublic/api/v1/houses/109/rooms/637/items/3703/multipleChoices/128/multipleChoiceOptions/243/updatePrice
HOST: [domain](https://htc.eyesiteview.uk/htcpublic)
Content-Type: application/json
Authorization: your-api-key

{
    "customer_input_price": 100
}
```

**Example response:**

RESPONSE: 200 OK

```json
{
    "valid": true,
    "data": {
        "id": 243,
        "name": "Yes",
        "description": null,
        "price": 798979,
        "customer_input_price": 798979,
        "multiple_choice_id": 128,
        "created_at": "2023-04-06T09:02:10.000000Z",
        "updated_at": "2023-04-06T13:07:23.000000Z"
    }
}
```

RESPONSE: 404 Not Found

```json
{
    "valid": false,
    "error": "No query results for model "
}
```

RESPONSE: API Key Error

```json
{
    "message": "Unauthorized"
}
```

---

## **Update Item Choice Customer Input**

**Endpoint:** `/api/v1/houses/{houseId}/rooms/{roomId}/items/{itemId}/itemChoices/{itemChoiceId}/updateCustomerInput`

**Description:** Update Item Choice pricing (most of the items can be found in the "Item Choices")

**Example image:**

<img src="https://github.com/JebLee-OasisStudio/HTC-Api-documentation/blob/main/item_choices.PNG?raw=true" alt="item_choices.png" style="zoom: 70%;" />

**Method:** `PUT`

**Path parameters:**

| Name           | Type      | Description    |
| -------------- | --------- | -------------- |
| `houseId`      | `integer` | House ID       |
| `roomId`       | `integer` | Room ID        |
| `itemId`       | `integer` | Item ID        |
| `itemChoiceId` | `integer` | Item Choice ID |

**Query parameters:** None

**Body parameters:**

| Name    | Type      | Description |
| ------- | --------- | ----------- |
| `customer_input_price` | `integer` | Item price  |
| `customer_input_name` | `string` | Item name  |
| `customer_input_description` | `string` | Item description  |

**Example request:**

```javascript
PUT https://htc.eyesiteview.uk/htcpublic/api/v1/houses/109/rooms/637/items/3704/itemChoices/82217/updateCustomerInput
HOST: [domain](https://htc.eyesiteview.uk/htcpublic)
Authorization: your-api-key

{
    "customer_input_price": 9888,
    "customer_input_name": "HC120",
    "customer_input_description": "Gold Long bar handle"
}
```

**Example response:**

RESPONSE: 200 OK

```json
{
    "valid": true,
    "data": {
        "id": 82217,
        "name": "HC357",
        "description": "Flat chrome handle",
        "reference": "6",
        "price": 9888,
        "customer_input_price": 9888,
        "customer_input_name": "HC120",
        "customer_input_description": "Gold Long bar handle",
        "thumbnail_image_id": 147192,
        "overlay_image_id": 79763,
        "item_id": 3704,
        "carousel_id": 2298,
        "most_popular": 0,
        "toggle_slider_id": null,
        "product_bundle_id": null,
        "disabled": 0,
        "has_conditioned_choices": 0,
        "gallery_id": null,
        "created_at": "2023-04-06T08:57:29.000000Z",
        "updated_at": "2023-04-06T13:13:49.000000Z"
    }
}
```

RESPONSE: 404 Not Found

```json
{
    "valid": false,
    "error": "No query results for model "
}
```

RESPONSE: API Key Error

```json
{
    "message": "Unauthorized"
}
```

---

## **Update popup item pricing**

**Endpoint:** `/api/v1/houses/{houseId}/rooms/{roomId}/items/{itemId}/multipleChoices/{multipleChoiceId}/popupItems/{popupItemId}/updatePrice`

**Description:** Update popup item pricing (currnetly only used for the "Led Strip Lighting")

**Example image:**

<img src="https://github.com/JebLee-OasisStudio/HTC-Api-documentation/blob/main/Pop.PNG?raw=true" alt="pupup_item.png" style="zoom: 70%;" />

**Method:** `PUT`

**Path parameters:**

| Name               | Type      | Description        |
| ------------------ | --------- | ------------------ |
| `houseId`          | `integer` | House ID           |
| `roomId`           | `integer` | Room ID            |
| `itemId`           | `integer` | Item ID            |
| `multipleChoiceId` | `integer` | Multiple Choice ID |
| `popupItemId`      | `integer` | Popup Item ID      |

**Query parameters:** None

**Body parameters:**

| Name    | Type      | Description |
| ------- | --------- | ----------- |
| `customer_input_price` | `integer` | Item price  |

**Example request:**

```javascript
PUT https://htc.eyesiteview.uk/htcpublic/api/v1/houses/109/rooms/637/items/3703/multipleChoices/128/popupItems/49/updatePrice
HOST: [domain](https://htc.eyesiteview.uk/htcpublic)
Authorization: your-api-key

{
    "customer_input_price": 100
}
```

**Example response:**

RESPONSE: 200 OK

```json
{
    "valid": true,
    "data": {
        "id": 49,
        "name": "Led Strip Lights",
        "description": "Led Strip Lights for under wall units",
        "multiple_choice_id": 128,
        "price": 99999,
        "customer_input_price": 99999,
        "overlay_image_id": 148179,
        "thumbnail_image_id": 148180,
        "created_at": "2023-04-06T09:10:27.000000Z",
        "updated_at": "2023-04-06T13:13:56.000000Z"
    }
}
```

RESPONSE: 404 Not Found

```json
{
    "valid": false,
    "error": "No query results for model "
}
```

RESPONSE: API Key Error

```json
{
    "message": "Unauthorized"
}
```
