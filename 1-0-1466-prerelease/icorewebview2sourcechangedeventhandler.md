---
description: Receives `SourceChanged` events.
title: WebView2 Win32 C++ ICoreWebView2SourceChangedEventHandler
ms.date: 10/31/2022
keywords: IWebView2, IWebView2WebView, webview2, webview, win32 apps, win32, edge, ICoreWebView2, ICoreWebView2Controller, browser control, edge html, ICoreWebView2SourceChangedEventHandler
---

# interface ICoreWebView2SourceChangedEventHandler

```
interface ICoreWebView2SourceChangedEventHandler
  : public IUnknown
```

Receives `SourceChanged` events.

## Summary

 Members                        | Descriptions
--------------------------------|---------------------------------------------
[Invoke](#invoke) | Provides the event args for the corresponding event.

## Applies to

Product                         | Introduced
--------------------------------|---------------------------------------------
WebView2 Win32            |    0.9.430
WebView2 Win32 Prerelease |    0.9.488

## Members

#### Invoke

Provides the event args for the corresponding event.

> public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) * sender, [ICoreWebView2SourceChangedEventArgs](icorewebview2sourcechangedeventargs.md) * args)

