---
title: "Add windowsManagementApp"
description: ""
localization_priority: Normal
author: "$(metadata.owner)"
ms.prod: "microsoft-identity-platform"
doc_type: "apiPageType"
---

# Add windowsManagementApp

Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Add windowsManagementApp by posting to the windowsManagementApp collection.

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

In the request body, supply JSON representation of the [windowsManagementApp](../resources/intune-windowsmanagementapp.md) object.

<!-- Actions and Functions -->

<!-- CRUD Methods -->

The following table shows the properties that are required when you create a windowsManagementApp object.

| Property         | Type   | Description                                                 |
| :--------------- | :----- | :---------------------------------------------------------- |
| availableVersion | String | Windows management app available version.                   |
| id               | String | Unique Identifier for the Windows management app Read-only. |

## Response

If successful, this method returns a `201 Created` response code and a windowsManagementApp object in the response body.

## Examples

### Request

<!-- {
  "blockType": "request",
  "name": "add_windowsmanagementapp"
}
-->

```http
POST https://graph.microsoft.com/beta/deviceAppManagement/windowsManagementApp

Content-Type: application/json
Content-Length: 95

{
  "@odata.type": "#microsoft.graph.windowsManagementApp",
  "availableVersion": "String"
}

```

### Response

**Note:** The response object shown here might be shortened for readability.

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.management.services.api.windowsManagementApp"
}
-->

```http
HTTP 1.1 201 Created

Content-Type: application/json
{
  "value": {
  "@odata.type": "#microsoft.graph.windowsManagementApp",
  "availableVersion": "String",
  "id": "String(identifier)"
}
}

```
