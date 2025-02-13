---
author: JeremyKelley
title: Remove item from bundle
description: Remove item from a bundle of driveItems
ms.localizationpriority: medium
ms.prod: "sharepoint"
doc_type: apiPageType
---

# Remove item from bundle

Namespace: microsoft.graph

Remove an item from a [bundle][].

## Permissions

One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).

|Permission type      | Permissions (from least to most privileged)              |
|:--------------------|:---------------------------------------------------------|
|Delegated (work or school account) | Not supported.                             |
|Delegated (personal Microsoft account) | Files.ReadWrite, Files.ReadWrite.All   |
|Application          | Not supported.                                           |

## HTTP request

```http
DELETE /drive/bundles/{bundle-id}/children/{item-id}
```

## Request headers

| Name          | Description  |
|:------------- |:------------ |
| Authorization | Bearer \{token\}. Required. |

## Request body

Do not supply a request body with this method.

## Response

If successful, the response is `204 No Content`.

For information about error responses, see [Error responses][error-response].

## Example

### Request

<!-- {"blockType": "request", "name": "remove-from-bundle" } -->

```http
DELETE https://graph.microsoft.com/beta/drive/bundles/{bundle-id}/children/{item-id}
```

### Response

<!-- { "blockType": "response" } -->

```http
HTTP/1.1 204 No Content
```


[bundle]: ../resources/bundle.md
[error-response]: /graph/errors

<!-- {
  "type": "#page.annotation",
  "description": "Remove an item from a bundle.",
  "keywords": "",
  "section": "documentation"
} -->


