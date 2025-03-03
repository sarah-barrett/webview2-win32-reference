---
description: Provides a set of properties for a frame in the ICoreWebView2.
title: WebView2 Win32 C++ ICoreWebView2FrameInfo
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/14/2021
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, webview, win32 apps, win32, edge, ICoreWebView2, ICoreWebView2Controller, browser control, edge html, ICoreWebView2FrameInfo
---

# interface ICoreWebView2FrameInfo

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]

```
interface ICoreWebView2FrameInfo
  : public IUnknown
```

Provides a set of properties for a frame in the [ICoreWebView2](icorewebview2.md).

## Summary

 Members                        | Descriptions
--------------------------------|---------------------------------------------
[get_Name](#get_name) | The name attribute of the frame, as in `<iframe name="frame-name" ...>`.
[get_Source](#get_source) | The URI of the document in the frame.

## Applies to

Product                         | Introduced
--------------------------------|---------------------------------------------
WebView2 Win32            |    1.0.818.41
WebView2 Win32 Prerelease |    1.0.824

## Members

#### get_Name

The name attribute of the frame, as in `<iframe name="frame-name" ...>`.

> public HRESULT [get_Name](#get_name)(LPWSTR * name)

The returned string is empty when the frame has no name attribute.

#### get_Source

The URI of the document in the frame.

> public HRESULT [get_Source](#get_source)(LPWSTR * source)

