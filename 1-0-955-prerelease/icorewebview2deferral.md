---
description: This interface is used to complete deferrals on event args that support getting deferrals using the `GetDeferral` method.
title: WebView2 Win32 C++ ICoreWebView2Deferral
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/14/2021
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, webview, win32 apps, win32, edge, ICoreWebView2, ICoreWebView2Controller, browser control, edge html, ICoreWebView2Deferral
---

# interface ICoreWebView2Deferral

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]

```
interface ICoreWebView2Deferral
  : public IUnknown
```

This interface is used to complete deferrals on event args that support getting deferrals using the `GetDeferral` method.

## Summary

 Members                        | Descriptions
--------------------------------|---------------------------------------------
[Complete](#complete) | Completes the associated deferred event.

## Applies to

Product                         | Introduced
--------------------------------|---------------------------------------------
WebView2 Win32            |    0.9.430
WebView2 Win32 Prerelease |    0.9.488

## Members

#### Complete

Completes the associated deferred event.

> public HRESULT [Complete](#complete)()

Complete should only be run once for each deferral taken.

