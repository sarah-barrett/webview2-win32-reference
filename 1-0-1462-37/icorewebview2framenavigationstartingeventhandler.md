---
description: Receives `NavigationStarting` events for iframe.
title: WebView2 Win32 C++ ICoreWebView2FrameNavigationStartingEventHandler
ms.date: 12/05/2022
keywords: IWebView2, IWebView2WebView, webview2, webview, win32 apps, win32, edge, ICoreWebView2, ICoreWebView2Controller, browser control, edge html, ICoreWebView2FrameNavigationStartingEventHandler
---

# interface ICoreWebView2FrameNavigationStartingEventHandler

```
interface ICoreWebView2FrameNavigationStartingEventHandler
  : public IUnknown
```

Receives `NavigationStarting` events for iframe.

## Summary

 Members                        | Descriptions
--------------------------------|---------------------------------------------
[Invoke](#invoke) | Provides the event args for the corresponding event.

## Applies to

Product                         | Introduced
--------------------------------|---------------------------------------------
WebView2 Win32            |    1.0.1108.44
WebView2 Win32 Prerelease |    1.0.1133

## Members

#### Invoke

Provides the event args for the corresponding event.

> public HRESULT [Invoke](#invoke)(ICoreWebView2Frame * sender, ICoreWebView2NavigationStartingEventArgs * args)

