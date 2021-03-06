## /messages
API end-point to send messages to conversation groups inside Kaizala. Current scope is to support posting of messages only.

### POST /messages

    POST https://{api_root}/groups/{groupId}/messages

##### Request Parameters

|  | Parameter | Type | Optional? | Description |
| :---: | :---: | :---: | :---:	| :--- |
| URL Path Parameter | groupId | String | No | GUID representing the groupId of the specific group resource |
| HTTP Header | applicationId | String | No | ID associated with the Connector that was registered by the developer – on behalf of which the API calls need to be made |
| HTTP Header | accessToken | String | No | Access Token received from the auth end-point |
| HTTP Header | Content-Type | String | No | value: application/json |

##### Request body

| Parameter | Type | Description |
| :---: | :---: | :--- |
| message | String | Text message to be sent (Max limit of 1000 Characters) |

###### Sample JSON Request

```javascript
{
  "message": "Hello All! Welcome to Kaizala."
}
```

##### Response body

| Parameter | Type | Description |
| :---: | :---: | :--- |
| referenceId | String | GUID representing the succesful completion of the request |

###### Sample JSON Response

```javascript
{
    "referenceId": "853654b2-5874-462d-b709-0c4e43a7083f"
}
```