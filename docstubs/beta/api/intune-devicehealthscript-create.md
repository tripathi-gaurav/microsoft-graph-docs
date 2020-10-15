---
title: "Create deviceHealthScript"
description: ""
localization_priority: Normal
author: "$(metadata.owner)"
ms.prod: "microsoft-identity-platform"
doc_type: "apiPageType"
---

# Create deviceHealthScript

Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Create a new deviceHealthScript object.

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

In the request body, supply JSON representation of the [deviceHealthScript](../resources/intune-devicehealthscript.md) object.

<!-- Actions and Functions -->

<!-- CRUD Methods -->

The following table shows the properties that are required when you create a deviceHealthScript object.

| Property                    | Type                                                                                  | Description                                                                              |
| :-------------------------- | :------------------------------------------------------------------------------------ | :--------------------------------------------------------------------------------------- |
| createdDateTime             | DateTimeOffset                                                                        | The timestamp of when the device health script was created. This property is read-only.  |
| description                 | String                                                                                | Description of the device health script                                                  |
| detectionScriptContent      | Binary                                                                                | The entire content of the detection powershell script                                    |
| detectionScriptParameters   | [deviceHealthScriptParameter](../resources/devicehealthscriptparameter.md) collection | List of ComplexType DetectionScriptParameters objects.                                   |
| displayName                 | String                                                                                | Name of the device health script                                                         |
| enforceSignatureCheck       | Boolean                                                                               | Indicate whether the script signature needs be checked                                   |
| highestAvailableVersion     | String                                                                                | Highest available version for a Microsoft Proprietary script                             |
| id                          | String                                                                                | Unique Identifier for the device health script Read-only.                                |
| isGlobalScript              | Boolean                                                                               | Determines if this is Microsoft Proprietary Script. Proprietary scripts are read-only    |
| lastModifiedDateTime        | DateTimeOffset                                                                        | The timestamp of when the device health script was modified. This property is read-only. |
| publisher                   | String                                                                                | Name of the device health script publisher                                               |
| remediationScriptContent    | Binary                                                                                | The entire content of the remediation powershell script                                  |
| remediationScriptParameters | [deviceHealthScriptParameter](../resources/devicehealthscriptparameter.md) collection | List of ComplexType RemediationScriptParameters objects.                                 |
| roleScopeTagIds             | String collection                                                                     | List of Scope Tag IDs for the device health script                                       |
| runAs32Bit                  | Boolean                                                                               | Indicate whether PowerShell script(s) should run as 32-bit                               |
| runAsAccount                | String                                                                                | Indicates the type of execution context                                                  |
| version                     | String                                                                                | Version of the device health script                                                      |

## Response

If successful, this method returns a `201 Created` response code and a deviceHealthScript object in the response body.

## Examples

### Request

<!-- {
  "blockType": "request",
  "name": "create_devicehealthscript"
}
-->

```http
POST https://graph.microsoft.com/beta/deviceManagement/deviceHealthScripts/{id}

Content-Type: application/json
Content-Length: 1159

{
  "@odata.type": "#microsoft.graph.deviceHealthScript",
  "createdDateTime": "DateTimeOffset",
  "description": "String",
  "detectionScriptContent": "Binary",
  "detectionScriptParameters": [
    {
      "@odata.type": "#microsoft.graph.deviceHealthScriptBooleanParameter",
      "applyDefaultValueWhenNotAssigned": "Boolean",
      "defaultValue": "Boolean",
      "description": "String",
      "isRequired": "Boolean",
      "name": "String"
    }
  ],
  "displayName": "String",
  "enforceSignatureCheck": "Boolean",
  "highestAvailableVersion": "String",
  "isGlobalScript": "Boolean",
  "lastModifiedDateTime": "DateTimeOffset",
  "publisher": "String",
  "remediationScriptContent": "Binary",
  "remediationScriptParameters": [
    {
      "@odata.type": "#microsoft.graph.deviceHealthScriptBooleanParameter",
      "applyDefaultValueWhenNotAssigned": "Boolean",
      "defaultValue": "Boolean",
      "description": "String",
      "isRequired": "Boolean",
      "name": "String"
    }
  ],
  "roleScopeTagIds": [
    "String"
  ],
  "runAs32Bit": "Boolean",
  "runAsAccount": "String",
  "version": "String"
}

```

### Response

**Note:** The response object shown here might be shortened for readability.

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.management.services.api.deviceHealthScript"
}
-->

```http
HTTP 1.1 201 Created

Content-Type: application/json
{
  "value": {
  "@odata.type": "#microsoft.graph.deviceHealthScript",
  "createdDateTime": "DateTimeOffset",
  "description": "String",
  "detectionScriptContent": "Binary",
  "detectionScriptParameters": [
    {
      "@odata.type": "#microsoft.graph.deviceHealthScriptBooleanParameter",
      "applyDefaultValueWhenNotAssigned": "Boolean",
      "defaultValue": "Boolean",
      "description": "String",
      "isRequired": "Boolean",
      "name": "String"
    }
  ],
  "displayName": "String",
  "enforceSignatureCheck": "Boolean",
  "highestAvailableVersion": "String",
  "id": "String(identifier)",
  "isGlobalScript": "Boolean",
  "lastModifiedDateTime": "DateTimeOffset",
  "publisher": "String",
  "remediationScriptContent": "Binary",
  "remediationScriptParameters": [
    {
      "@odata.type": "#microsoft.graph.deviceHealthScriptBooleanParameter",
      "applyDefaultValueWhenNotAssigned": "Boolean",
      "defaultValue": "Boolean",
      "description": "String",
      "isRequired": "Boolean",
      "name": "String"
    }
  ],
  "roleScopeTagIds": [
    "String"
  ],
  "runAs32Bit": "Boolean",
  "runAsAccount": "String",
  "version": "String"
}
}

```
