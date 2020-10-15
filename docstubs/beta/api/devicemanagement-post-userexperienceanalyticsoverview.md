---
title: "Create userExperienceAnalyticsOverview"
description: ""
localization_priority: Normal
author: "$(metadata.owner)"
ms.prod: "microsoft-identity-platform"
doc_type: "apiPageType"
---

# Create userExperienceAnalyticsOverview

Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Create a new userExperienceAnalyticsOverview object.

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

In the request body, supply JSON representation of the [userExperienceAnalyticsOverview](../resources/intune-userexperienceanalyticsoverview.md) object.

<!-- Actions and Functions -->

<!-- CRUD Methods -->

The following table shows the properties that are required when you create a userExperienceAnalyticsOverview object.

| Property                          | Type                                                                                        | Description                                                                           |
| :-------------------------------- | :------------------------------------------------------------------------------------------ | :------------------------------------------------------------------------------------ |
| bestPracticesHealthState          | String                                                                                      | The current health state of the user experience analytics 'BestPractices' category.   |
| bestPracticesOverallScore         | Int32                                                                                       | The user experience analytics best practices overall score.                           |
| deviceBootPerformanceHealthState  | String                                                                                      | The current health state of the user experience analytics 'BootPerformance' category. |
| deviceBootPerformanceOverallScore | Int32                                                                                       | The user experience analytics device boot performance overall score.                  |
| id                                | String                                                                                      | The unique identifier of the user experience analytics overview. Read-only.           |
| insights                          | [userExperienceAnalyticsInsight](../resources/userexperienceanalyticsinsight.md) collection | The user experience analytics insights.                                               |
| overallScore                      | Int32                                                                                       | The user experience analytics overall score.                                          |
| state                             | String                                                                                      | The current health state of the user experience analytics overview.                   |

## Response

If successful, this method returns a `201 Created` response code and a userExperienceAnalyticsOverview object in the response body.

## Examples

### Request

<!-- {
  "blockType": "request",
  "name": "create_userexperienceanalyticsoverview"
}
-->

```http
POST https://graph.microsoft.com/beta/deviceManagement/userExperienceAnalyticsOverview

Content-Type: application/json
Content-Length: 668

{
  "@odata.type": "#microsoft.graph.userExperienceAnalyticsOverview",
  "bestPracticesHealthState": "String",
  "bestPracticesOverallScore": "Int32",
  "deviceBootPerformanceHealthState": "String",
  "deviceBootPerformanceOverallScore": "Int32",
  "insights": [
    {
      "@odata.type": "#microsoft.graph.userExperienceAnalyticsInsight",
      "insightId": "String",
      "severity": "String",
      "userExperienceAnalyticsMetricId": "String",
      "values": [
        {
          "@odata.type": "#microsoft.graph.insightValueDouble",
          "value": "Double"
        }
      ]
    }
  ],
  "overallScore": "Int32",
  "state": "String"
}

```

### Response

**Note:** The response object shown here might be shortened for readability.

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.management.services.api.userExperienceAnalyticsOverview"
}
-->

```http
HTTP 1.1 201 Created

Content-Type: application/json
{
  "value": {
  "@odata.type": "#microsoft.graph.userExperienceAnalyticsOverview",
  "bestPracticesHealthState": "String",
  "bestPracticesOverallScore": "Int32",
  "deviceBootPerformanceHealthState": "String",
  "deviceBootPerformanceOverallScore": "Int32",
  "id": "String(identifier)",
  "insights": [
    {
      "@odata.type": "#microsoft.graph.userExperienceAnalyticsInsight",
      "insightId": "String",
      "severity": "String",
      "userExperienceAnalyticsMetricId": "String",
      "values": [
        {
          "@odata.type": "#microsoft.graph.insightValueDouble",
          "value": "Double"
        }
      ]
    }
  ],
  "overallScore": "Int32",
  "state": "String"
}
}

```
