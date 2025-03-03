---
description: Represents the information regarding the context menu target.
title: WebView2 Win32 C++ ICoreWebView2ExperimentalContextMenuTarget
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/28/2021
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, webview, win32 apps, win32, edge, ICoreWebView2, ICoreWebView2Controller, browser control, edge html, ICoreWebView2ExperimentalContextMenuTarget
---

# interface ICoreWebView2ExperimentalContextMenuTarget

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]

[!INCLUDE [prerelease-note](../includes/prerelease-note.md)]

```
interface ICoreWebView2ExperimentalContextMenuTarget
  : public IUnknown
```

Represents the information regarding the context menu target.

## Summary

 Members                        | Descriptions
--------------------------------|---------------------------------------------
[get_FrameUri](#get_frameuri) | Gets the uri of the frame. Will match the PageUri if `IsRequestedForMainFrame` is TRUE.
[get_HasLinkText](#get_haslinktext) | Returns TRUE if the context menu is requested on text element that contains an anchor tag.
[get_HasLinkUri](#get_haslinkuri) | Returns TRUE if the context menu is requested on HTML containing an anchor tag.
[get_HasSelection](#get_hasselection) | Returns TRUE if the context menu is requested on a selection.
[get_HasSourceUri](#get_hassourceuri) | Returns TRUE if the context menu is requested on HTML containing a source uri.
[get_IsEditable](#get_iseditable) | Returns TRUE if the context menu is requested on an editable component.
[get_IsRequestedForMainFrame](#get_isrequestedformainframe) | Returns TRUE if the context menu was requested on the main frame and FALSE if invoked on another frame.
[get_Kind](#get_kind) | Gets the kind of context that the user selected.
[get_LinkText](#get_linktext) | Gets the text of the link (if `HasLinkText` is TRUE, null otherwise).
[get_LinkUri](#get_linkuri) | Gets the uri of the link (if `HasLinkUri` is TRUE, null otherwise).
[get_PageUri](#get_pageuri) | Gets the uri of the page.
[get_SelectionText](#get_selectiontext) | Gets the selected text (if `HasSelection` is TRUE, null otherwise).
[get_SourceUri](#get_sourceuri) | Gets the active source uri of element (if `HasSourceUri` is TRUE, null otherwise).

Includes the context selected and the appropriate data used for the actions of a context menu.

## Applies to

Product                         | Introduced
--------------------------------|---------------------------------------------
WebView2 Win32            |    N/A
WebView2 Win32 Prerelease |    1.0.1010

## Members

#### get_FrameUri

Gets the uri of the frame. Will match the PageUri if `IsRequestedForMainFrame` is TRUE.

> public HRESULT [get_FrameUri](#get_frameuri)(LPWSTR * value)

#### get_HasLinkText

Returns TRUE if the context menu is requested on text element that contains an anchor tag.

> public HRESULT [get_HasLinkText](#get_haslinktext)(BOOL * value)

#### get_HasLinkUri

Returns TRUE if the context menu is requested on HTML containing an anchor tag.

> public HRESULT [get_HasLinkUri](#get_haslinkuri)(BOOL * value)

#### get_HasSelection

Returns TRUE if the context menu is requested on a selection.

> public HRESULT [get_HasSelection](#get_hasselection)(BOOL * value)

#### get_HasSourceUri

Returns TRUE if the context menu is requested on HTML containing a source uri.

> public HRESULT [get_HasSourceUri](#get_hassourceuri)(BOOL * value)

#### get_IsEditable

Returns TRUE if the context menu is requested on an editable component.

> public HRESULT [get_IsEditable](#get_iseditable)(BOOL * value)

#### get_IsRequestedForMainFrame

Returns TRUE if the context menu was requested on the main frame and FALSE if invoked on another frame.

> public HRESULT [get_IsRequestedForMainFrame](#get_isrequestedformainframe)(BOOL * value)

#### get_Kind

Gets the kind of context that the user selected.

> public HRESULT [get_Kind](#get_kind)(COREWEBVIEW2_CONTEXT_MENU_TARGET_KIND * value)

#### get_LinkText

Gets the text of the link (if `HasLinkText` is TRUE, null otherwise).

> public HRESULT [get_LinkText](#get_linktext)(LPWSTR * value)

#### get_LinkUri

Gets the uri of the link (if `HasLinkUri` is TRUE, null otherwise).

> public HRESULT [get_LinkUri](#get_linkuri)(LPWSTR * value)

#### get_PageUri

Gets the uri of the page.

> public HRESULT [get_PageUri](#get_pageuri)(LPWSTR * value)

#### get_SelectionText

Gets the selected text (if `HasSelection` is TRUE, null otherwise).

> public HRESULT [get_SelectionText](#get_selectiontext)(LPWSTR * value)

#### get_SourceUri

Gets the active source uri of element (if `HasSourceUri` is TRUE, null otherwise).

> public HRESULT [get_SourceUri](#get_sourceuri)(LPWSTR * value)

