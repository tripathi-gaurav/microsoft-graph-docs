---
title: "Update userExperienceAnalyticsDevicePerformance"
description: ""
localization_priority: Normal
author: "$(metadata.owner)"
ms.prod: "microsoft-identity-platform"
doc_type: "apiPageType"
---

# Update userExperienceAnalyticsDevicePerformance

Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Update the properties of a userExperienceAnalyticsDevicePerformance object.

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

In the request body, supply JSON representation of the [userExperienceAnalyticsDevicePerformance](../resources/intune-userexperienceanalyticsdeviceperformance.md) object.

<!-- Actions and Functions -->

<!-- CRUD Methods -->

The following table shows the properties that are required when you create a userExperienceAnalyticsDevicePerformance object.

| Property                  | Type   | Description                                                                                       |
| :------------------------ | :----- | :------------------------------------------------------------------------------------------------ |
| averageBlueScreens        | Double | Average (mean) number of Blue Screens per device in the last 14 days. Valid values 0 to 9999999   |
| averageRestarts           | Double | Average (mean) number of Restarts per device in the last 14 days. Valid values 0 to 9999999       |
| blueScreenCount           | Int32  | Number of Blue Screens in the last 14 days. Valid values 0 to 9999999                             |
| bootScore                 | Int32  | The user experience analytics device boot score.                                                  |
| coreBootTimeInMs          | Int32  | The user experience analytics device core boot time in milliseconds.                              |
| coreLoginTimeInMs         | Int32  | The user experience analytics device core login time in milliseconds.                             |
| deviceCount               | Int64  | User experience analytics summarized device count.                                                |
| deviceName                | String | The user experience analytics device name.                                                        |
| diskType                  | String | The user experience analytics device disk type.                                                   |
| groupPolicyBootTimeInMs   | Int32  | The user experience analytics device group policy boot time in milliseconds.                      |
| groupPolicyLoginTimeInMs  | Int32  | The user experience analytics device group policy login time in milliseconds.                     |
| healthStatus              | String | The health state of the user experience analytics device.                                         |
| id                        | String | The unique identifier of the user experience analytics device boot performance device. Read-only. |
| loginScore                | Int32  | The user experience analytics device login score.                                                 |
| manufacturer              | String | The user experience analytics device manufacturer.                                                |
| model                     | String | The user experience analytics device model.                                                       |
| operatingSystemVersion    | String | The user experience analytics device Operating System version.                                    |
| responsiveDesktopTimeInMs | Int32  | The user experience analytics responsive desktop time in milliseconds.                            |
| restartCount              | Int32  | Number of Restarts in the last 14 days. Valid values 0 to 9999999                                 |

## Response

If successful, this method returns a `200 OK` response code and a userExperienceAnalyticsDevicePerformance object in the response body.

## Examples

### Request

<!-- {
  "blockType": "request",
  "name": "update_userexperienceanalyticsdeviceperformance"
}
-->

```http
PATCH https://graph.microsoft.com/beta

Content-Type: application/json
Content-Length: 723

[
  {
    "@odata.type": "#microsoft.graph.userExperienceAnalyticsDevicePerformance",
    "averageBlueScreens": "Double",
    "averageRestarts": "Double",
    "blueScreenCount": "Int32",
    "bootScore": "Int32",
    "coreBootTimeInMs": "Int32",
    "coreLoginTimeInMs": "Int32",
    "deviceCount": "Int64",
    "deviceName": "String",
    "diskType": "String",
    "groupPolicyBootTimeInMs": "Int32",
    "groupPolicyLoginTimeInMs": "Int32",
    "healthStatus": "String",
    "id": "String(identifier)",
    "loginScore": "Int32",
    "manufacturer": "String",
    "model": "String",
    "operatingSystemVersion": "String",
    "responsiveDesktopTimeInMs": "Int32",
    "restartCount": "Int32"
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
    "@odata.type": "#microsoft.graph.userExperienceAnalyticsDevicePerformance",
    "averageBlueScreens": "Double",
    "averageRestarts": "Double",
    "blueScreenCount": "Int32",
    "bootScore": "Int32",
    "coreBootTimeInMs": "Int32",
    "coreLoginTimeInMs": "Int32",
    "deviceCount": "Int64",
    "deviceName": "String",
    "diskType": "String",
    "groupPolicyBootTimeInMs": "Int32",
    "groupPolicyLoginTimeInMs": "Int32",
    "healthStatus": "String",
    "id": "String(identifier)",
    "loginScore": "Int32",
    "manufacturer": "String",
    "model": "String",
    "operatingSystemVersion": "String",
    "responsiveDesktopTimeInMs": "Int32",
    "restartCount": "Int32"
  }
]
}

```
