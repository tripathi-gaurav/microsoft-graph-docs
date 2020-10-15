---
title: "Add runSummary"
description: ""
localization_priority: Normal
author: "$(metadata.owner)"
ms.prod: "microsoft-identity-platform"
doc_type: "apiPageType"
---

# Add runSummary

Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Add deviceManagementScriptRunSummary by posting to the deviceManagementScriptRunSummary collection.

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

In the request body, supply JSON representation of the [deviceManagementScriptRunSummary](../resources/intune-devicemanagementscriptrunsummary.md) object.

<!-- Actions and Functions -->

<!-- CRUD Methods -->

The following table shows the properties that are required when you create a deviceManagementScriptRunSummary object.

| Property           | Type   | Description                                                                                    |
| :----------------- | :----- | :--------------------------------------------------------------------------------------------- |
| errorDeviceCount   | Int32  | Error device count.                                                                            |
| errorUserCount     | Int32  | Error user count.                                                                              |
| id                 | String | Key of the device management script run summary entity. This property is read-only. Read-only. |
| successDeviceCount | Int32  | Success device count.                                                                          |
| successUserCount   | Int32  | Success user count.                                                                            |

## Response

If successful, this method returns a `201 Created` response code and a deviceManagementScriptRunSummary object in the response body.

## Examples

### Request

<!-- {
  "blockType": "request",
  "name": "add_runsummary"
}
-->

```http
POST https://graph.microsoft.com/beta/deviceManagement/deviceShellScripts/{id}/runSummary

Content-Type: application/json
Content-Length: 202

{
  "@odata.type": "#microsoft.graph.deviceManagementScriptRunSummary",
  "errorDeviceCount": "Int32",
  "errorUserCount": "Int32",
  "successDeviceCount": "Int32",
  "successUserCount": "Int32"
}

```

### Response

**Note:** The response object shown here might be shortened for readability.

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.management.services.api.deviceManagementScriptRunSummary"
}
-->

```http
HTTP 1.1 201 Created

Content-Type: application/json
{
  "value": {
  "@odata.type": "#microsoft.graph.deviceManagementScriptRunSummary",
  "errorDeviceCount": "Int32",
  "errorUserCount": "Int32",
  "id": "String(identifier)",
  "successDeviceCount": "Int32",
  "successUserCount": "Int32"
}
}

```
