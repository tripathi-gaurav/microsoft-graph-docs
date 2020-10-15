---
title: "Update userRunStates"
description: ""
localization_priority: Normal
author: "$(metadata.owner)"
ms.prod: "microsoft-identity-platform"
doc_type: "apiPageType"
---

# Update userRunStates

Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Update the properties of a deviceManagementScriptUserState object.

## Permissions

One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).

| Permission type                        | Permissions (from most to least privileged) |
| :------------------------------------- | :------------------------------------------ |
| Delegated (work or school account)     |                                             |
| Delegated (personal Microsoft account) |                                             |
| Application                            |                                             |

## HTTP request

<!-- {
  "blockType": "ignored"
}
-->

```http

```

## Request headers

| Name          | Description                 |
| :------------ | :-------------------------- |
| Authorization | Bearer {token}. Required.   |
| Content-Type  | application/json. Required. |

## Request Body

In the request body, supply JSON representation of the [deviceManagementScriptUserState](../resources/intune-devicemanagementscriptuserstate.md) object.

<!-- Actions and Functions -->

<!-- CRUD Methods -->

The following table shows the properties that are required when you create a deviceManagementScriptUserState object.

| Property           | Type   | Description                                                                                   |
| :----------------- | :----- | :-------------------------------------------------------------------------------------------- |
| errorDeviceCount   | Int32  | Error device count for specific user.                                                         |
| id                 | String | Key of the device management script user state entity. This property is read-only. Read-only. |
| successDeviceCount | Int32  | Success device count for specific user.                                                       |
| userPrincipalName  | String | User principle name of specific user.                                                         |

## Response

If successful, this method returns a `200 OK` response code and a deviceManagementScriptUserState object in the response body.

## Examples

### Request

<!-- {
  "blockType": "request",
  "name": "update_userrunstates"
}
-->

```http
PATCH https://graph.microsoft.com/beta

Content-Type: application/json
Content-Length: 224

[
  {
    "@odata.type": "#microsoft.graph.deviceManagementScriptUserState",
    "errorDeviceCount": "Int32",
    "id": "String(identifier)",
    "successDeviceCount": "Int32",
    "userPrincipalName": "String"
  }
]

```

### Response

**Note:** The response object shown here might be shortened for readability.

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "$(this.ReturnTypeFullName)"
}
-->

```http
HTTP 1.1 200 OK

Content-Type: application/json
{
  "value": [
  {
    "@odata.type": "#microsoft.graph.deviceManagementScriptUserState",
    "errorDeviceCount": "Int32",
    "id": "String(identifier)",
    "successDeviceCount": "Int32",
    "userPrincipalName": "String"
  }
]
}

```
