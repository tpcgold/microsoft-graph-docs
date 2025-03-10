---
title: "List softwareOathMethods"
description: "Retrieve a list of a user's softwareOathAuthenticationMethods objects and their properties."
author: "mmcla"
ms.localizationpriority: medium
ms.prod: "identity-and-sign-in"
doc_type: apiPageType
---

# List softwareOathMethods
Namespace: microsoft.graph

Retrieve a list of a user's [software OATH token authentication method](../resources/softwareoathauthenticationmethod.md) objects and their properties.

## Permissions

One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).

### Permissions acting on self

|Permission type      | Permissions (from least to most privileged)              |
|:---------------------------------------|:-------------------------|
| Delegated (work or school account)     | UserAuthenticationMethod.Read, UserAuthenticationMethod.ReadWrite |
| Delegated (personal Microsoft account) | Not supported. |
| Application                            | Not supported. |

### Permissions acting on other users

|Permission type      | Permissions (from least to most privileged)              |
|:---------------------------------------|:-------------------------|
| Delegated (work or school account)     | UserAuthenticationMethod.Read.All, UserAuthenticationMethod.ReadWrite.All |
| Delegated (personal Microsoft account) | Not supported. |
| Application                            | UserAuthenticationMethod.Read.All, UserAuthenticationMethod.ReadWrite.All |

For delegated scenarios where an admin is acting on another user, the admin needs [one of the following directory roles](/azure/active-directory/users-groups-roles/directory-assign-admin-roles#available-roles):
* Global Reader
* Authentication administrator
* Privileged authentication administrator
* Global administrator

## HTTP request

<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /me/authentication/softwareOathMethods
GET /users/{id | userPrincipalName}/authentication/softwareOathMethods
```

## Request headers
|Name|Description|
|:---|:---|
|Authorization|Bearer {token}. Required.|

## Request body
Do not supply a request body for this method.

## Response

If successful, this method returns a `200 OK` response code and a collection of [softwareOathAuthenticationMethod](../resources/softwareoathauthenticationmethod.md) objects in the response body.

## Examples

### Request

<!-- {
  "blockType": "request",
  "name": "list_softwareoathauthenticationmethod"
}
-->
``` http
GET https://graph.microsoft.com/v1.0/me/authentication/softwareOathMethods
```

---



### Response
>**Note:** The response object shown here might be shortened for readability.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "Collection(microsoft.graph.softwareOathAuthenticationMethod)"
}
-->
``` http
HTTP/1.1 200 OK
Content-Type: application/json

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.softwareOathAuthenticationMethod",
      "id": "b172893e-893e-b172-3e89-72b13e8972b1",
      "secretKey": null
    }
  ]
}
```
