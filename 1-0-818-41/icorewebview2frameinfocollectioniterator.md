---
description: Iterator for a collection of `FrameInfo`s.
title: WebView2 Win32 C++ ICoreWebView2FrameInfoCollectionIterator
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/01/2021
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, webview, win32 apps, win32, edge, ICoreWebView2, ICoreWebView2Controller, browser control, edge html, ICoreWebView2FrameInfoCollectionIterator
---

# interface ICoreWebView2FrameInfoCollectionIterator

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]

```
interface ICoreWebView2FrameInfoCollectionIterator
  : public IUnknown
```

Iterator for a collection of `FrameInfo`s.

## Summary

 Members                        | Descriptions
--------------------------------|---------------------------------------------
[get_HasCurrent](#get_hascurrent) | `TRUE` when the iterator has not run out of `FrameInfo`s.
[GetCurrent](#getcurrent) | Get the current ICoreWebView2FrameInfo of the iterator.
[MoveNext](#movenext) | Move the iterator to the next `FrameInfo` in the collection.

For more info, see ICoreWebView2ProcessFailedEventArgs2 and ICoreWebView2FrameInfoCollection.

## Applies to

Product                         | Introduced
--------------------------------|---------------------------------------------
WebView2 Win32            |    1.0.774.44
WebView2 Win32 Prerelease |    1.0.824

## Members

#### get_HasCurrent

`TRUE` when the iterator has not run out of `FrameInfo`s.

> public HRESULT [get_HasCurrent](#get_hascurrent)(BOOL * hasCurrent)

If the collection over which the iterator is iterating is empty or if the iterator has gone past the end of the collection, then this is `FALSE`.

#### GetCurrent

Get the current ICoreWebView2FrameInfo of the iterator.

> public HRESULT [GetCurrent](#getcurrent)(ICoreWebView2FrameInfo ** frameInfo)

#### MoveNext

Move the iterator to the next `FrameInfo` in the collection.

> public HRESULT [MoveNext](#movenext)(BOOL * hasNext)

