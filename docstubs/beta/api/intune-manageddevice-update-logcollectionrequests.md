---
title: "Update logCollectionRequests"
description: ""
localization_priority: Normal
author: "$(metadata.owner)"
ms.prod: "microsoft-identity-platform"
doc_type: "apiPageType"
---

# Update logCollectionRequests

Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Update the properties of a deviceLogCollectionResponse object.

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

In the request body, supply JSON representation of the [deviceLogCollectionResponse](../resources/intune-devicelogcollectionresponse.md) object.

<!-- Actions and Functions -->

<!-- CRUD Methods -->

The following table shows the properties that are required when you create a deviceLogCollectionResponse object.

| Property                     | Type           | Description                                                                        |
| :--------------------------- | :------------- | :--------------------------------------------------------------------------------- |
| errorCode                    | Int64          | The error code, if any. Valid values -9.22337203685478E+18 to 9.22337203685478E+18 |
| expirationDateTimeUTC        | DateTimeOffset | The DateTime of the expiration of the logs                                         |
| id                           | String         | The unique identifier in the form of tenantId_deviceId_requestId Read-only.        |
| initiatedByUserPrincipalName | String         | The UPN for who initiated the request                                              |
| managedDeviceId              | Guid           | The device Id                                                                      |
| receivedDateTimeUTC          | DateTimeOffset | The DateTime the request was received                                              |
| requestedDateTimeUTC         | DateTimeOffset | The DateTime of the request                                                        |
| size                         | Double         | The size of the logs. Valid values -1.79769313486232E+308 to 1.79769313486232E+308 |
| status                       | String         | The status of the log collection request                                           |

## Response

If successful, this method returns a `200 OK` response code and a deviceLogCollectionResponse object in the response body.

## Examples

### Request

<!-- {
  "blockType": "request",
  "name": "update_logcollectionrequests"
}
-->

```http
PATCH https://graph.microsoft.com/beta

Content-Type: application/json
Content-Length: 409

[
  {
    "@odata.type": "#microsoft.graph.deviceLogCollectionResponse",
    "errorCode": "Int64",
    "expirationDateTimeUTC": "DateTimeOffset",
    "id": "String(identifier)",
    "initiatedByUserPrincipalName": "String",
    "managedDeviceId": "Guid",
    "receivedDateTimeUTC": "DateTimeOffset",
    "requestedDateTimeUTC": "DateTimeOffset",
    "size": "Double",
    "status": "String"
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
    "@odata.type": "#microsoft.graph.deviceLogCollectionResponse",
    "errorCode": "Int64",
    "expirationDateTimeUTC": "DateTimeOffset",
    "id": "String(identifier)",
    "initiatedByUserPrincipalName": "String",
    "managedDeviceId": "Guid",
    "receivedDateTimeUTC": "DateTimeOffset",
    "requestedDateTimeUTC": "DateTimeOffset",
    "size": "Double",
    "status": "String"
  }
]
}

```
