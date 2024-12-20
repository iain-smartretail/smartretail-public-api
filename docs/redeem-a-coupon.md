---
sidebar_position: 3
---

# Redeem a Coupon

API Documentation for this endpoint...

```
POST <API_ROOT>/get/engage-v2/{session_id}
```

## Request Parameters

| Type       | Name         | Required | Example Value                        |
|------------|--------------|----------|--------------------------------------|
| URL Path   | session_id   | Yes      | 83c64b31-5128-40f1-b12d-df09062f9c8f |
| URL Query  | campaign_id  | No       | 2328927                              |

## Response Status

| Status Code | Meaning               |
|-------------|-----------------------|
| 200         | You're all set champ! |
| 202         | We'll sort it later   |
| 403         | Don't try that again  |

## Response Body

<Tabs>
<TabItem value="ok" label="Success">
```json
{
  "result": "ok"
}
```
</TabItem>
<TabItem value="error" label="Error">
```json
{
  "result": "error",
  "message": "This offer has already been redeemed by this session_id."
}
```
</TabItem>
</Tabs>
