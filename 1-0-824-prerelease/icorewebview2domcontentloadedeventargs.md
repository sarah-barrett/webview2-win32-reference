---
description: Event args for the DOMContentLoaded event.
title: WebView2 Win32 C++ ICoreWebView2DOMContentLoadedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/23/2021
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, webview, win32 apps, win32, edge, ICoreWebView2, ICoreWebView2Controller, browser control, edge html, ICoreWebView2DOMContentLoadedEventArgs
---

# interface ICoreWebView2DOMContentLoadedEventArgs

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]

```
interface ICoreWebView2DOMContentLoadedEventArgs
  : public IUnknown
```

Event args for the DOMContentLoaded event.

## Summary

 Members                        | Descriptions
--------------------------------|---------------------------------------------
[get_NavigationId](#get_navigationid) | The ID of the navigation which corresponds to other navigation ID properties on other navigation events.

## Applies to

Product                         | Introduced
--------------------------------|---------------------------------------------
WebView2 Win32            |    1.0.705.50
WebView2 Win32 Prerelease |    1.0.721

## Members

#### get_NavigationId

The ID of the navigation which corresponds to other navigation ID properties on other navigation events.

> public HRESULT [get_NavigationId](#get_navigationid)(UINT64 * navigationId)

