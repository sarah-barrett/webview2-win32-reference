---
description: The UpdateRuntime operation result.
title: WebView2 Win32 C++ ICoreWebView2ExperimentalUpdateRuntimeResult
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/26/2021
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, webview, win32 apps, win32, edge, ICoreWebView2, ICoreWebView2Controller, browser control, edge html, ICoreWebView2ExperimentalUpdateRuntimeResult
---

# interface ICoreWebView2ExperimentalUpdateRuntimeResult

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]

[!INCLUDE [prerelease-note](../includes/prerelease-note.md)]

```
interface ICoreWebView2ExperimentalUpdateRuntimeResult
  : public IUnknown
```

The UpdateRuntime operation result.

## Summary

 Members                        | Descriptions
--------------------------------|---------------------------------------------
[get_ExtendedError](#get_extendederror) | The update error happened while trying to update Edge WebView2 Runtime.
[get_Status](#get_status) | The status for the UpdateRuntime operation.

## Applies to

Product                         | Introduced
--------------------------------|---------------------------------------------
WebView2 Win32            |    N/A
WebView2 Win32 Prerelease |    1.0.865

## Members

#### get_ExtendedError

The update error happened while trying to update Edge WebView2 Runtime.

> public HRESULT [get_ExtendedError](#get_extendederror)(HRESULT * error)

ExtendedError will be S_OK if Status is not `COREWEBVIEW2_UPDATE_RUNTIME_STATUS_FAILED` or `COREWEBVIEW2_UPDATE_RUNTIME_STATUS_BLOCKED_BY_POLICY`.

#### get_Status

The status for the UpdateRuntime operation.

> public HRESULT [get_Status](#get_status)(COREWEBVIEW2_UPDATE_RUNTIME_STATUS * status)

