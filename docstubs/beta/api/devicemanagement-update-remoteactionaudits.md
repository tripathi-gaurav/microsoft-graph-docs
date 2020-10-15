---
title: "Update remoteActionAudits"
description: ""
localization_priority: Normal
author: "$(metadata.owner)"
ms.prod: "microsoft-identity-platform"
doc_type: "apiPageType"
---

# Update remoteActionAudits

Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Update the properties of a remoteActionAudit object.

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

In the request body, supply JSON representation of the [remoteActionAudit](../resources/intune-remoteactionaudit.md) object.

<!-- Actions and Functions -->

<!-- CRUD Methods -->

The following table shows the properties that are required when you create a remoteActionAudit object.

| Property                     | Type           | Description                                                   |
| :--------------------------- | :------------- | :------------------------------------------------------------ |
| action                       | String         | The action name.                                              |
| actionState                  | String         | Action state.                                                 |
| deviceDisplayName            | String         | Intune device name.                                           |
| deviceIMEI                   | String         | IMEI of the device.                                           |
| deviceOwnerUserPrincipalName | String         | Upn of the device owner.                                      |
| id                           | String         | Report Id. Read-only.                                         |
| initiatedByUserPrincipalName | String         | User who initiated the device action, format is UPN.          |
| managedDeviceId              | String         | Action target.                                                |
| requestDateTime              | DateTimeOffset | Time when the action was issued, given in UTC.                |
| userName                     | String         | [deprecated] Please use InitiatedByUserPrincipalName instead. |

## Response

If successful, this method returns a `200 OK` response code and a remoteActionAudit object in the response body.

## Examples

### Request

<!-- {
  "blockType": "request",
  "name": "update_remoteactionaudits"
}
-->

```http
PATCH https://graph.microsoft.com/beta

Content-Type: application/json
Content-Length: 421

[
  {
    "@odata.type": "#microsoft.graph.remoteActionAudit",
    "action": "String",
    "actionState": "String",
    "deviceDisplayName": "String",
    "deviceIMEI": "String",
    "deviceOwnerUserPrincipalName": "String",
    "id": "String(identifier)",
    "initiatedByUserPrincipalName": "String",
    "managedDeviceId": "String",
    "requestDateTime": "DateTimeOffset",
    "userName": "String"
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
    "@odata.type": "#microsoft.graph.remoteActionAudit",
    "action": "String",
    "actionState": "String",
    "deviceDisplayName": "String",
    "deviceIMEI": "String",
    "deviceOwnerUserPrincipalName": "String",
    "id": "String(identifier)",
    "initiatedByUserPrincipalName": "String",
    "managedDeviceId": "String",
    "requestDateTime": "DateTimeOffset",
    "userName": "String"
  }
]
}

```
