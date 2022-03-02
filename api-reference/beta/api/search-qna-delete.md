---
title: "Delete qna"
description: "Delete a qna object."
author: "jakeost-msft"
ms.localizationpriority: medium
ms.prod: "search"
doc_type: apiPageType
---

# Delete qna
Namespace: microsoft.graph.search

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Delete a [qna](../resources/search-qna.md) object.

## Permissions
One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).

|Permission type|Permissions (from least to most privileged)|
|:---|:---|
|Delegated (work or school account)| SearchConfiguration.Read.All, SearchConfiguration.ReadWrite.All |
|Delegated (personal Microsoft account)| Not supported. |
|Application| SearchConfiguration.Read.All, SearchConfiguration.ReadWrite.All |

## HTTP request

<!-- {
  "blockType": "ignored"
}
-->
``` http
DELETE /search/qnas/{qnaId}
```

## Request headers
|Name|Description|
|:---|:---|
|Authorization|Bearer {token}. Required.|

## Request body
Do not supply a request body for this method.

## Response

If successful, this method returns a `204 No Content` response code.

## Examples

### Request
<!-- {
  "blockType": "request",
  "name": "delete_qna"
}
-->
``` http
DELETE https://graph.microsoft.com/beta/search/qnas/{qnaId}
```


### Response
<!-- {
  "blockType": "response",
  "truncated": true
}
-->
``` http
HTTP/1.1 204 No Content
```
