---
title: "Get phoneAuthenticationMethod"
description: "Retrieve a single phoneAuthenticationMethod object for a user."
ms.localizationpriority: medium
author: "mmcla"
ms.prod: "identity-and-sign-in"
doc_type: "apiPageType"
---

# Get phoneAuthenticationMethod

Namespace: microsoft.graph

Retrieve a single [phoneAuthenticationMethod](../resources/phoneauthenticationmethod.md) object for a user. This method is available only for standard Azure AD and B2B users, but not B2C users.

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

For delegated scenarios where an admin is acting on another user, the admin needs one of the following [Azure AD roles](/azure/active-directory/users-groups-roles/directory-assign-admin-roles#available-roles):
* Global administrator
* Global reader
* Privileged authentication administrator
* Authentication administrator (only sees masked phone numbers)

## HTTP request

<!-- { "blockType": "ignored" } -->

```http
GET /me/authentication/phoneMethods/{phoneMethodId}
GET /users/{userId | userPrincipalName}/authentication/phoneMethods/{phoneMethodId}
```
The value of `phoneMethodId` corresponding to the phoneType is one of the following:
+ `b6332ec1-7057-4abe-9331-3d72feddfe41` to retrieve the `alternateMobile` **phoneType**.
+ `e37fc753-ff3b-4958-9484-eaa9425c82bc` to retrieve the `office` **phoneType**.
+ `3179e48a-750b-4051-897c-87b9720928f7` to retrieve the `mobile` **phoneType**.

## Optional query parameters

This method does not support optional query parameters to customize the response.

## Request headers

| Name      |Description|
|:----------|:----------|
| Authorization | Bearer {token}. Required. |

## Request body

Do not supply a request body for this method.

## Response

If successful, this method returns a `200 OK` response code and the requested [phoneAuthenticationMethod](../resources/phoneauthenticationmethod.md) object in the response body.

## Examples

### Request

The following is an example of the request.

<!-- {
  "blockType": "request",
  "name": "get_phoneauthenticationmethod"
}-->

```msgraph-interactive
GET https://graph.microsoft.com/v1.0/me/authentication/phoneMethods/3179e48a-750b-4051-897c-87b9720928f7
```

---


### Response

The following is an example of the response.

> **Note:** The response object shown here might be shortened for readability.

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.phoneAuthenticationMethod"
} -->

```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "phoneNumber": "+1 2065555555",
  "phoneType": "mobile",
  "smsSignInState": "ready",
  "id": "3179e48a-750b-4051-897c-87b9720928f7"
}
```

<!-- uuid: 16cd6b66-4b1a-43a1-adaf-3a886856ed98
2019-02-04 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get phoneAuthenticationMethod",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
