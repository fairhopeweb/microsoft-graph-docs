---
author: JeremyKelley
title: Delete bundle
description: Delete a bundle of driveItems
ms.localizationpriority: medium
ms.prod: "sharepoint"
doc_type: apiPageType
---

# Delete bundle

Namespace: microsoft.graph

Delete a [bundle][] of driveItems by using its **id**.
Note that deleting a bundle using this method permanently deletes the bundle and does not move it to the Recycle Bin.
It does not, however, remove the items that were referenced by the bundle.
They will remain in their parent folders.

## Permissions

One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).

|Permission type      | Permissions (from least to most privileged)              |
|:--------------------|:---------------------------------------------------------|
|Delegated (work or school account) | Not supported.                             |
|Delegated (personal Microsoft account) | Files.ReadWrite, Files.ReadWrite.All   |
|Application          | Not supported.                                           |

## HTTP request

<!-- { "blockType": "ignored" } -->

```http
DELETE /drive/items/{bundle-id}
```

## Request headers

| Name          | Description  |
|:------------- |:------------ |
| Authorization | Bearer \{token\}. Required. |
| if-match      | eTag. Optional. If this request header is included and the eTag (or cTag) provided does not match the current tag on the bundle, a `412 Precondition Failed` response is returned and the bundle will not be deleted.

## Request body

Do not supply a request body with this method.

## Response

If successful, this call returns a `204 No Content` response to indicate that resource was deleted and there was nothing to return.

For information about error responses, see [Error responses][error-response].

## Example

### Request

<!-- { "blockType": "request", "name": "delete-bundle" } -->

```http
DELETE https://graph.microsoft.com/beta/drive/items/{bundle-id}
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
  "description": "Delete a bundle from OneDrive",
  "keywords": "delete,existing bundle,onedrive",
  "section": "documentation",
  "tocPath": "Bundles/Delete"
} -->


