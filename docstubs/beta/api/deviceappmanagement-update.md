---
title: "Update deviceAppManagement"
description: ""
localization_priority: Normal
author: "$(metadata.owner)"
ms.prod: "microsoft-identity-platform"
doc_type: "apiPageType"
---

# Update deviceAppManagement

Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Update the properties of a deviceAppManagement object.

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

In the request body, supply JSON representation of the [deviceAppManagement](../resources/intune-deviceappmanagement.md) object.

<!-- Actions and Functions -->

<!-- CRUD Methods -->

The following table shows the properties that are required when you create a deviceAppManagement object.

| Property | Type   | Description                   |
| :------- | :----- | :---------------------------- |
| id       | String | Key of the entity. Read-only. |

## Response

If successful, this method returns a `200 OK` response code and a deviceAppManagement object in the response body.

## Examples

### Request

<!-- {
  "blockType": "request",
  "name": "update_deviceappmanagement"
}
-->

```http
PATCH https://graph.microsoft.com/beta/deviceAppManagement

Content-Type: application/json
Content-Length: 61

{
  "@odata.type": "#microsoft.graph.deviceAppManagement"
}

```

### Response

**Note:** The response object shown here might be shortened for readability.

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.management.services.api.deviceAppManagement"
}
-->

```http
HTTP 1.1 200 OK

Content-Type: application/json
{
  "value": {
  "@odata.type": "#microsoft.graph.deviceAppManagement",
  "id": "String(identifier)"
}
}

```
