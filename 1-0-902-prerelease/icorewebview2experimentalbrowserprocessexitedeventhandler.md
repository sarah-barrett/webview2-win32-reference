---
description: Receives `BrowserProcessExited` events.
title: WebView2 Win32 C++ ICoreWebView2ExperimentalBrowserProcessExitedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/26/2021
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, webview, win32 apps, win32, edge, ICoreWebView2, ICoreWebView2Controller, browser control, edge html, ICoreWebView2ExperimentalBrowserProcessExitedEventHandler
---

# interface ICoreWebView2ExperimentalBrowserProcessExitedEventHandler

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]

[!INCLUDE [prerelease-note](../includes/prerelease-note.md)]

```
interface ICoreWebView2ExperimentalBrowserProcessExitedEventHandler
  : public IUnknown
```

Receives `BrowserProcessExited` events.

## Summary

 Members                        | Descriptions
--------------------------------|---------------------------------------------
[Invoke](#invoke) | Provides the event args for the corresponding event.

## Applies to

Product                         | Introduced
--------------------------------|---------------------------------------------
WebView2 Win32            |    N/A
WebView2 Win32 Prerelease |    1.0.902

## Members

#### Invoke

Provides the event args for the corresponding event.

> public HRESULT [Invoke](#invoke)([ICoreWebView2Environment](icorewebview2environment.md) * sender, [ICoreWebView2ExperimentalBrowserProcessExitedEventArgs](icorewebview2experimentalbrowserprocessexitedeventargs.md) * args)

