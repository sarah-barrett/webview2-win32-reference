---
description: Receives `AcceleratorKeyPressed` events.
title: WebView2 Win32 C++ ICoreWebView2AcceleratorKeyPressedEventHandler
ms.date: 10/31/2022
keywords: IWebView2, IWebView2WebView, webview2, webview, win32 apps, win32, edge, ICoreWebView2, ICoreWebView2Controller, browser control, edge html, ICoreWebView2AcceleratorKeyPressedEventHandler
---

# interface ICoreWebView2AcceleratorKeyPressedEventHandler

```
interface ICoreWebView2AcceleratorKeyPressedEventHandler
  : public IUnknown
```

Receives `AcceleratorKeyPressed` events.

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

> public HRESULT [Invoke](#invoke)(ICoreWebView2Controller * sender, ICoreWebView2AcceleratorKeyPressedEventArgs * args)

