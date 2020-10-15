---
title: "Create userExperienceAnalyticsAppHealthApplicationPerformanceByAppVersion"
description: ""
localization_priority: Normal
author: "$(metadata.owner)"
ms.prod: "microsoft-identity-platform"
doc_type: "apiPageType"
---

# Create userExperienceAnalyticsAppHealthApplicationPerformanceByAppVersion

Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Create a new userExperienceAnalyticsAppHealthAppPerformanceByAppVersion object.

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

In the request body, supply JSON representation of the userExperienceAnalyticsAppHealthAppPerformanceByAppVersion object.

<!-- Actions and Functions -->

<!-- CRUD Methods -->

The following table shows the properties that are required when you create an userExperienceAnalyticsAppHealthAppPerformanceByAppVersion object.

| Property                   | Type   | Description                                                                                |
| :------------------------- | :----- | :----------------------------------------------------------------------------------------- |
| appCrashCount              | Int32  | The number of crashes for the app. Valid values -2147483648 to 2147483647                  |
| appDisplayName             | String | The friendly name of the application.                                                      |
| appName                    | String | The name of the application.                                                               |
| appPublisher               | String | The publisher of the application.                                                          |
| appUsageDuration           | Int32  | The total usage time of the application in minutes. Valid values -2147483648 to 2147483647 |
| appVersion                 | String | The version of the application.                                                            |
| id                         | String | The unique identifier of the user experience analytics app performance object. Read-only.  |
| meanTimeToFailureInMinutes | Int32  | The mean time to failure for the app in minutes. Valid values -2147483648 to 2147483647    |

## Response

If successful, this method returns a `201 Created` response code and an userExperienceAnalyticsAppHealthAppPerformanceByAppVersion object in the response body.

## Examples

### Request

<!-- {
  "blockType": "request",
  "name": "create_userexperienceanalyticsapphealthapplicationperformancebyappversion"
}
-->

```http
POST https://graph.microsoft.com/beta

Content-Type: application/json
Content-Length: 373

[
  {
    "@odata.type": "#microsoft.graph.userExperienceAnalyticsAppHealthAppPerformanceByAppVersion",
    "appCrashCount": "Int32",
    "appDisplayName": "String",
    "appName": "String",
    "appPublisher": "String",
    "appUsageDuration": "Int32",
    "appVersion": "String",
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
HTTP 1.1 201 Created

Content-Type: application/json
{
  "value": [
  {
    "@odata.type": "#microsoft.graph.userExperienceAnalyticsAppHealthAppPerformanceByAppVersion",
    "appCrashCount": "Int32",
    "appDisplayName": "String",
    "appName": "String",
    "appPublisher": "String",
    "appUsageDuration": "Int32",
    "appVersion": "String",
    "id": "String(identifier)",
    "meanTimeToFailureInMinutes": "Int32"
  }
]
}

```
