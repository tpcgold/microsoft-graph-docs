---
title: "documentSetVersion: restore"
description: "Restore a documentSetVersion."
author: "swapnil1993"
ms.localizationpriority: medium
ms.prod: "sites-and-lists"
doc_type: apiPageType
---

# documentSetVersion: restore
Namespace: microsoft.graph

Restore a [document set version](../resources/documentsetversion.md).

## Permissions
One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).

| Permission type                        | Permissions (from least to most privileged)                                  |
|:---------------------------------------|:-----------------------------------------------------------------------------|
| Delegated (work or school account)     | Sites.ReadWrite.All, Sites.Manage.All, Sites.FullControl.All                 |
| Delegated (personal Microsoft account) | Not supported.                                                               |
| Application                            | Sites.ReadWrite.All, Sites.Manage.All, Sites.FullControl.All, Sites.Selected |

## HTTP request

<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /sites/{siteId}/lists/{listId}/items/{itemId}/documentSetVersions/{documentSetVersionId}/restore
```

## Request headers
|Name|Description|
|:---|:---|
|Authorization|Bearer {token}. Required.|

## Request body
Do not supply a request body for this method.

## Response

If successful, this action returns a `204 No Content` response code.

## Examples

### Request

The following is an example of a request.


<!-- {
  "blockType": "request",
  "name": "documentsetversionthis.restore",
  "sampleKeys": ["root", "Documents", "2", "1"]
}
-->
``` http
POST https://graph.microsoft.com/v1.0/sites/root/lists/Documents/items/2/documentSetVersions/1/restore
```

### Response

The following is an example of the response.

<!-- {
  "blockType": "response",
  "name": "documentsetversionthis.restore",
  "truncated": true
}
-->
``` http
HTTP/1.1 204 No Content
```

