---
title: "Update runSummary"
description: ""
localization_priority: Normal
author: "$(metadata.owner)"
ms.prod: "microsoft-identity-platform"
doc_type: "apiPageType"
---

# Update runSummary

Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Update the properties of a deviceComplianceScriptRunSummary object.

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

In the request body, supply JSON representation of the [deviceComplianceScriptRunSummary](../resources/intune-devicecompliancescriptrunsummary.md) object.

<!-- Actions and Functions -->

<!-- CRUD Methods -->

The following table shows the properties that are required when you create a deviceComplianceScriptRunSummary object.

| Property                          | Type           | Description                                                                                                                                 |
| :-------------------------------- | :------------- | :------------------------------------------------------------------------------------------------------------------------------------------ |
| detectionScriptErrorDeviceCount   | Int32          | Number of devices on which the detection script execution encountered an error and did not complete. Valid values -2147483648 to 2147483647 |
| detectionScriptPendingDeviceCount | Int32          | Number of devices which have not yet run the latest version of the device compliance script. Valid values -2147483648 to 2147483647         |
| id                                | String         | Key of the device compliance script run summary entity. This property is read-only. Read-only.                                              |
| issueDetectedDeviceCount          | Int32          | Number of devices for which the detection script found an issue. Valid values -2147483648 to 2147483647                                     |
| lastScriptRunDateTime             | DateTimeOffset | Last run time for the script across all devices                                                                                             |
| noIssueDetectedDeviceCount        | Int32          | Number of devices for which the detection script did not find an issue and the device is healthy. Valid values -2147483648 to 2147483647    |

## Response

If successful, this method returns a `200 OK` response code and a deviceComplianceScriptRunSummary object in the response body.

## Examples

### Request

<!-- {
  "blockType": "request",
  "name": "update_runsummary"
}
-->

```http
PATCH https://graph.microsoft.com/beta/deviceManagement/deviceComplianceScripts/{id}/runSummary

Content-Type: application/json
Content-Length: 298

{
  "@odata.type": "#microsoft.graph.deviceComplianceScriptRunSummary",
  "detectionScriptErrorDeviceCount": "Int32",
  "detectionScriptPendingDeviceCount": "Int32",
  "issueDetectedDeviceCount": "Int32",
  "lastScriptRunDateTime": "DateTimeOffset",
  "noIssueDetectedDeviceCount": "Int32"
}

```

### Response

**Note:** The response object shown here might be shortened for readability.

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.management.services.api.deviceComplianceScriptRunSummary"
}
-->

```http
HTTP 1.1 200 OK

Content-Type: application/json
{
  "value": {
  "@odata.type": "#microsoft.graph.deviceComplianceScriptRunSummary",
  "detectionScriptErrorDeviceCount": "Int32",
  "detectionScriptPendingDeviceCount": "Int32",
  "id": "String(identifier)",
  "issueDetectedDeviceCount": "Int32",
  "lastScriptRunDateTime": "DateTimeOffset",
  "noIssueDetectedDeviceCount": "Int32"
}
}

```
