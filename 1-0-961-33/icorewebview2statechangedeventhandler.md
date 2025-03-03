---
description: Implements the interface to receive `StateChanged` event.
title: WebView2 Win32 C++ ICoreWebView2StateChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/27/2021
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, webview, win32 apps, win32, edge, ICoreWebView2, ICoreWebView2Controller, browser control, edge html, ICoreWebView2StateChangedEventHandler
---

# interface ICoreWebView2StateChangedEventHandler

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]

```
interface ICoreWebView2StateChangedEventHandler
  : public IUnknown
```

Implements the interface to receive `StateChanged` event.

## Summary

 Members                        | Descriptions
--------------------------------|---------------------------------------------
[Invoke](#invoke) | Provides the event args for the corresponding event.

Use the `ICoreWebView2DownloadOperation.State` property to get the current state, which can be in progress, interrupted, or completed. Use the `ICoreWebView2DownloadOperation.InterruptReason` property to get the interrupt reason if the download is interrupted.

## Applies to

Product                         | Introduced
--------------------------------|---------------------------------------------
WebView2 Win32            |    1.0.902.49
WebView2 Win32 Prerelease |    1.0.902

## Members

#### Invoke

Provides the event args for the corresponding event.

> public HRESULT [Invoke](#invoke)([ICoreWebView2DownloadOperation](icorewebview2downloadoperation.md) * sender, IUnknown * args)

No event args exist and the `args` parameter is set to `null`.

