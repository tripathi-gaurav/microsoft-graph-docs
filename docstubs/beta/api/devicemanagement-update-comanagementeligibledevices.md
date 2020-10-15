---
title: "Update comanagementEligibleDevices"
description: ""
localization_priority: Normal
author: "$(metadata.owner)"
ms.prod: "microsoft-identity-platform"
doc_type: "apiPageType"
---

# Update comanagementEligibleDevices

Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Update the properties of a comanagementEligibleDevice object.

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

In the request body, supply JSON representation of the [comanagementEligibleDevice](../resources/intune-comanagementeligibledevice.md) object.

<!-- Actions and Functions -->

<!-- CRUD Methods -->

The following table shows the properties that are required when you create a comanagementEligibleDevice object.

| Property                 | Type   | Description                         |
| :----------------------- | :----- | :---------------------------------- |
| clientRegistrationStatus | String | ClientRegistrationStatus            |
| deviceName               | String | DeviceName                          |
| deviceType               | String | DeviceType                          |
| entitySource             | Int32  | EntitySource                        |
| id                       | String | Unique Id for the device Read-only. |
| managementAgents         | String | ManagementAgents                    |
| managementState          | String | ManagementState                     |
| manufacturer             | String | Manufacturer                        |
| mdmStatus                | String | MDMStatus                           |
| model                    | String | Model                               |
| osDescription            | String | OSDescription                       |
| osVersion                | String | OSVersion                           |
| ownerType                | String | OwnerType                           |
| referenceId              | String | ReferenceId                         |
| serialNumber             | String | SerialNumber                        |
| status                   | String | ComanagementEligibleStatus          |
| upn                      | String | UPN                                 |
| userEmail                | String | UserEmail                           |
| userId                   | String | UserId                              |
| userName                 | String | UserName                            |

## Response

If successful, this method returns a `200 OK` response code and a comanagementEligibleDevice object in the response body.

## Examples

### Request

<!-- {
  "blockType": "request",
  "name": "update_comanagementeligibledevices"
}
-->

```http
PATCH https://graph.microsoft.com/beta

Content-Type: application/json
Content-Length: 672

[
  {
    "@odata.type": "#microsoft.graph.comanagementEligibleDevice",
    "clientRegistrationStatus": "String",
    "deviceName": "String",
    "deviceType": "String",
    "entitySource": "Int32",
    "id": "String(identifier)",
    "managementAgents": "String",
    "managementState": "String",
    "manufacturer": "String",
    "mdmStatus": "String",
    "model": "String",
    "osDescription": "String",
    "osVersion": "String",
    "ownerType": "String",
    "referenceId": "String",
    "serialNumber": "String",
    "status": "String",
    "upn": "String",
    "userEmail": "String",
    "userId": "String",
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
    "@odata.type": "#microsoft.graph.comanagementEligibleDevice",
    "clientRegistrationStatus": "String",
    "deviceName": "String",
    "deviceType": "String",
    "entitySource": "Int32",
    "id": "String(identifier)",
    "managementAgents": "String",
    "managementState": "String",
    "manufacturer": "String",
    "mdmStatus": "String",
    "model": "String",
    "osDescription": "String",
    "osVersion": "String",
    "ownerType": "String",
    "referenceId": "String",
    "serialNumber": "String",
    "status": "String",
    "upn": "String",
    "userEmail": "String",
    "userId": "String",
    "userName": "String"
  }
]
}

```
