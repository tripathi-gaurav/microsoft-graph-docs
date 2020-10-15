---
title: "Create userExperienceAnalyticsDeviceStartupHistory"
description: ""
localization_priority: Normal
author: "$(metadata.owner)"
ms.prod: "microsoft-identity-platform"
doc_type: "apiPageType"
---

# Create userExperienceAnalyticsDeviceStartupHistory

Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Create a new userExperienceAnalyticsDeviceStartupHistory object.

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

In the request body, supply JSON representation of the [userExperienceAnalyticsDeviceStartupHistory](../resources/intune-userexperienceanalyticsdevicestartuphistory.md) object.

<!-- Actions and Functions -->

<!-- CRUD Methods -->

The following table shows the properties that are required when you create a userExperienceAnalyticsDeviceStartupHistory object.

| Property                  | Type           | Description                                                                                              |
| :------------------------ | :------------- | :------------------------------------------------------------------------------------------------------- |
| coreBootTimeInMs          | Int32          | The user experience analytics device core boot time in milliseconds.                                     |
| coreLoginTimeInMs         | Int32          | The user experience analytics device core login time in milliseconds.                                    |
| deviceId                  | String         | The user experience analytics device id.                                                                 |
| featureUpdateBootTimeInMs | Int32          | The user experience analytics device feature update time in milliseconds.                                |
| groupPolicyBootTimeInMs   | Int32          | The User experience analytics Device group policy boot time in milliseconds.                             |
| groupPolicyLoginTimeInMs  | Int32          | The User experience analytics Device group policy login time in milliseconds.                            |
| id                        | String         | The unique identifier of the user experience analytics device startup history. Read-only.                |
| isFeatureUpdate           | Boolean        | The user experience analytics device boot record is a feature update.                                    |
| isFirstLogin              | Boolean        | The user experience analytics device first login.                                                        |
| operatingSystemVersion    | String         | The user experience analytics device boot record's operating system version.                             |
| responsiveDesktopTimeInMs | Int32          | The user experience analytics responsive desktop time in milliseconds.                                   |
| restartCategory           | String         | OS restart category                                                                                      |
| restartFaultBucket        | String         | OS restart fault bucket. The fault bucket is used to find additional information about a system crash.   |
| restartStopCode           | String         | OS restart stop code. This shows the bug check code which can be used to look up the blue screen reason. |
| startTime                 | DateTimeOffset | The user experience analytics device boot start time.                                                    |
| totalBootTimeInMs         | Int32          | The user experience analytics device total boot time in milliseconds.                                    |
| totalLoginTimeInMs        | Int32          | The user experience analytics device total login time in milliseconds.                                   |

## Response

If successful, this method returns a `201 Created` response code and a userExperienceAnalyticsDeviceStartupHistory object in the response body.

## Examples

### Request

<!-- {
  "blockType": "request",
  "name": "create_userexperienceanalyticsdevicestartuphistory"
}
-->

```http
POST https://graph.microsoft.com/beta

Content-Type: application/json
Content-Length: 715

[
  {
    "@odata.type": "#microsoft.graph.userExperienceAnalyticsDeviceStartupHistory",
    "coreBootTimeInMs": "Int32",
    "coreLoginTimeInMs": "Int32",
    "deviceId": "String",
    "featureUpdateBootTimeInMs": "Int32",
    "groupPolicyBootTimeInMs": "Int32",
    "groupPolicyLoginTimeInMs": "Int32",
    "id": "String(identifier)",
    "isFeatureUpdate": "Boolean",
    "isFirstLogin": "Boolean",
    "operatingSystemVersion": "String",
    "responsiveDesktopTimeInMs": "Int32",
    "restartCategory": "String",
    "restartFaultBucket": "String",
    "restartStopCode": "String",
    "startTime": "DateTimeOffset",
    "totalBootTimeInMs": "Int32",
    "totalLoginTimeInMs": "Int32"
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
    "@odata.type": "#microsoft.graph.userExperienceAnalyticsDeviceStartupHistory",
    "coreBootTimeInMs": "Int32",
    "coreLoginTimeInMs": "Int32",
    "deviceId": "String",
    "featureUpdateBootTimeInMs": "Int32",
    "groupPolicyBootTimeInMs": "Int32",
    "groupPolicyLoginTimeInMs": "Int32",
    "id": "String(identifier)",
    "isFeatureUpdate": "Boolean",
    "isFirstLogin": "Boolean",
    "operatingSystemVersion": "String",
    "responsiveDesktopTimeInMs": "Int32",
    "restartCategory": "String",
    "restartFaultBucket": "String",
    "restartStopCode": "String",
    "startTime": "DateTimeOffset",
    "totalBootTimeInMs": "Int32",
    "totalLoginTimeInMs": "Int32"
  }
]
}

```
