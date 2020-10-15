---
title: "Create deviceHealthScriptRunSummary"
description: ""
localization_priority: Normal
author: "$(metadata.owner)"
ms.prod: "microsoft-identity-platform"
doc_type: "apiPageType"
---

# Create deviceHealthScriptRunSummary

Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Create a new deviceHealthScriptRunSummary object.

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

In the request body, supply JSON representation of the [deviceHealthScriptRunSummary](../resources/intune-devicehealthscriptrunsummary.md) object.

<!-- Actions and Functions -->

<!-- CRUD Methods -->

The following table shows the properties that are required when you create a deviceHealthScriptRunSummary object.

| Property                             | Type           | Description                                                                                                       |
| :----------------------------------- | :------------- | :---------------------------------------------------------------------------------------------------------------- |
| detectionScriptErrorDeviceCount      | Int32          | Number of devices on which the detection script execution encountered an error and did not complete               |
| detectionScriptPendingDeviceCount    | Int32          | Number of devices which have not yet run the latest version of the device health script                           |
| id                                   | String         | Key of the device health script run summary entity. This property is read-only. Read-only.                        |
| issueDetectedDeviceCount             | Int32          | Number of devices for which the detection script found an issue                                                   |
| issueRemediatedCumulativeDeviceCount | Int32          | Number of devices that were remediated over the last 30 days                                                      |
| issueRemediatedDeviceCount           | Int32          | Number of devices for which the remediation script was able to resolve the detected issue                         |
| issueReoccurredDeviceCount           | Int32          | Number of devices for which the remediation script executed successfully but failed to resolve the detected issue |
| lastScriptRunDateTime                | DateTimeOffset | Last run time for the script across all devices                                                                   |
| noIssueDetectedDeviceCount           | Int32          | Number of devices for which the detection script did not find an issue and the device is healthy                  |
| remediationScriptErrorDeviceCount    | Int32          | Number of devices for which the remediation script execution encountered an error and did not complete            |
| remediationSkippedDeviceCount        | Int32          | Number of devices for which remediation was skipped                                                               |

## Response

If successful, this method returns a `201 Created` response code and a deviceHealthScriptRunSummary object in the response body.

## Examples

### Request

<!-- {
  "blockType": "request",
  "name": "create_devicehealthscriptrunsummary"
}
-->

```http
POST https://graph.microsoft.com/beta/deviceManagement/deviceHealthScripts/{id}/runSummary

Content-Type: application/json
Content-Length: 524

{
  "@odata.type": "#microsoft.graph.deviceHealthScriptRunSummary",
  "detectionScriptErrorDeviceCount": "Int32",
  "detectionScriptPendingDeviceCount": "Int32",
  "issueDetectedDeviceCount": "Int32",
  "issueRemediatedCumulativeDeviceCount": "Int32",
  "issueRemediatedDeviceCount": "Int32",
  "issueReoccurredDeviceCount": "Int32",
  "lastScriptRunDateTime": "DateTimeOffset",
  "noIssueDetectedDeviceCount": "Int32",
  "remediationScriptErrorDeviceCount": "Int32",
  "remediationSkippedDeviceCount": "Int32"
}

```

### Response

**Note:** The response object shown here might be shortened for readability.

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.management.services.api.deviceHealthScriptRunSummary"
}
-->

```http
HTTP 1.1 201 Created

Content-Type: application/json
{
  "value": {
  "@odata.type": "#microsoft.graph.deviceHealthScriptRunSummary",
  "detectionScriptErrorDeviceCount": "Int32",
  "detectionScriptPendingDeviceCount": "Int32",
  "id": "String(identifier)",
  "issueDetectedDeviceCount": "Int32",
  "issueRemediatedCumulativeDeviceCount": "Int32",
  "issueRemediatedDeviceCount": "Int32",
  "issueReoccurredDeviceCount": "Int32",
  "lastScriptRunDateTime": "DateTimeOffset",
  "noIssueDetectedDeviceCount": "Int32",
  "remediationScriptErrorDeviceCount": "Int32",
  "remediationSkippedDeviceCount": "Int32"
}
}

```
