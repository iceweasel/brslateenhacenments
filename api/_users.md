# Users

## Get User

```bash
curl "https://api.bitreserve.org/v0/me"
  -H "Authorization: Bearer <token>"
```

> The above command returns the following JSON:

```json
{
  "username": "byrnereese",
  "email": "byrne@bitreserve.org",
  "firstName": "Byrne",
  "lastName": "Reese",
  "name": "Byrne Reese",
  "country": "US",
  "state": "CA",
  "currencies": [
    "BTC",
    "USD",
    "EUR",
    "GBP",
    "CNY",
    "JPY",
    "XAU"
  ],
  "status": {
    "email": "ok",
    "phone": "pending",
    "review": "pending",
    "volume": "ok",
    "identity": "pending",
    "overview": "pending",
    "screening": "pending",
    "registration": "running"
  },
  "settings": {
    "theme": "minimalistic",
    "currency": "USD",
    "hasNewsSubscription": "true",
    "intl": {
      "language": {
        "locale": "en-US"
      },
      "dateTimeFormat": {
        "locale": "en-US"
      },
      "numberFormat": {
        "locale": "en-US"
      }
    },
    "hasOtpEnabled": "false"
  },
  "phones": [
    {
      "id": "1d78aeb5-43ac-4ee8-8d28-1291b5d8355c",
      "verified": "true",
      "primary": "true",
      "e164Masked": "+XXXXXXXXX04",
      "nationalMasked": "(XXX) XXX-XX04",
      "internationalMasked": "+X XXX-XXX-XX04"
    }
  ],
  "balances": {
    "total": "1083.77",
    "currencies": {
      "CNY": {
        "amount": "6.98",
        "balance": "42.82",
        "currency": "USD",
        "rate": "6.13880"
      },
      "EUR": {
        "amount": "75.01",
        "balance": "58.05",
        "currency": "USD",
        "rate": "1.29220"
      }
    }
  },
  "cards": [
    {
      "id": "2b2eb351-b1cc-48f7-a3d0-cb4f1721f3a3",
      "address": {
        "bitcoin": "145ZeN94MAtTmEgvhXEch3rRgrs7BdD2cY"
      },
      "label": "CNY card",
      "currency": "CNY",
      "balance": "42.82",
      "available": "42.82",
      "lastTransactionAt": "2014-06-16T20:46:51.002Z",
      "addresses": [
        {
          "id": "145ZeN94MAtTmEgvhXEch3rRgrs7BdD2cY",
          "network": "bitcoin"
        }
      ],
      "settings": {
        "position": 5,
        "starred": true
      }
    }
  ]
}
```

### Request

`GET https://api.bitreserve.org/v0/me`

### Response

Returns the details associated the current user.

<aside class="notice">Be advised that this method has the potential to return a great deal of data.</aside>

## Get User Phone Numbers

```bash
curl "https://api.bitreserve.org/v0/me/phones"
  -H "Authorization: Bearer <token>"
```

> The above command returns the following JSON:

```json
[
  {
    "id": "1d78aeb5-43ac-4ee8-8d28-1291b5d8355c",
    "verified": "true",
    "primary": "true",
    "e164Masked": "+XXXXXXXXX04",
    "nationalMasked": "(XXX) XXX-XX04",
    "internationalMasked": "+X XXX-XXX-XX04"
  }
]
```

### Request

`GET https://api.bitreserve.org/v0/me/phones`

### Response

Returns an array of all the phone numbers associated with the current user.
