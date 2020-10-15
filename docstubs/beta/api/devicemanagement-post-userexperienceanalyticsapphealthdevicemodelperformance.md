---
title: "Create userExperienceAnalyticsAppHealthDeviceModelPerformance"
description: ""
localization_priority: Normal
author: "$(metadata.owner)"
ms.prod: "microsoft-identity-platform"
doc_type: "apiPageType"
---

# Create userExperienceAnalyticsAppHealthDeviceModelPerformance

Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Create a new userExperienceAnalyticsAppHealthDeviceModelPerformance object.

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

In the request body, supply JSON representation of the userExperienceAnalyticsAppHealthDeviceModelPerformance object.

<!-- Actions and Functions -->

<!-- CRUD Methods -->

The following table shows the properties that are required when you create an userExperienceAnalyticsAppHealthDeviceModelPerformance object.

| Property                   | Type   | Description                                                                                            |
| :------------------------- | :----- | :----------------------------------------------------------------------------------------------------- |
| activeDeviceCount          | Int32  | The number of active devices for the model. Valid values -2147483648 to 2147483647                     |
| deviceManufacturer         | String | The manufacturer name of the device.                                                                   |
| deviceModel                | String | The model name of the device.                                                                          |
| id                         | String | The unique identifier of the user experience analytics device model performance object. Read-only.     |
| meanTimeToFailureInMinutes | Int32  | The mean time to failure for the model device in minutes. Valid values -2147483648 to 2147483647       |
| modelAppHealthScore        | Double | The app health score of the device model. Valid values -1.79769313486232E+308 to 1.79769313486232E+308 |
| modelAppHealthStatus       | String | The overall app health status of the device model.                                                     |

## Response

If successful, this method returns a `201 Created` response code and an userExperienceAnalyticsAppHealthDeviceModelPerformance object in the response body.

## Examples

### Request

<!-- {
  "blockType": "request",
  "name": "create_userexperienceanalyticsapphealthdevicemodelperformance"
}
-->

```http
POST https://graph.microsoft.com/beta

Content-Type: application/json
Content-Length: 364

[
  {
    "@odata.type": "#microsoft.graph.userExperienceAnalyticsAppHealthDeviceModelPerformance",
    "activeDeviceCount": "Int32",
    "deviceManufacturer": "String",
    "deviceModel": "String",
    "id": "String(identifier)",
    "meanTimeToFailureInMinutes": "Int32",
    "modelAppHealthScore": "Double",
    "modelAppHealthStatus": "String"
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
HTTP 1.1 201 Created

Content-Type: application/json
{
  "value": [
  {
    "@odata.type": "#microsoft.graph.userExperienceAnalyticsAppHealthDeviceModelPerformance",
    "activeDeviceCount": "Int32",
    "deviceManufacturer": "String",
    "deviceModel": "String",
    "id": "String(identifier)",
    "meanTimeToFailureInMinutes": "Int32",
    "modelAppHealthScore": "Double",
    "modelAppHealthStatus": "String"
  }
]
}

```
