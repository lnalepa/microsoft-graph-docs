---
title: "governanceResource: register"
description: "Register a governanceResource object in PIM."
ms.localizationpriority: medium
doc_type: apiPageType
ms.prod: "governance"
author: "rkarim-ms"
---

# governanceResource: register

Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

[!INCLUDE [pim-v2ResourceRoles-deprecation](../../includes/pim-v2ResourceRoles-deprecation.md)]

Register a [governanceResource](../resources/governanceresource.md) object in Privileged Identity Management.

## Permissions

Choose the permission or permissions marked as least privileged for this API. Use a higher privileged permission or permissions [only if your app requires it](/graph/permissions-overview#best-practices-for-using-microsoft-graph-permissions). For details about delegated and application permissions, see [Permission types](/graph/permissions-overview#permission-types). To learn more about these permissions, see the [permissions reference](/graph/permissions-reference).

>**Note:** This API also requires that the requester have at least one active role assignment on the resource.

### Azure resources

<!-- { "blockType": "permissions", "name": "governanceresource_register" } -->
[!INCLUDE [permissions-table](../includes/permissions/governanceresource-register-permissions.md)]

### Azure AD

| Permission type | Permissions |
|:--------------- |:----------- |
| Delegated (work or school account) | PrivilegedAccess.ReadWrite.AzureAD |
| Delegated (personal Microsoft account) | Not supported. |
| Application | Not supported. |

### Groups

|Permission type | Permissions |
|:-------------- |:----------- |
| Delegated (work or school account) | PrivilegedAccess.ReadWrite.AzureADGroup |
| Delegated (personal Microsoft account) | Not supported. |
| Application | Not supported. |

## HTTP request

<!-- { "blockType": "ignored" } -->
```http
POST /privilegedAccess/azureResources/resources/register
```

## Optional query parameters

This method **only** supports the `$select` and `$expand` [OData query parameters](/graph/query-parameters) to help customize the response.

## Request headers

| Name | Description |
|:---- |:----------- |
| Authorization | Bearer {token} |
| Content-type | application/json |

## Request body

| Properties | Type	| Description |
|:---------- |:---- |:----------- |
| externalId | String | The external identifier of the resource to be registered in PIM. If registering a subscription, the identifier is the subscription identifier prepended by `/subscriptions/`. For example, `/subscriptions/c14ae696-5e0c-4e5d-88cc-bef6637737ac`. |

## Response

If successful, this method returns a `200 OK` response.

## Example

The following example shows how to call this API.
<!-- {
  "blockType": "request",
  "name": "get_governanceresource"
}-->
### Request
```http
POST https://graph.microsoft.com/beta/privilegedAccess/azureResources/resources/register
Content-type: application/json

{
  "externalId": "/subscriptions/c14ae696-5e0c-4e5d-88cc-bef6637737ac"
}
```
### Response
<!-- {
  "blockType": "response",
  "truncated": false,
  "@odata.type": "microsoft.graph.governanceResource"
} -->
```http
HTTP/1.1 200 OK
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "Register governanceResource",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": []
}
-->


