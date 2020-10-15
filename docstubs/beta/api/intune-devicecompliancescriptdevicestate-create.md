---
title: "Create deviceComplianceScriptDeviceState"
description: ""
localization_priority: Normal
author: "$(metadata.owner)"
ms.prod: "microsoft-identity-platform"
doc_type: "apiPageType"
---

# Create deviceComplianceScriptDeviceState

Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Create a new deviceComplianceScriptDeviceState object.

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

In the request body, supply JSON representation of the [deviceComplianceScriptDeviceState](../resources/intune-devicecompliancescriptdevicestate.md) object.

<!-- Actions and Functions -->

<!-- CRUD Methods -->

The following table shows the properties that are required when you create a deviceComplianceScriptDeviceState object.

| Property                    | Type           | Description                                                                                     |
| :-------------------------- | :------------- | :---------------------------------------------------------------------------------------------- |
| detectionState              | String         | Detection state from the lastest device compliance script execution                             |
| expectedStateUpdateDateTime | DateTimeOffset | The next timestamp of when the device compliance script is expected to execute                  |
| id                          | String         | Key of the device compliance script device state entity. This property is read-only. Read-only. |
| lastStateUpdateDateTime     | DateTimeOffset | The last timestamp of when the device compliance script executed                                |
| lastSyncDateTime            | DateTimeOffset | The last time that Intune Managment Extension synced with Intune                                |
| scriptError                 | String         | Error from the detection script                                                                 |
| scriptOutput                | String         | Output of the detection script                                                                  |

## Response

If successful, this method returns a `201 Created` response code and a deviceComplianceScriptDeviceState object in the response body.

## Examples

### Request

<!-- {
  "blockType": "request",
  "name": "create_devicecompliancescriptdevicestate"
}
-->

```http
POST https://graph.microsoft.com/beta/deviceManagement/deviceComplianceScripts/{id}/deviceRunStates/{id}

Content-Type: application/json
Content-Length: 304

{
  "@odata.type": "#microsoft.graph.deviceComplianceScriptDeviceState",
  "detectionState": "String",
  "expectedStateUpdateDateTime": "DateTimeOffset",
  "lastStateUpdateDateTime": "DateTimeOffset",
  "lastSyncDateTime": "DateTimeOffset",
  "scriptError": "String",
  "scriptOutput": "String"
}

```

### Response

**Note:** The response object shown here might be shortened for readability.

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.management.services.api.deviceComplianceScriptDeviceState"
}
-->

```http
HTTP 1.1 201 Created

Content-Type: application/json
{
  "value": {
  "@odata.type": "#microsoft.graph.deviceComplianceScriptDeviceState",
  "detectionState": "String",
  "expectedStateUpdateDateTime": "DateTimeOffset",
  "id": "String(identifier)",
  "lastStateUpdateDateTime": "DateTimeOffset",
  "lastSyncDateTime": "DateTimeOffset",
  "scriptError": "String",
  "scriptOutput": "String"
}
}

```
