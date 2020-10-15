---
title: "Update userExperienceAnalyticsAppHealthOSVersionPerformance"
description: ""
localization_priority: Normal
author: "$(metadata.owner)"
ms.prod: "microsoft-identity-platform"
doc_type: "apiPageType"
---

# Update userExperienceAnalyticsAppHealthOSVersionPerformance

Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Update the properties of an userExperienceAnalyticsAppHealthOSVersionPerformance object.

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

In the request body, supply JSON representation of the userExperienceAnalyticsAppHealthOSVersionPerformance object.

<!-- Actions and Functions -->

<!-- CRUD Methods -->

The following table shows the properties that are required when you create an userExperienceAnalyticsAppHealthOSVersionPerformance object.

| Property                   | Type   | Description                                                                                          |
| :------------------------- | :----- | :--------------------------------------------------------------------------------------------------- |
| activeDeviceCount          | Int32  | The number of active devices for the OS version. Valid values -2147483648 to 2147483647              |
| id                         | String | The unique identifier of the user experience analytics OS version performance object. Read-only.     |
| meanTimeToFailureInMinutes | Int32  | The mean time to failure for the OS version in minutes. Valid values -2147483648 to 2147483647       |
| osBuildNumber              | String | The OS build number installed on the device.                                                         |
| osVersion                  | String | The OS version installed on the device.                                                              |
| osVersionAppHealthScore    | Double | The app health score of the OS version. Valid values -1.79769313486232E+308 to 1.79769313486232E+308 |
| osVersionAppHealthStatus   | String | The overall app health status of the OS version.                                                     |

## Response

If successful, this method returns a `200 OK` response code and an userExperienceAnalyticsAppHealthOSVersionPerformance object in the response body.

## Examples

### Request

<!-- {
  "blockType": "request",
  "name": "update_userexperienceanalyticsapphealthosversionperformance"
}
-->

```http
PATCH https://graph.microsoft.com/beta

Content-Type: application/json
Content-Length: 363

[
  {
    "@odata.type": "#microsoft.graph.userExperienceAnalyticsAppHealthOSVersionPerformance",
    "activeDeviceCount": "Int32",
    "id": "String(identifier)",
    "meanTimeToFailureInMinutes": "Int32",
    "osBuildNumber": "String",
    "osVersion": "String",
    "osVersionAppHealthScore": "Double",
    "osVersionAppHealthStatus": "String"
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
    "@odata.type": "#microsoft.graph.userExperienceAnalyticsAppHealthOSVersionPerformance",
    "activeDeviceCount": "Int32",
    "id": "String(identifier)",
    "meanTimeToFailureInMinutes": "Int32",
    "osBuildNumber": "String",
    "osVersion": "String",
    "osVersionAppHealthScore": "Double",
    "osVersionAppHealthStatus": "String"
  }
]
}

```
