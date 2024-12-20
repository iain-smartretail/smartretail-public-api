---
sidebar_position: 4
---

# Track a User Journey

API Documentation for this endpoint...

```
POST <API_ROOT>/post/update-action-status/{session_id}
```

## Request Parameters

| Type       | Name         | Required | Example Value                        |
|------------|--------------|----------|--------------------------------------|
| URL Path   | session_id   | Yes      | 83c64b31-5128-40f1-b12d-df09062f9c8f |
| HTTP Header| Content-Type | Yes      | application/json                     |

## Request Body

```json
{
  "events": [
    {
      "time": "2024-12-19T08:40:00Z",
      "action": "scan_qr"
    }
  ]
}
```

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
  "message": "This session_id is not recognized"
}
```
</TabItem>
</Tabs>
