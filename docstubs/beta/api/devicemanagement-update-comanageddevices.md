---
title: "Update comanagedDevices"
description: ""
localization_priority: Normal
author: "$(metadata.owner)"
ms.prod: "microsoft-identity-platform"
doc_type: "apiPageType"
---

# Update comanagedDevices

Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Update the properties of a managedDevice object.

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

In the request body, supply JSON representation of the [managedDevice](../resources/intune-manageddevice.md) object.

<!-- Actions and Functions -->

<!-- CRUD Methods -->

The following table shows the properties that are required when you create a managedDevice object.

| Property                                  | Type                                                                                                   | Description                                                                                                                                                                                              |
| :---------------------------------------- | :----------------------------------------------------------------------------------------------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| aadRegistered                             | Boolean                                                                                                | Whether the device is Azure Active Directory registered. This property is read-only.                                                                                                                     |
| activationLockBypassCode                  | String                                                                                                 | Code that allows the Activation Lock on a device to be bypassed. This property is read-only.                                                                                                             |
| androidSecurityPatchLevel                 | String                                                                                                 | Android security patch level. This property is read-only.                                                                                                                                                |
| autopilotEnrolled                         | Boolean                                                                                                | Reports if the managed device is enrolled via auto-pilot. This property is read-only.                                                                                                                    |
| azureActiveDirectoryDeviceId              | String                                                                                                 | The unique identifier for the Azure Active Directory device. Read only. This property is read-only.                                                                                                      |
| azureADDeviceId                           | String                                                                                                 | The unique identifier for the Azure Active Directory device. Read only. This property is read-only.                                                                                                      |
| azureADRegistered                         | Boolean                                                                                                | Whether the device is Azure Active Directory registered. This property is read-only.                                                                                                                     |
| chassisType                               | String                                                                                                 | Chassis type of the device. This property is read-only.                                                                                                                                                  |
| complianceGracePeriodExpirationDateTime   | DateTimeOffset                                                                                         | The DateTime when device compliance grace period expires. This property is read-only.                                                                                                                    |
| complianceState                           | String                                                                                                 | Compliance state of the device. This property is read-only.                                                                                                                                              |
| configurationManagerClientEnabledFeatures | [configurationManagerClientEnabledFeatures](../resources/configurationmanagerclientenabledfeatures.md) | ConfigrMgr client enabled features. This property is read-only.                                                                                                                                          |
| configurationManagerClientHealthState     | [configurationManagerClientHealthState](../resources/configurationmanagerclienthealthstate.md)         | Configuration manager client health state, valid only for devices managed by MDM/ConfigMgr Agent                                                                                                         |
| configurationManagerClientInformation     | [configurationManagerClientInformation](../resources/configurationmanagerclientinformation.md)         | Configuration manager client information, valid only for devices managed, duel-managed or tri-managed by ConfigMgr Agent                                                                                 |
| deviceActionResults                       | [deviceActionResult](../resources/deviceactionresult.md) collection                                    | List of ComplexType deviceActionResult objects. This property is read-only.                                                                                                                              |
| deviceCategoryDisplayName                 | String                                                                                                 | Device category display name. This property is read-only.                                                                                                                                                |
| deviceEnrollmentType                      | String                                                                                                 | Enrollment type of the device. This property is read-only.                                                                                                                                               |
| deviceHealthAttestationState              | [deviceHealthAttestationState](../resources/devicehealthattestationstate.md)                           | The device health attestation state. This property is read-only.                                                                                                                                         |
| deviceName                                | String                                                                                                 | Name of the device. This property is read-only.                                                                                                                                                          |
| deviceRegistrationState                   | String                                                                                                 | Device registration state. This property is read-only.                                                                                                                                                   |
| deviceType                                | String                                                                                                 | Platform of the device. This property is read-only.                                                                                                                                                      |
| easActivated                              | Boolean                                                                                                | Whether the device is Exchange ActiveSync activated. This property is read-only.                                                                                                                         |
| easActivationDateTime                     | DateTimeOffset                                                                                         | Exchange ActivationSync activation time of the device. This property is read-only.                                                                                                                       |
| easDeviceId                               | String                                                                                                 | Exchange ActiveSync Id of the device. This property is read-only.                                                                                                                                        |
| emailAddress                              | String                                                                                                 | Email(s) for the user associated with the device. This property is read-only.                                                                                                                            |
| enrolledDateTime                          | DateTimeOffset                                                                                         | Enrollment time of the device. This property is read-only.                                                                                                                                               |
| ethernetMacAddress                        | String                                                                                                 | Ethernet MAC. This property is read-only.                                                                                                                                                                |
| exchangeAccessState                       | String                                                                                                 | The Access State of the device in Exchange. This property is read-only.                                                                                                                                  |
| exchangeAccessStateReason                 | String                                                                                                 | The reason for the device's access state in Exchange. This property is read-only.                                                                                                                        |
| exchangeLastSuccessfulSyncDateTime        | DateTimeOffset                                                                                         | Last time the device contacted Exchange. This property is read-only.                                                                                                                                     |
| freeStorageSpaceInBytes                   | Int64                                                                                                  | Free Storage in Bytes. This property is read-only.                                                                                                                                                       |
| hardwareInformation                       | [hardwareInformation](../resources/hardwareinformation.md)                                             | The hardward details for the device.  Includes information such as storage space, manufacturer, serial number, etc. This property is read-only.                                                          |
| iccid                                     | String                                                                                                 | Integrated Circuit Card Identifier, it is A SIM card's unique identification number. This property is read-only.                                                                                         |
| id                                        | String                                                                                                 | Unique Identifier for the device. This property is read-only. Read-only.                                                                                                                                 |
| imei                                      | String                                                                                                 | IMEI. This property is read-only.                                                                                                                                                                        |
| isEncrypted                               | Boolean                                                                                                | Device encryption status. This property is read-only.                                                                                                                                                    |
| isSupervised                              | Boolean                                                                                                | Device supervised status. This property is read-only.                                                                                                                                                    |
| jailBroken                                | String                                                                                                 | whether the device is jail broken or rooted. This property is read-only.                                                                                                                                 |
| joinType                                  | String                                                                                                 | Device join type                                                                                                                                                                                         |
| lastSyncDateTime                          | DateTimeOffset                                                                                         | The date and time that the device last completed a successful sync with Intune. This property is read-only.                                                                                              |
| lostModeState                             | String                                                                                                 | Indicates if Lost mode is enabled or disabled. This property is read-only.                                                                                                                               |
| managedDeviceName                         | String                                                                                                 | Automatically generated name to identify a device. Can be overwritten to a user friendly name.                                                                                                           |
| managedDeviceOwnerType                    | String                                                                                                 | Ownership of the device. Can be 'company' or 'personal'                                                                                                                                                  |
| managementAgent                           | String                                                                                                 | Management channel of the device. Intune, EAS, etc. This property is read-only.                                                                                                                          |
| managementCertificateExpirationDate       | DateTimeOffset                                                                                         | Reports device management certificate expiration date. This property is read-only.                                                                                                                       |
| managementFeatures                        | String                                                                                                 | Device management features                                                                                                                                                                               |
| managementState                           | String                                                                                                 | Management state of the device. This property is read-only.                                                                                                                                              |
| manufacturer                              | String                                                                                                 | Manufacturer of the device. This property is read-only.                                                                                                                                                  |
| meid                                      | String                                                                                                 | MEID. This property is read-only.                                                                                                                                                                        |
| model                                     | String                                                                                                 | Model of the device. This property is read-only.                                                                                                                                                         |
| notes                                     | String                                                                                                 | Notes on the device created by IT Admin                                                                                                                                                                  |
| operatingSystem                           | String                                                                                                 | Operating system of the device. Windows, iOS, etc. This property is read-only.                                                                                                                           |
| osVersion                                 | String                                                                                                 | Operating system version of the device. This property is read-only.                                                                                                                                      |
| ownerType                                 | String                                                                                                 | Ownership of the device. Can be 'company' or 'personal'                                                                                                                                                  |
| partnerReportedThreatState                | String                                                                                                 | Indicates the threat state of a device when a Mobile Threat Defense partner is in use by the account and device. Read Only. This property is read-only.                                                  |
| phoneNumber                               | String                                                                                                 | Phone number of the device. This property is read-only.                                                                                                                                                  |
| physicalMemoryInBytes                     | Int64                                                                                                  | Total Memory in Bytes. This property is read-only.                                                                                                                                                       |
| preferMdmOverGroupPolicyAppliedDateTime   | DateTimeOffset                                                                                         | Reports the DateTime the preferMdmOverGroupPolicy setting was set.  When set, the Intune MDM settings will override Group Policy settings if there is a conflict. Read Only. This property is read-only. |
| processorArchitecture                     | String                                                                                                 | Processor architecture. This property is read-only.                                                                                                                                                      |
| remoteAssistanceSessionErrorDetails       | String                                                                                                 | An error string that identifies issues when creating Remote Assistance session objects. This property is read-only.                                                                                      |
| remoteAssistanceSessionUrl                | String                                                                                                 | Url that allows a Remote Assistance session to be established with the device. This property is read-only.                                                                                               |
| requireUserEnrollmentApproval             | Boolean                                                                                                | Reports if the managed iOS device is user approval enrollment. This property is read-only.                                                                                                               |
| retireAfterDateTime                       | DateTimeOffset                                                                                         | Indicates the time after when a device will be auto retired because of scheduled action. This property is read-only.                                                                                     |
| roleScopeTagIds                           | String collection                                                                                      | List of Scope Tag IDs for this Device instance.                                                                                                                                                          |
| serialNumber                              | String                                                                                                 | SerialNumber. This property is read-only.                                                                                                                                                                |
| skuFamily                                 | String                                                                                                 | Device sku family                                                                                                                                                                                        |
| skuNumber                                 | Int32                                                                                                  | Device sku number, see also: https://docs.microsoft.com/en-us/windows/win32/api/sysinfoapi/nf-sysinfoapi-getproductinfo. Valid values 0 to 2147483647. This property is read-only.                       |
| specificationVersion                      | String                                                                                                 | Specification version. This property is read-only.                                                                                                                                                       |
| subscriberCarrier                         | String                                                                                                 | Subscriber Carrier. This property is read-only.                                                                                                                                                          |
| totalStorageSpaceInBytes                  | Int64                                                                                                  | Total Storage in Bytes. This property is read-only.                                                                                                                                                      |
| udid                                      | String                                                                                                 | Unique Device Identifier for iOS and macOS devices. This property is read-only.                                                                                                                          |
| userDisplayName                           | String                                                                                                 | User display name. This property is read-only.                                                                                                                                                           |
| userId                                    | String                                                                                                 | Unique Identifier for the user associated with the device. This property is read-only.                                                                                                                   |
| userPrincipalName                         | String                                                                                                 | Device user principal name. This property is read-only.                                                                                                                                                  |
| usersLoggedOn                             | [loggedOnUser](../resources/loggedonuser.md) collection                                                | Indicates the last logged on users of a device. This property is read-only.                                                                                                                              |
| wiFiMacAddress                            | String                                                                                                 | Wi-Fi MAC. This property is read-only.                                                                                                                                                                   |
| windowsActiveMalwareCount                 | Int32                                                                                                  | Count of active malware for this windows device. This property is read-only.                                                                                                                             |
| windowsRemediatedMalwareCount             | Int32                                                                                                  | Count of remediated malware for this windows device. This property is read-only.                                                                                                                         |

## Response

If successful, this method returns a `200 OK` response code and a managedDevice object in the response body.

## Examples

### Request

<!-- {
  "blockType": "request",
  "name": "update_comanageddevices"
}
-->

```http
PATCH https://graph.microsoft.com/beta

Content-Type: application/json
Content-Length: 6848

[
  {
    "@odata.type": "#microsoft.graph.managedDevice",
    "aadRegistered": "Boolean",
    "activationLockBypassCode": "String",
    "androidSecurityPatchLevel": "String",
    "autopilotEnrolled": "Boolean",
    "azureADDeviceId": "String",
    "azureADRegistered": "Boolean",
    "azureActiveDirectoryDeviceId": "String",
    "chassisType": "String",
    "complianceGracePeriodExpirationDateTime": "DateTimeOffset",
    "complianceState": "String",
    "configurationManagerClientEnabledFeatures": {
      "@odata.type": "#microsoft.graph.configurationManagerClientEnabledFeatures",
      "compliancePolicy": "Boolean",
      "deviceConfiguration": "Boolean",
      "endpointProtection": "Boolean",
      "inventory": "Boolean",
      "modernApps": "Boolean",
      "officeApps": "Boolean",
      "resourceAccess": "Boolean",
      "windowsUpdateForBusiness": "Boolean"
    },
    "configurationManagerClientHealthState": {
      "@odata.type": "#microsoft.graph.configurationManagerClientHealthState",
      "errorCode": "Int32",
      "lastSyncDateTime": "DateTimeOffset",
      "state": "String"
    },
    "configurationManagerClientInformation": {
      "@odata.type": "#microsoft.graph.configurationManagerClientInformation",
      "clientIdentifier": "String",
      "isBlocked": "Boolean"
    },
    "deviceActionResults": [
      {
        "@odata.type": "#microsoft.graph.deviceActionResult",
        "actionName": "String",
        "actionState": "String",
        "lastUpdatedDateTime": "DateTimeOffset",
        "startDateTime": "DateTimeOffset"
      }
    ],
    "deviceCategoryDisplayName": "String",
    "deviceEnrollmentType": "String",
    "deviceHealthAttestationState": {
      "@odata.type": "#microsoft.graph.deviceHealthAttestationState",
      "attestationIdentityKey": "String",
      "bitLockerStatus": "String",
      "bootAppSecurityVersion": "String",
      "bootDebugging": "String",
      "bootManagerSecurityVersion": "String",
      "bootManagerVersion": "String",
      "bootRevisionListInfo": "String",
      "codeIntegrity": "String",
      "codeIntegrityCheckVersion": "String",
      "codeIntegrityPolicy": "String",
      "contentNamespaceUrl": "String",
      "contentVersion": "String",
      "dataExcutionPolicy": "String",
      "deviceHealthAttestationStatus": "String",
      "earlyLaunchAntiMalwareDriverProtection": "String",
      "healthAttestationSupportedStatus": "String",
      "healthStatusMismatchInfo": "String",
      "issuedDateTime": "DateTimeOffset",
      "lastUpdateDateTime": "String",
      "operatingSystemKernelDebugging": "String",
      "operatingSystemRevListInfo": "String",
      "pcr0": "String",
      "pcrHashAlgorithm": "String",
      "resetCount": "Int64",
      "restartCount": "Int64",
      "safeMode": "String",
      "secureBoot": "String",
      "secureBootConfigurationPolicyFingerPrint": "String",
      "testSigning": "String",
      "tpmVersion": "String",
      "virtualSecureMode": "String",
      "windowsPE": "String"
    },
    "deviceName": "String",
    "deviceRegistrationState": "String",
    "deviceType": "String",
    "easActivated": "Boolean",
    "easActivationDateTime": "DateTimeOffset",
    "easDeviceId": "String",
    "emailAddress": "String",
    "enrolledDateTime": "DateTimeOffset",
    "ethernetMacAddress": "String",
    "exchangeAccessState": "String",
    "exchangeAccessStateReason": "String",
    "exchangeLastSuccessfulSyncDateTime": "DateTimeOffset",
    "freeStorageSpaceInBytes": "Int64",
    "hardwareInformation": {
      "@odata.type": "#microsoft.graph.hardwareInformation",
      "batteryChargeCycles": "Int32",
      "batteryHealthPercentage": "Int32",
      "batterySerialNumber": "String",
      "cellularTechnology": "String",
      "deviceFullQualifiedDomainName": "String",
      "deviceGuardLocalSystemAuthorityCredentialGuardState": "String",
      "deviceGuardVirtualizationBasedSecurityHardwareRequirementState": "String",
      "deviceGuardVirtualizationBasedSecurityState": "String",
      "freeStorageSpace": "Int64",
      "imei": "String",
      "isEncrypted": "Boolean",
      "isSharedDevice": "Boolean",
      "isSupervised": "Boolean",
      "manufacturer": "String",
      "meid": "String",
      "model": "String",
      "operatingSystemEdition": "String",
      "operatingSystemLanguage": "String",
      "operatingSystemProductType": "Int32",
      "osBuildNumber": "String",
      "phoneNumber": "String",
      "serialNumber": "String",
      "sharedDeviceCachedUsers": [
        {
          "@odata.type": "#microsoft.graph.sharedAppleDeviceUser",
          "dataQuota": "Int64",
          "dataToSync": "Boolean",
          "dataUsed": "Int64",
          "userPrincipalName": "String"
        }
      ],
      "subscriberCarrier": "String",
      "totalStorageSpace": "Int64",
      "tpmSpecificationVersion": "String",
      "wifiMac": "String"
    },
    "iccid": "String",
    "id": "String(identifier)",
    "imei": "String",
    "isEncrypted": "Boolean",
    "isSupervised": "Boolean",
    "jailBroken": "String",
    "joinType": "String",
    "lastSyncDateTime": "DateTimeOffset",
    "lostModeState": "String",
    "managedDeviceName": "String",
    "managedDeviceOwnerType": "String",
    "managementAgent": "String",
    "managementCertificateExpirationDate": "DateTimeOffset",
    "managementFeatures": "String",
    "managementState": "String",
    "manufacturer": "String",
    "meid": "String",
    "model": "String",
    "notes": "String",
    "operatingSystem": "String",
    "osVersion": "String",
    "ownerType": "String",
    "partnerReportedThreatState": "String",
    "phoneNumber": "String",
    "physicalMemoryInBytes": "Int64",
    "preferMdmOverGroupPolicyAppliedDateTime": "DateTimeOffset",
    "processorArchitecture": "String",
    "remoteAssistanceSessionErrorDetails": "String",
    "remoteAssistanceSessionUrl": "String",
    "requireUserEnrollmentApproval": "Boolean",
    "retireAfterDateTime": "DateTimeOffset",
    "roleScopeTagIds": [
      "String"
    ],
    "serialNumber": "String",
    "skuFamily": "String",
    "skuNumber": "Int32",
    "specificationVersion": "String",
    "subscriberCarrier": "String",
    "totalStorageSpaceInBytes": "Int64",
    "udid": "String",
    "userDisplayName": "String",
    "userId": "String",
    "userPrincipalName": "String",
    "usersLoggedOn": [
      {
        "@odata.type": "#microsoft.graph.loggedOnUser",
        "lastLogOnDateTime": "DateTimeOffset",
        "userId": "String"
      }
    ],
    "wiFiMacAddress": "String",
    "windowsActiveMalwareCount": "Int32",
    "windowsRemediatedMalwareCount": "Int32"
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
    "@odata.type": "#microsoft.graph.managedDevice",
    "aadRegistered": "Boolean",
    "activationLockBypassCode": "String",
    "androidSecurityPatchLevel": "String",
    "autopilotEnrolled": "Boolean",
    "azureADDeviceId": "String",
    "azureADRegistered": "Boolean",
    "azureActiveDirectoryDeviceId": "String",
    "chassisType": "String",
    "complianceGracePeriodExpirationDateTime": "DateTimeOffset",
    "complianceState": "String",
    "configurationManagerClientEnabledFeatures": {
      "@odata.type": "#microsoft.graph.configurationManagerClientEnabledFeatures",
      "compliancePolicy": "Boolean",
      "deviceConfiguration": "Boolean",
      "endpointProtection": "Boolean",
      "inventory": "Boolean",
      "modernApps": "Boolean",
      "officeApps": "Boolean",
      "resourceAccess": "Boolean",
      "windowsUpdateForBusiness": "Boolean"
    },
    "configurationManagerClientHealthState": {
      "@odata.type": "#microsoft.graph.configurationManagerClientHealthState",
      "errorCode": "Int32",
      "lastSyncDateTime": "DateTimeOffset",
      "state": "String"
    },
    "configurationManagerClientInformation": {
      "@odata.type": "#microsoft.graph.configurationManagerClientInformation",
      "clientIdentifier": "String",
      "isBlocked": "Boolean"
    },
    "deviceActionResults": [
      {
        "@odata.type": "#microsoft.graph.deviceActionResult",
        "actionName": "String",
        "actionState": "String",
        "lastUpdatedDateTime": "DateTimeOffset",
        "startDateTime": "DateTimeOffset"
      }
    ],
    "deviceCategoryDisplayName": "String",
    "deviceEnrollmentType": "String",
    "deviceHealthAttestationState": {
      "@odata.type": "#microsoft.graph.deviceHealthAttestationState",
      "attestationIdentityKey": "String",
      "bitLockerStatus": "String",
      "bootAppSecurityVersion": "String",
      "bootDebugging": "String",
      "bootManagerSecurityVersion": "String",
      "bootManagerVersion": "String",
      "bootRevisionListInfo": "String",
      "codeIntegrity": "String",
      "codeIntegrityCheckVersion": "String",
      "codeIntegrityPolicy": "String",
      "contentNamespaceUrl": "String",
      "contentVersion": "String",
      "dataExcutionPolicy": "String",
      "deviceHealthAttestationStatus": "String",
      "earlyLaunchAntiMalwareDriverProtection": "String",
      "healthAttestationSupportedStatus": "String",
      "healthStatusMismatchInfo": "String",
      "issuedDateTime": "DateTimeOffset",
      "lastUpdateDateTime": "String",
      "operatingSystemKernelDebugging": "String",
      "operatingSystemRevListInfo": "String",
      "pcr0": "String",
      "pcrHashAlgorithm": "String",
      "resetCount": "Int64",
      "restartCount": "Int64",
      "safeMode": "String",
      "secureBoot": "String",
      "secureBootConfigurationPolicyFingerPrint": "String",
      "testSigning": "String",
      "tpmVersion": "String",
      "virtualSecureMode": "String",
      "windowsPE": "String"
    },
    "deviceName": "String",
    "deviceRegistrationState": "String",
    "deviceType": "String",
    "easActivated": "Boolean",
    "easActivationDateTime": "DateTimeOffset",
    "easDeviceId": "String",
    "emailAddress": "String",
    "enrolledDateTime": "DateTimeOffset",
    "ethernetMacAddress": "String",
    "exchangeAccessState": "String",
    "exchangeAccessStateReason": "String",
    "exchangeLastSuccessfulSyncDateTime": "DateTimeOffset",
    "freeStorageSpaceInBytes": "Int64",
    "hardwareInformation": {
      "@odata.type": "#microsoft.graph.hardwareInformation",
      "batteryChargeCycles": "Int32",
      "batteryHealthPercentage": "Int32",
      "batterySerialNumber": "String",
      "cellularTechnology": "String",
      "deviceFullQualifiedDomainName": "String",
      "deviceGuardLocalSystemAuthorityCredentialGuardState": "String",
      "deviceGuardVirtualizationBasedSecurityHardwareRequirementState": "String",
      "deviceGuardVirtualizationBasedSecurityState": "String",
      "freeStorageSpace": "Int64",
      "imei": "String",
      "isEncrypted": "Boolean",
      "isSharedDevice": "Boolean",
      "isSupervised": "Boolean",
      "manufacturer": "String",
      "meid": "String",
      "model": "String",
      "operatingSystemEdition": "String",
      "operatingSystemLanguage": "String",
      "operatingSystemProductType": "Int32",
      "osBuildNumber": "String",
      "phoneNumber": "String",
      "serialNumber": "String",
      "sharedDeviceCachedUsers": [
        {
          "@odata.type": "#microsoft.graph.sharedAppleDeviceUser",
          "dataQuota": "Int64",
          "dataToSync": "Boolean",
          "dataUsed": "Int64",
          "userPrincipalName": "String"
        }
      ],
      "subscriberCarrier": "String",
      "totalStorageSpace": "Int64",
      "tpmSpecificationVersion": "String",
      "wifiMac": "String"
    },
    "iccid": "String",
    "id": "String(identifier)",
    "imei": "String",
    "isEncrypted": "Boolean",
    "isSupervised": "Boolean",
    "jailBroken": "String",
    "joinType": "String",
    "lastSyncDateTime": "DateTimeOffset",
    "lostModeState": "String",
    "managedDeviceName": "String",
    "managedDeviceOwnerType": "String",
    "managementAgent": "String",
    "managementCertificateExpirationDate": "DateTimeOffset",
    "managementFeatures": "String",
    "managementState": "String",
    "manufacturer": "String",
    "meid": "String",
    "model": "String",
    "notes": "String",
    "operatingSystem": "String",
    "osVersion": "String",
    "ownerType": "String",
    "partnerReportedThreatState": "String",
    "phoneNumber": "String",
    "physicalMemoryInBytes": "Int64",
    "preferMdmOverGroupPolicyAppliedDateTime": "DateTimeOffset",
    "processorArchitecture": "String",
    "remoteAssistanceSessionErrorDetails": "String",
    "remoteAssistanceSessionUrl": "String",
    "requireUserEnrollmentApproval": "Boolean",
    "retireAfterDateTime": "DateTimeOffset",
    "roleScopeTagIds": [
      "String"
    ],
    "serialNumber": "String",
    "skuFamily": "String",
    "skuNumber": "Int32",
    "specificationVersion": "String",
    "subscriberCarrier": "String",
    "totalStorageSpaceInBytes": "Int64",
    "udid": "String",
    "userDisplayName": "String",
    "userId": "String",
    "userPrincipalName": "String",
    "usersLoggedOn": [
      {
        "@odata.type": "#microsoft.graph.loggedOnUser",
        "lastLogOnDateTime": "DateTimeOffset",
        "userId": "String"
      }
    ],
    "wiFiMacAddress": "String",
    "windowsActiveMalwareCount": "Int32",
    "windowsRemediatedMalwareCount": "Int32"
  }
]
}

```
