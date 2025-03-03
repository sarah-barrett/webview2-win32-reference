---
description: Receives the result of the `GetCookies` method.
title: WebView2 Win32 C++ ICoreWebView2GetCookiesCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/23/2021
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, webview, win32 apps, win32, edge, ICoreWebView2, ICoreWebView2Controller, browser control, edge html, ICoreWebView2GetCookiesCompletedHandler
---

# interface ICoreWebView2GetCookiesCompletedHandler

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]

```
interface ICoreWebView2GetCookiesCompletedHandler
  : public IUnknown
```

Receives the result of the `GetCookies` method.

## Summary

 Members                        | Descriptions
--------------------------------|---------------------------------------------
[Invoke](#invoke) | Provides the completion status of the corresponding asynchronous method call.

The result is written to the cookie list provided in the `GetCookies` method call.

## Applies to

Product                         | Introduced
--------------------------------|---------------------------------------------
WebView2 Win32            |    1.0.705.50
WebView2 Win32 Prerelease |    1.0.721

## Members

#### Invoke

Provides the completion status of the corresponding asynchronous method call.

> public HRESULT [Invoke](#invoke)(HRESULT result, [ICoreWebView2CookieList](icorewebview2cookielist.md) * cookieList)

