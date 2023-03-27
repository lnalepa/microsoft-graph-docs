---
title: "getOemWarranty function"
description: "Not yet documented"
author: "jaiprakashmb"
localization_priority: Normal
ms.prod: "intune"
doc_type: apiPageType
---

# getOemWarranty function

Namespace: microsoft.graph

> **Important:** Microsoft Graph APIs under the /beta version are subject to change; production use is not supported.

> **Note:** The Microsoft Graph API for Intune requires an [active Intune license](https://go.microsoft.com/fwlink/?linkid=839381) for the tenant.

Not yet documented

## Permissions
Choose the permission or permissions marked as least privileged for this API. Use a higher privileged permission or permissions [only if your app requires it](/graph/permissions-overview#best-practices-for-using-microsoft-graph-permissions). For details about delegated and application permissions, see [Permission types](/graph/permissions-overview#permission-types). To learn more about these permissions, see the [permissions reference](/graph/permissions-reference).

<!-- { "blockType": "permissions", "name": "intune_devices_manageddevice_getoemwarranty" } -->
[!INCLUDE [permissions-table](../includes/permissions/intune-devices-manageddevice-getoemwarranty-permissions.md)]

## HTTP Request
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/managedDevices/{managedDeviceId}/getOemWarranty
GET /deviceManagement/comanagedDevices/{managedDeviceId}/getOemWarranty
GET /deviceManagement/deviceHealthScripts/{deviceHealthScriptId}/deviceRunStates/{deviceHealthScriptDeviceStateId}/managedDevice/getOemWarranty
GET /deviceManagement/deviceManagementScripts/{deviceManagementScriptId}/deviceRunStates/{deviceManagementScriptDeviceStateId}/managedDevice/getOemWarranty
GET /deviceManagement/deviceComplianceScripts/{deviceComplianceScriptId}/deviceRunStates/{deviceComplianceScriptDeviceStateId}/managedDevice/getOemWarranty
GET /deviceManagement/deviceManagementScripts/{deviceManagementScriptId}/deviceRunStates/{deviceManagementScriptDeviceStateId}/managedDevice/users/{userId}/managedDevices/{managedDeviceId}/getOemWarranty
GET /deviceManagement/deviceManagementScripts/{deviceManagementScriptId}/deviceRunStates/{deviceManagementScriptDeviceStateId}/managedDevice/detectedApps/{detectedAppId}/managedDevices/{managedDeviceId}/getOemWarranty
```

## Request headers
|Header|Value|
|:---|:---|
|Authorization|Bearer &lt;token&gt; Required.|
|Accept|application/json|

## Request body
Do not supply a request body for this method.

## Response
If successful, this function returns a `200 OK` response code and a [oemWarranty](../resources/intune-devices-oemwarranty.md) in the response body.

## Example

### Request
Here is an example of the request.
``` http
GET https://graph.microsoft.com/beta/deviceManagement/managedDevices/{managedDeviceId}/getOemWarranty
```

### Response
Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 843

{
  "value": {
    "@odata.type": "microsoft.graph.oemWarranty",
    "baseWarranties": [
      {
        "@odata.type": "microsoft.graph.warrantyOffer",
        "type": "manufacturer",
        "description": "Description value",
        "startDateTime": "2016-12-31T23:58:46.7156189-08:00",
        "endDateTime": "2017-01-01T00:03:30.9241974-08:00"
      }
    ],
    "additionalWarranties": [
      {
        "@odata.type": "microsoft.graph.warrantyOffer",
        "type": "manufacturer",
        "description": "Description value",
        "startDateTime": "2016-12-31T23:58:46.7156189-08:00",
        "endDateTime": "2017-01-01T00:03:30.9241974-08:00"
      }
    ],
    "deviceWarrantyUrl": "https://example.com/deviceWarrantyUrl/",
    "deviceConfigurationUrl": "https://example.com/deviceConfigurationUrl/"
  }
}
```
