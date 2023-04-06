[domain]: https://www.domain/.uk
[token]: your-api-key

# **Get All Houses**

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

# **Get house info**

**Endpoint:** `/api/v1/house/{houseId}/itemChoices`

**Description:** Get all items

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
GET https://htc.eyesiteview.uk/htcpublic/api/v1/house/104/itemChoices
Host: [domain](https://htc.eyesiteview.uk/htcpublic)
Content-Type: application/json
Authorization: your-api-key
```

**Example response:**

RESPONSE: 200 OK

```json
{
    "data": {
         "houseId": 104,
        "house_name": "Testing",
        "productBundles": [
            {
                "productBundleId": 6,
                "productBundle_name": "The AEG Convenience Package",
                "productBundle_description": "This convenience package upgrades your standard inclusive Zanussi appliances to the AEG equivalent. Items are not available individually for upgrade.",
                "price": 390430,
                "customer_input_price": 999999
            }
        ],
        "categories": [
            {
                "roomId": 113,
                "room_name": "Bathroom",
                "itemId": 426,
                "item_name": "Tiles",
                "categoryCollectionId": 139,
                "categoryCollection_name": "Tile Layout",
                "categoryId": 397,
                "category_name": "Standard",
                "category_description": null,
                "price": 390430,
                "customer_input_price": 0
            },
            {
                "roomId": 113,
                "room_name": "Bathroom",
                "itemId": 426,
                "item_name": "Tiles",
                "categoryCollectionId": 139,
                "categoryCollection_name": "Tile Layout",
                "categoryId": 398,
                "category_name": "Premium Half",
                "category_description": null,
                "price": 0,
                "customer_input_price": 55555
            },
            {
                "roomId": 113,
                "room_name": "Bathroom",
                "itemId": 426,
                "item_name": "Tiles",
                "categoryCollectionId": 139,
                "categoryCollection_name": "Tile Layout",
                "categoryId": 399,
                "category_name": "Premium Whole Bathroom",
                "category_description": null,
                "price": 390430,
                "customer_input_price": 666666
            }
        ],
        "popupItems": [
            {
                "roomId": 496,
                "room_name": "Kitchen",
                "itemId": 2672,
                "item_name": "Cupboards",
                "multipleChoiceId": 49,
                "multipleChoice_name": "Wall Units",
                "popupItemId": 5,
                "popupItem_name": "Led Strip Lights",
                "popupItem_description": "Led Strip Lights for under wall units",
                "price": 390430,
                "customer_input_price": 55555
            }
        ],
        "multipleChoiceOptions": [
            {
                "roomId": 496,
                "room_name": "Kitchen",
                "itemId": 2672,
                "item_name": "Cupboards",
                "multipleChoiceId": 49,
                "multipleChoice_name": "Wall Units",
                "multipleChoiceOptionId": 89,
                "multipleChoiceOption_name": "Yes",
                "multipleChoiceOption_description": null,
                "price": 390430,
                "customer_input_price": 999999
            },
            {
                "roomId": 496,
                "room_name": "Kitchen",
                "itemId": 2672,
                "item_name": "Cupboards",
                "multipleChoiceId": 49,
                "multipleChoice_name": "Wall Units",
                "multipleChoiceOptionId": 90,
                "multipleChoiceOption_name": "No",
                "multipleChoiceOption_description": null,
                "price": 390430,
                "customer_input_price": null
            }
        ],
        "itemChoices": [
            {
                "roomId": 496,
                "room_name": "Kitchen",
                "itemId": 2609,
                "item_name": "Handles",
                "itemChoiceId": 58961,
                "itemChoice_name": "HC357",
                "itemChoice_description": "Flat chrome handle",
                "price": 390430,
                "customer_input_price": null
            },
            {
                "roomId": 496,
                "room_name": "Kitchen",
                "itemId": 2609,
                "item_name": "Handles",
                "itemChoiceId": 58962,
                "itemChoice_name": "HC900 & HC905",
                "itemChoice_description": "Flat chrome handle",
                "customer_input_price": null
            },
            {
                "roomId": 496,
                "room_name": "Kitchen",
                "itemId": 2609,
                "item_name": "Handles",
                "itemChoiceId": 58963,
                "itemChoice_name": "HC120",
                "itemChoice_description": "Flat chrome handle",
                "price": 390430,
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

# **Update Product Bundle pricing**

**Endpoint:** `/api/v1/houses/{houseId}/productBundles/{productBundleId}/updatePrice`

**Description:** Update Product Bundle pricing

**Example image:**

<img src="https://raw.githubusercontent.com/JebLee-OasisStudio/HTC-Api-documentation/main/Product_bundle.PNG?raw=true" alt="product_bundle_pricing.png" style="zoom: 70%;" />

**Method:** `PUT`

**Path parameters:** None

**Query parameters:** None

**Body parameters:**

| Name              | Type      | Description       |
| ----------------- | --------- | ----------------- |
| `houseId`         | `integer` | Item price        |
| `productBundleId` | `integer` | Product Bundle ID |

**Example request:**

```javascript

PUT https://htc.eyesiteview.uk/htcpublic/api/v1/houses/104/productBundles/67/updatePrice
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
            "id": 6,
            "name": "The AEG Convenience Package",
            "description": "This convenience package upgrades your standard inclusive Zanussi appliances to the AEG equivalent. Items are not available individually for upgrade.",
            "rrp": 31392,
            "customer_input_price": 6699,
            "discount": 0,
            "house_id": 44,
            "updated_at": "2023-03-30T09:43:09.000000Z",
            "created_at": "2022-07-22T13:24:30.000000Z"
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

# **Update Category pricing**

**Endpoint:** `/api/v1/houses/{houseId}/rooms/{roomId}/items/{itemId}/categoryCollections/{categoryCollectionId}/categories/{categoryId}/updatePrice`

**Description:** Update Category pricing (e.g. Premium Whole Bathroom)

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
| `price` | `integer` | Item price  |

**Example request:**

```javascript
PUT https://htc.eyesiteview.uk/htcpublic/api/v1/houses/104/rooms/603/items/3469/categoryCollections/1613/categories/5318/updatePrice
HOST: [domain](https://htc.eyesiteview.uk/htcpublic)
Content-Type: application/json
Authorization: token

{
    "price": 100
}
```

**Example response:**

RESPONSE: 200 OK

```json
{
    "valid": true,
    "data": {
        "id": 397,
        "name": "Standard",
        "description": null,
        "category_collection_id": 139,
        "price": 0,
        "customer_input_price": 112233,
        "created_at": "2022-07-22T13:24:31.000000Z",
        "updated_at": "2023-03-30T10:41:05.000000Z",
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

# **Update multiple choice options pricing**

**Endpoint:** `/api/v1/houses/{houseId}/rooms/{roomId}/items/{itemId}/multipleChoices/{multipleChoiceId}/multipleChoiceOptions/{multipleChoiceOptionId}/updatePrice`

**Description:** Update multiple choice options pricing (e.g the AEG convenience package)

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
| `price` | `integer` | Item price  |

**Example request:**

```javascript
PUT https://htc.eyesiteview.uk/htcpublic/api/v1/houses/104/rooms/601/items/3444/multipleChoices/114/multipleChoiceOptions/216/updatePrice
HOST: [domain](https://htc.eyesiteview.uk/htcpublic)
Content-Type: application/json
Authorization: token

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
        "id": 89,
        "name": "Yes",
        "description": null,
        "price": 131535,
        "customer_input_price": 8888,
        "multiple_choice_id": 49,
        "created_at": "2022-12-22T14:38:55.000000Z",
        "updated_at": "2023-03-30T10:49:34.000000Z"
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

# **Update Item Choice pricing**

**Endpoint:** `/api/v1/houses/{houseId}/rooms/{roomId}/items/{itemId}/itemChoices/{itemChoiceId}/updatePrice`

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
| `price` | `integer` | Item price  |

**Example request:**

```javascript
PUT https://htc.eyesiteview.uk/htcpublic/api/v1/houses/104/rooms/601/items/3445/itemChoices/77178/updatePrice
HOST: [domain](https://htc.eyesiteview.uk/htcpublic)
Authorization: token

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
        "id": 58961,
        "name": "HC357",
        "description": "Flat chrome handle",
        "reference": "6",
        "price": 0,
        "customer_input_price": 100,
        "thumbnail_image_id": 91004,
        "overlay_image_id": 91340,
        "item_id": 2609,
        "carousel_id": 1537,
        "most_popular": 0,
        "toggle_slider_id": null,
        "product_bundle_id": null,
        "disabled": 0,
        "has_conditioned_choices": 0,
        "gallery_id": null,
        "created_at": "2022-12-22T14:13:33.000000Z",
        "updated_at": "2023-03-30T10:55:10.000000Z"
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

# **Update popup item pricing**

**Endpoint:** `/api/v1/houses/{houseId}/rooms/{roomId}/items/{itemId}/multipleChoices/multipleChoiceId/popupItems/{popupItemId}/updatePrice`

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
| `price` | `integer` | Item price  |

**Example request:**

```javascript
PUT https://htc.eyesiteview.uk/htcpublic/api/v1/houses/37/rooms/65/items/1864/multipleChoices/28/popupItem/12/updatePrice
HOST: domain
Authorization: token

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
        "id": 12,
        "name": "Led Strip Lights",
        "description": "Led Strip Lights for under wall units",
        "multiple_choice_id": 28,
        "price": 49900,
        "customer_input_price": -1,
        "overlay_image_id": 122751,
        "thumbnail_image_id": 122750,
        "created_at": "2023-02-14T12:07:09.000000Z",
        "updated_at": "2023-04-05T15:27:18.000000Z"
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
