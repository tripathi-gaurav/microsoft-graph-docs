---
title: "Update deviceManagement"
description: ""
localization_priority: Normal
author: "$(metadata.owner)"
ms.prod: "microsoft-identity-platform"
doc_type: "apiPageType"
---

# Update deviceManagement

Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Update the properties of a deviceManagement object.

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

In the request body, supply JSON representation of the [deviceManagement](../resources/intune-devicemanagement.md) object.

<!-- Actions and Functions -->

<!-- CRUD Methods -->

The following table shows the properties that are required when you create a deviceManagement object.

| Property                        | Type                                                                               | Description                                                |
| :------------------------------ | :--------------------------------------------------------------------------------- | :--------------------------------------------------------- |
| accountMoveCompletionDateTime   | DateTimeOffset                                                                     | The date & time when tenant data moved between scaleunits. |
| adminConsent                    | [adminConsent](../resources/adminconsent.md)                                       | Admin consent information.                                 |
| deviceProtectionOverview        | [deviceProtectionOverview](../resources/deviceprotectionoverview.md)               | Device protection overview.                                |
| id                              | String                                                                             | Unique Identifier for the device Read-only.                |
| managedDeviceCleanupSettings    | [managedDeviceCleanupSettings](../resources/manageddevicecleanupsettings.md)       | Device cleanup rule                                        |
| subscriptions                   | String                                                                             | Tenant's Subscription.                                     |
| subscriptionState               | String                                                                             | Tenant mobile device management subscription state.        |
| userExperienceAnalyticsSettings | [userExperienceAnalyticsSettings](../resources/userexperienceanalyticssettings.md) | User experience analytics device settings                  |
| windowsMalwareOverview          | [windowsMalwareOverview](../resources/windowsmalwareoverview.md)                   | Malware overview for windows devices.                      |

## Response

If successful, this method returns a `200 OK` response code and a deviceManagement object in the response body.

## Examples

### Request

<!-- {
  "blockType": "request",
  "name": "update_devicemanagement"
}
-->

```http
PATCH https://graph.microsoft.com/beta/deviceManagement

Content-Type: application/json
Content-Length: 3220

{
  "@odata.type": "#microsoft.graph.deviceManagement",
  "accountMoveCompletionDateTime": "DateTimeOffset",
  "adminConsent": {
    "@odata.type": "#microsoft.graph.adminConsent",
    "shareAPNSData": "String",
    "shareUserExperienceAnalyticsData": "String"
  },
  "deviceProtectionOverview": {
    "@odata.type": "#microsoft.graph.deviceProtectionOverview",
    "cleanDeviceCount": "Int32",
    "criticalFailuresDeviceCount": "Int32",
    "inactiveThreatAgentDeviceCount": "Int32",
    "pendingFullScanDeviceCount": "Int32",
    "pendingManualStepsDeviceCount": "Int32",
    "pendingOfflineScanDeviceCount": "Int32",
    "pendingQuickScanDeviceCount": "Int32",
    "pendingRestartDeviceCount": "Int32",
    "pendingSignatureUpdateDeviceCount": "Int32",
    "totalReportedDeviceCount": "Int32",
    "unknownStateThreatAgentDeviceCount": "Int32"
  },
  "managedDeviceCleanupSettings": {
    "@odata.type": "#microsoft.graph.managedDeviceCleanupSettings",
    "deviceInactivityBeforeRetirementInDays": "String"
  },
  "subscriptionState": "String",
  "subscriptions": "String",
  "userExperienceAnalyticsSettings": {
    "@odata.type": "#microsoft.graph.userExperienceAnalyticsSettings",
    "configurationManagerDataConnectorConfigured": "Boolean"
  },
  "windowsMalwareOverview": {
    "@odata.type": "#microsoft.graph.windowsMalwareOverview",
    "malwareCategorySummary": [
      {
        "@odata.type": "#microsoft.graph.windowsMalwareCategoryCount",
        "activeMalwareDetectionCount": "Int32",
        "category": "String",
        "deviceCount": "Int32",
        "distinctActiveMalwareCount": "Int32",
        "lastUpdateDateTime": "DateTimeOffset"
      }
    ],
    "malwareDetectedDeviceCount": "Int32",
    "malwareExecutionStateSummary": [
      {
        "@odata.type": "#microsoft.graph.windowsMalwareExecutionStateCount",
        "deviceCount": "Int32",
        "executionState": "String",
        "lastUpdateDateTime": "DateTimeOffset"
      }
    ],
    "malwareNameSummary": [
      {
        "@odata.type": "#microsoft.graph.windowsMalwareNameCount",
        "deviceCount": "Int32",
        "lastUpdateDateTime": "DateTimeOffset",
        "malwareIdentifier": "String",
        "name": "String"
      }
    ],
    "malwareSeveritySummary": [
      {
        "@odata.type": "#microsoft.graph.windowsMalwareSeverityCount",
        "distinctMalwareCount": "Int32",
        "lastUpdateDateTime": "DateTimeOffset",
        "malwareDetectionCount": "Int32",
        "severity": "String"
      }
    ],
    "malwareStateSummary": [
      {
        "@odata.type": "#microsoft.graph.windowsMalwareStateCount",
        "deviceCount": "Int32",
        "distinctMalwareCount": "Int32",
        "lastUpdateDateTime": "DateTimeOffset",
        "malwareDetectionCount": "Int32",
        "state": "String"
      }
    ],
    "osVersionsSummary": [
      {
        "@odata.type": "#microsoft.graph.osVersionCount",
        "deviceCount": "Int32",
        "lastUpdateDateTime": "DateTimeOffset",
        "osVersion": "String"
      }
    ],
    "totalDistinctMalwareCount": "Int32",
    "totalMalwareCount": "Int32"
  }
}

```

### Response

**Note:** The response object shown here might be shortened for readability.

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.management.services.api.deviceManagement"
}
-->

```http
HTTP 1.1 200 OK

Content-Type: application/json
{
  "value": {
  "@odata.type": "#microsoft.graph.deviceManagement",
  "accountMoveCompletionDateTime": "DateTimeOffset",
  "adminConsent": {
    "@odata.type": "#microsoft.graph.adminConsent",
    "shareAPNSData": "String",
    "shareUserExperienceAnalyticsData": "String"
  },
  "deviceProtectionOverview": {
    "@odata.type": "#microsoft.graph.deviceProtectionOverview",
    "cleanDeviceCount": "Int32",
    "criticalFailuresDeviceCount": "Int32",
    "inactiveThreatAgentDeviceCount": "Int32",
    "pendingFullScanDeviceCount": "Int32",
    "pendingManualStepsDeviceCount": "Int32",
    "pendingOfflineScanDeviceCount": "Int32",
    "pendingQuickScanDeviceCount": "Int32",
    "pendingRestartDeviceCount": "Int32",
    "pendingSignatureUpdateDeviceCount": "Int32",
    "totalReportedDeviceCount": "Int32",
    "unknownStateThreatAgentDeviceCount": "Int32"
  },
  "id": "String(identifier)",
  "managedDeviceCleanupSettings": {
    "@odata.type": "#microsoft.graph.managedDeviceCleanupSettings",
    "deviceInactivityBeforeRetirementInDays": "String"
  },
  "subscriptionState": "String",
  "subscriptions": "String",
  "userExperienceAnalyticsSettings": {
    "@odata.type": "#microsoft.graph.userExperienceAnalyticsSettings",
    "configurationManagerDataConnectorConfigured": "Boolean"
  },
  "windowsMalwareOverview": {
    "@odata.type": "#microsoft.graph.windowsMalwareOverview",
    "malwareCategorySummary": [
      {
        "@odata.type": "#microsoft.graph.windowsMalwareCategoryCount",
        "activeMalwareDetectionCount": "Int32",
        "category": "String",
        "deviceCount": "Int32",
        "distinctActiveMalwareCount": "Int32",
        "lastUpdateDateTime": "DateTimeOffset"
      }
    ],
    "malwareDetectedDeviceCount": "Int32",
    "malwareExecutionStateSummary": [
      {
        "@odata.type": "#microsoft.graph.windowsMalwareExecutionStateCount",
        "deviceCount": "Int32",
        "executionState": "String",
        "lastUpdateDateTime": "DateTimeOffset"
      }
    ],
    "malwareNameSummary": [
      {
        "@odata.type": "#microsoft.graph.windowsMalwareNameCount",
        "deviceCount": "Int32",
        "lastUpdateDateTime": "DateTimeOffset",
        "malwareIdentifier": "String",
        "name": "String"
      }
    ],
    "malwareSeveritySummary": [
      {
        "@odata.type": "#microsoft.graph.windowsMalwareSeverityCount",
        "distinctMalwareCount": "Int32",
        "lastUpdateDateTime": "DateTimeOffset",
        "malwareDetectionCount": "Int32",
        "severity": "String"
      }
    ],
    "malwareStateSummary": [
      {
        "@odata.type": "#microsoft.graph.windowsMalwareStateCount",
        "deviceCount": "Int32",
        "distinctMalwareCount": "Int32",
        "lastUpdateDateTime": "DateTimeOffset",
        "malwareDetectionCount": "Int32",
        "state": "String"
      }
    ],
    "osVersionsSummary": [
      {
        "@odata.type": "#microsoft.graph.osVersionCount",
        "deviceCount": "Int32",
        "lastUpdateDateTime": "DateTimeOffset",
        "osVersion": "String"
      }
    ],
    "totalDistinctMalwareCount": "Int32",
    "totalMalwareCount": "Int32"
  }
}
}

```
