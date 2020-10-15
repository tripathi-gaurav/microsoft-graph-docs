---
title: "Create userExperienceAnalyticsBaselines"
description: ""
localization_priority: Normal
author: "$(metadata.owner)"
ms.prod: "microsoft-identity-platform"
doc_type: "apiPageType"
---

# Create userExperienceAnalyticsBaselines

Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Create a new userExperienceAnalyticsBaseline object.

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

In the request body, supply JSON representation of the [userExperienceAnalyticsBaseline](../resources/intune-userexperienceanalyticsbaseline.md) object.

<!-- Actions and Functions -->

<!-- CRUD Methods -->

The following table shows the properties that are required when you create a userExperienceAnalyticsBaseline object.

| Property        | Type           | Description                                                                               |
| :-------------- | :------------- | :---------------------------------------------------------------------------------------- |
| createdDateTime | DateTimeOffset | The date the custom baseline was created.                                                 |
| displayName     | String         | The name of the user experience analytics baseline.                                       |
| id              | String         | The unique identifier of the user experience analytics baseline. Read-only.               |
| isBuiltIn       | Boolean        | Signifies if the current baseline is the commercial median baseline or a custom baseline. |
| overallScore    | Int32          | The overall score of the user experience analytics baseline.                              |

## Response

If successful, this method returns a `201 Created` response code and a userExperienceAnalyticsBaseline object in the response body.

## Examples

### Request

<!-- {
  "blockType": "request",
  "name": "create_userexperienceanalyticsbaselines"
}
-->

```http
POST https://graph.microsoft.com/beta

Content-Type: application/json
Content-Length: 249

[
  {
    "@odata.type": "#microsoft.graph.userExperienceAnalyticsBaseline",
    "createdDateTime": "DateTimeOffset",
    "displayName": "String",
    "id": "String(identifier)",
    "isBuiltIn": "Boolean",
    "overallScore": "Int32"
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
    "@odata.type": "#microsoft.graph.userExperienceAnalyticsBaseline",
    "createdDateTime": "DateTimeOffset",
    "displayName": "String",
    "id": "String(identifier)",
    "isBuiltIn": "Boolean",
    "overallScore": "Int32"
  }
]
}

```
