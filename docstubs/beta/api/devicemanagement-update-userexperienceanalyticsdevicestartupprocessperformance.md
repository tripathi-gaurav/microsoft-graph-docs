---
title: "Update userExperienceAnalyticsDeviceStartupProcessPerformance"
description: ""
localization_priority: Normal
author: "$(metadata.owner)"
ms.prod: "microsoft-identity-platform"
doc_type: "apiPageType"
---

# Update userExperienceAnalyticsDeviceStartupProcessPerformance

Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Update the properties of a userExperienceAnalyticsDeviceStartupProcessPerformance object.

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

In the request body, supply JSON representation of the [userExperienceAnalyticsDeviceStartupProcessPerformance](../resources/intune-userexperienceanalyticsdevicestartupprocessperformance.md) object.

<!-- Actions and Functions -->

<!-- CRUD Methods -->

The following table shows the properties that are required when you create a userExperienceAnalyticsDeviceStartupProcessPerformance object.

| Property         | Type   | Description                                                                                           |
| :--------------- | :----- | :---------------------------------------------------------------------------------------------------- |
| deviceCount      | Int64  | User experience analytics device startup process summarized count.                                    |
| id               | String | The unique identifier of the user experience analytics device startup process performance. Read-only. |
| medianImpactInMs | Int32  | User experience analytics device startup process median impact in milliseconds.                       |
| processName      | String | User experience analytics device startup process name.                                                |
| productName      | String | The user experience analytics device startup process product name.                                    |
| publisher        | String | The User experience analytics device startup process publisher.                                       |
| totalImpactInMs  | Int32  | User experience analytics device startup process total impact in milliseconds.                        |

## Response

If successful, this method returns a `200 OK` response code and a userExperienceAnalyticsDeviceStartupProcessPerformance object in the response body.

## Examples

### Request

<!-- {
  "blockType": "request",
  "name": "update_userexperienceanalyticsdevicestartupprocessperformance"
}
-->

```http
PATCH https://graph.microsoft.com/beta

Content-Type: application/json
Content-Length: 325

[
  {
    "@odata.type": "#microsoft.graph.userExperienceAnalyticsDeviceStartupProcessPerformance",
    "deviceCount": "Int64",
    "id": "String(identifier)",
    "medianImpactInMs": "Int32",
    "processName": "String",
    "productName": "String",
    "publisher": "String",
    "totalImpactInMs": "Int32"
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
    "@odata.type": "#microsoft.graph.userExperienceAnalyticsDeviceStartupProcessPerformance",
    "deviceCount": "Int64",
    "id": "String(identifier)",
    "medianImpactInMs": "Int32",
    "processName": "String",
    "productName": "String",
    "publisher": "String",
    "totalImpactInMs": "Int32"
  }
]
}

```
