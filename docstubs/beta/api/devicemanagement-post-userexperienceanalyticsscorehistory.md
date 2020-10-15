---
title: "Create userExperienceAnalyticsScoreHistory"
description: ""
localization_priority: Normal
author: "$(metadata.owner)"
ms.prod: "microsoft-identity-platform"
doc_type: "apiPageType"
---

# Create userExperienceAnalyticsScoreHistory

Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Create a new userExperienceAnalyticsScoreHistory object.

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

In the request body, supply JSON representation of the [userExperienceAnalyticsScoreHistory](../resources/intune-userexperienceanalyticsscorehistory.md) object.

<!-- Actions and Functions -->

<!-- CRUD Methods -->

The following table shows the properties that are required when you create a userExperienceAnalyticsScoreHistory object.

| Property                 | Type           | Description                                                                                                                        |
| :----------------------- | :------------- | :--------------------------------------------------------------------------------------------------------------------------------- |
| coreBootScore            | Int32          | The user experience analytics device core boot score. Score will be in the range 0-100, 100 is the ideal score.                    |
| coreSigninScore          | Int32          | The User experience analytics device core sign-in score. Score will be in the range 0-100, 100 is the ideal score.                 |
| id                       | String         | The unique identifier of the user experience analytics device startup process. Read-only.                                          |
| recommendedSoftwareScore | Int32          | The User experience analytics device core sign-in score. Score will be in the range 0-100, 100 is the ideal score.                 |
| restartScore             | Int32          | Restart score. Score will be in the range 0-100, 100 is the ideal score, 0 indicates excessive restarts. Valid values 0 to 9999999 |
| startupDateTime          | DateTimeOffset | The user experience analytics device startup date time.                                                                            |
| startupScore             | Int32          | User experience analytics device startup score. Score will be in the range 0-100, 100 is the ideal score.                          |

## Response

If successful, this method returns a `201 Created` response code and a userExperienceAnalyticsScoreHistory object in the response body.

## Examples

### Request

<!-- {
  "blockType": "request",
  "name": "create_userexperienceanalyticsscorehistory"
}
-->

```http
POST https://graph.microsoft.com/beta

Content-Type: application/json
Content-Length: 330

[
  {
    "@odata.type": "#microsoft.graph.userExperienceAnalyticsScoreHistory",
    "coreBootScore": "Int32",
    "coreSigninScore": "Int32",
    "id": "String(identifier)",
    "recommendedSoftwareScore": "Int32",
    "restartScore": "Int32",
    "startupDateTime": "DateTimeOffset",
    "startupScore": "Int32"
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
    "@odata.type": "#microsoft.graph.userExperienceAnalyticsScoreHistory",
    "coreBootScore": "Int32",
    "coreSigninScore": "Int32",
    "id": "String(identifier)",
    "recommendedSoftwareScore": "Int32",
    "restartScore": "Int32",
    "startupDateTime": "DateTimeOffset",
    "startupScore": "Int32"
  }
]
}

```
