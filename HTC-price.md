[domain]: https://www.domain/.uk
[token]: your-api-key

# **Get all items by house id**

**Endpoint:** `{{domain}}/api/v1/house/44/itemChoices`

**Description:** Get all items

**Method:** `GET`

**Path parameters:**

| Name       | Type      | Description |
| ---------- | --------- | ----------- |
| `house_id` | `interge` | House ID    |

**Query parameters:**

None

**Body parameters:**

None

**Example request:**

```http
GET {{domain}}/api/v1/house/44/itemChoices
Host: {{domain}}
Content-Type: application/json
Authorization: {{token}}
```

**Example response:**

RESPONSE: 200 OK

```json
{
    "data": {
        "houseId": 44,
        "house_name": "Stratford_brid",
        "productBundles": [
            {
                "productBundleId": 6,
                "productBundle_name": "The AEG Convenience Package",
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
                "customer_input_price": null
            },
            {
                "roomId": 496,
                "room_name": "Kitchen",
                "itemId": 2609,
                "item_name": "Handles",
                "itemChoiceId": 58962,
                "itemChoice_name": "HC900 & HC905",
                "customer_input_price": null
            },
            {
                "roomId": 496,
                "room_name": "Kitchen",
                "itemId": 2609,
                "item_name": "Handles",
                "itemChoiceId": 58963,
                "itemChoice_name": "HC120",
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

# **Update Product Bundle pricing**

**Endpoint:** `https://api.{{domain}}/api/v1/houses/{houseId}/productBundles/{productBundleId}/updatePrice`

**Description:** Update Product Bundle pricing

**Method:** `PUT`

**Path parameters:** None

**Query parameters:** None

**Body parameters:**

| Name       | Type      | Description   |
| ---------- | --------- | ------------- |
| `price`    | `integer` | Item price    |

**Example request:**

```http

PUT https://api.{{domain}}/api/v1/houses/44/productBundles/6/updatePrice
HOST: api.{{domain}}
Content-Type: application/json
Authorization: Bearer {{token}}

{
    "price": 100
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

