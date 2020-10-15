---
title: "Update managedDeviceOverview"
description: ""
localization_priority: Normal
author: "$(metadata.owner)"
ms.prod: "microsoft-identity-platform"
doc_type: "apiPageType"
---

# Update managedDeviceOverview

Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Update the properties of a managedDeviceOverview object.

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

In the request body, supply JSON representation of the [managedDeviceOverview](../resources/intune-manageddeviceoverview.md) object.

<!-- Actions and Functions -->

<!-- CRUD Methods -->

The following table shows the properties that are required when you create a managedDeviceOverview object.

| Property                            | Type                                                                                       | Description                                                                          |
| :---------------------------------- | :----------------------------------------------------------------------------------------- | :----------------------------------------------------------------------------------- |
| deviceExchangeAccessStateSummary    | [deviceExchangeAccessStateSummary](../resources/deviceexchangeaccessstatesummary.md)       | Distribution of Exchange Access State in Intune                                      |
| deviceOperatingSystemSummary        | [deviceOperatingSystemSummary](../resources/deviceoperatingsystemsummary.md)               | Device operating system summary.                                                     |
| dualEnrolledDeviceCount             | Int32                                                                                      | The number of devices enrolled in both MDM and EAS                                   |
| enrolledDeviceCount                 | Int32                                                                                      | Total enrolled device count. Does not include PC devices managed via Intune PC Agent |
| id                                  | String                                                                                     | Unique Identifier for the summary Read-only.                                         |
| lastModifiedDateTime                | DateTimeOffset                                                                             | Last modified date time of device overview                                           |
| managedDeviceModelsAndManufacturers | [managedDeviceModelsAndManufacturers](../resources/manageddevicemodelsandmanufacturers.md) | Models and Manufactures meatadata for managed devices in the account                 |
| mdmEnrolledCount                    | Int32                                                                                      | The number of devices enrolled in MDM                                                |

## Response

If successful, this method returns a `200 OK` response code and a managedDeviceOverview object in the response body.

## Examples

### Request

<!-- {
  "blockType": "request",
  "name": "update_manageddeviceoverview"
}
-->

```http
PATCH https://graph.microsoft.com/beta/deviceManagement/managedDeviceOverview

Content-Type: application/json
Content-Length: 1324

{
  "@odata.type": "#microsoft.graph.managedDeviceOverview",
  "deviceExchangeAccessStateSummary": {
    "@odata.type": "#microsoft.graph.deviceExchangeAccessStateSummary",
    "allowedDeviceCount": "Int32",
    "blockedDeviceCount": "Int32",
    "quarantinedDeviceCount": "Int32",
    "unavailableDeviceCount": "Int32",
    "unknownDeviceCount": "Int32"
  },
  "deviceOperatingSystemSummary": {
    "@odata.type": "#microsoft.graph.deviceOperatingSystemSummary",
    "androidCorporateWorkProfileCount": "Int32",
    "androidCount": "Int32",
    "androidDedicatedCount": "Int32",
    "androidDeviceAdminCount": "Int32",
    "androidFullyManagedCount": "Int32",
    "androidWorkProfileCount": "Int32",
    "aospUserlessCount": "Int32",
    "configMgrDeviceCount": "Int32",
    "iosCount": "Int32",
    "macOSCount": "Int32",
    "unknownCount": "Int32",
    "windowsCount": "Int32",
    "windowsMobileCount": "Int32"
  },
  "dualEnrolledDeviceCount": "Int32",
  "enrolledDeviceCount": "Int32",
  "lastModifiedDateTime": "DateTimeOffset",
  "managedDeviceModelsAndManufacturers": {
    "@odata.type": "#microsoft.graph.managedDeviceModelsAndManufacturers",
    "deviceManufacturers": [
      "String"
    ],
    "deviceModels": [
      "String"
    ]
  },
  "mdmEnrolledCount": "Int32"
}

```

### Response

**Note:** The response object shown here might be shortened for readability.

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.management.services.api.managedDeviceOverview"
}
-->

```http
HTTP 1.1 200 OK

Content-Type: application/json
{
  "value": {
  "@odata.type": "#microsoft.graph.managedDeviceOverview",
  "deviceExchangeAccessStateSummary": {
    "@odata.type": "#microsoft.graph.deviceExchangeAccessStateSummary",
    "allowedDeviceCount": "Int32",
    "blockedDeviceCount": "Int32",
    "quarantinedDeviceCount": "Int32",
    "unavailableDeviceCount": "Int32",
    "unknownDeviceCount": "Int32"
  },
  "deviceOperatingSystemSummary": {
    "@odata.type": "#microsoft.graph.deviceOperatingSystemSummary",
    "androidCorporateWorkProfileCount": "Int32",
    "androidCount": "Int32",
    "androidDedicatedCount": "Int32",
    "androidDeviceAdminCount": "Int32",
    "androidFullyManagedCount": "Int32",
    "androidWorkProfileCount": "Int32",
    "aospUserlessCount": "Int32",
    "configMgrDeviceCount": "Int32",
    "iosCount": "Int32",
    "macOSCount": "Int32",
    "unknownCount": "Int32",
    "windowsCount": "Int32",
    "windowsMobileCount": "Int32"
  },
  "dualEnrolledDeviceCount": "Int32",
  "enrolledDeviceCount": "Int32",
  "id": "String(identifier)",
  "lastModifiedDateTime": "DateTimeOffset",
  "managedDeviceModelsAndManufacturers": {
    "@odata.type": "#microsoft.graph.managedDeviceModelsAndManufacturers",
    "deviceManufacturers": [
      "String"
    ],
    "deviceModels": [
      "String"
    ]
  },
  "mdmEnrolledCount": "Int32"
}
}

```
