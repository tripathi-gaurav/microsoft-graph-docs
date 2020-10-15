---
title: "Update userExperienceAnalyticsAppHealthDevicePerformance"
description: ""
localization_priority: Normal
author: "$(metadata.owner)"
ms.prod: "microsoft-identity-platform"
doc_type: "apiPageType"
---

# Update userExperienceAnalyticsAppHealthDevicePerformance

Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Update the properties of an userExperienceAnalyticsAppHealthDevicePerformance object.

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

In the request body, supply JSON representation of the userExperienceAnalyticsAppHealthDevicePerformance object.

<!-- Actions and Functions -->

<!-- CRUD Methods -->

The following table shows the properties that are required when you create an userExperienceAnalyticsAppHealthDevicePerformance object.

| Property                   | Type   | Description                                                                                      |
| :------------------------- | :----- | :----------------------------------------------------------------------------------------------- |
| appCrashCount              | Int32  | The number of app crashes for the device. Valid values -2147483648 to 2147483647                 |
| appHangCount               | Int32  | The number of app hangs for the device. Valid values -2147483648 to 2147483647                   |
| crashedAppCount            | Int32  | The number of distinct app crashes for the device. Valid values -2147483648 to 2147483647        |
| deviceAppHealthScore       | Double | The app health score of the device. Valid values -1.79769313486232E+308 to 1.79769313486232E+308 |
| deviceAppHealthStatus      | String | The overall app health status of the device.                                                     |
| deviceDisplayName          | String | The name of the device.                                                                          |
| deviceId                   | String | The id of the device.                                                                            |
| deviceManufacturer         | String | The manufacturer name of the device.                                                             |
| deviceModel                | String | The model name of the device.                                                                    |
| id                         | String | The unique identifier of the user experience analytics device performance object. Read-only.     |
| meanTimeToFailureInMinutes | Int32  | The mean time to failure for the device in minutes. Valid values -2147483648 to 2147483647       |

## Response

If successful, this method returns a `200 OK` response code and an userExperienceAnalyticsAppHealthDevicePerformance object in the response body.

## Examples

### Request

<!-- {
  "blockType": "request",
  "name": "update_userexperienceanalyticsapphealthdeviceperformance"
}
-->

```http
PATCH https://graph.microsoft.com/beta

Content-Type: application/json
Content-Length: 483

[
  {
    "@odata.type": "#microsoft.graph.userExperienceAnalyticsAppHealthDevicePerformance",
    "appCrashCount": "Int32",
    "appHangCount": "Int32",
    "crashedAppCount": "Int32",
    "deviceAppHealthScore": "Double",
    "deviceAppHealthStatus": "String",
    "deviceDisplayName": "String",
    "deviceId": "String",
    "deviceManufacturer": "String",
    "deviceModel": "String",
    "id": "String(identifier)",
    "meanTimeToFailureInMinutes": "Int32"
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
    "@odata.type": "#microsoft.graph.userExperienceAnalyticsAppHealthDevicePerformance",
    "appCrashCount": "Int32",
    "appHangCount": "Int32",
    "crashedAppCount": "Int32",
    "deviceAppHealthScore": "Double",
    "deviceAppHealthStatus": "String",
    "deviceDisplayName": "String",
    "deviceId": "String",
    "deviceManufacturer": "String",
    "deviceModel": "String",
    "id": "String(identifier)",
    "meanTimeToFailureInMinutes": "Int32"
  }
]
}

```
