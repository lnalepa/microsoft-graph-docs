---
title: "Assign appliesTo"
description: "Assign an appManagementPolicy to an application or service principal object."
ms.localizationpriority: medium
author: "madansr7"
ms.prod: "identity-and-sign-in"
doc_type: "apiPageType"
---

# Assign appliesTo

Namespace: microsoft.graph

Assign an [appManagementPolicy](../resources/appManagementPolicy.md) policy object to an application or service principal object. The application or service principal adopts this policy over the tenant-wide [tenantAppManagementPolicy](../resources/tenantappmanagementpolicy.md) setting. Only one policy object can be assigned to an application or service principal.

## Permissions

Choose the permission or permissions marked as least privileged for this API. Use a higher privileged permission or permissions [only if your app requires it](/graph/permissions-overview#best-practices-for-using-microsoft-graph-permissions). For details about delegated and application permissions, see [Permission types](/graph/permissions-overview#permission-types). To learn more about these permissions, see the [permissions reference](/graph/permissions-reference).

<!-- { "blockType": "permissions", "name": "appmanagementpolicy_post_appliesto" } -->
[!INCLUDE [permissions-table](../includes/permissions/appmanagementpolicy-post-appliesto-permissions.md)]

## HTTP request

<!-- { "blockType": "ignored" } -->

```http
POST /applications/{id}/appManagementPolicies/$ref
```

## Request headers

| Name          | Description                 |
| :------------ | :-------------------------- |
| Authorization | Bearer {token}. Required.   |
| Content-Type  | application/json. Required. |

## Request body

In the request body, provide a reference to a single policy object from the [appManagementPolicies](../resources/appmanagementpolicy.md) collection.

## Response

If successful, this method returns `204 No Content` response code. It does not return anything in the response body.

## Examples

### Example 1: Assign an appManagementPolicy to an application object

#### Request

The following is an example of the request to assign an appManagementPolicy to an application.


<!-- {
  "blockType": "request",
  "name": "assign_appliesTo"
}-->

```http
POST https://graph.microsoft.com/v1.0/applications/{id}/appManagementPolicies/$ref
Content-type: application/json

{
 "@odata.id":"https://graph.microsoft.com/v1.0/policies/appManagementPolicies/{id}"
}
```

#### Response

The following is an example of the response.

<!-- {
  "blockType": "response",
  "truncated": true
} -->

```http
HTTP/1.1 204 No Content
```

### Example 2: Assign an appManagementPolicy to a service principal object

#### Request

The following is an example of the request to assign an appManagementPolicy to a service principal.

<!-- {
  "blockType": "request",
  "name": "assign_appliesTo"
}-->

``` http
POST https://graph.microsoft.com/v1.0/servicePrincipals/{id}/appManagementPolicies/$ref

{
 "@odata.id":"https://graph.microsoft.com/v1.0/policies/appManagementPolicies/{id}"
}
```

#### Response

The following is an example of the response.

<!-- {
  "blockType": "response",
  "truncated": true
} -->

```http
HTTP/1.1 204 No Content
```

<!-- uuid: 16cd6b66-4b1a-43a1-adaf-3a886856ed98
2019-02-04 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "list resources for appManagementPolicies",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
