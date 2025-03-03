---
description: The ICoreWebView2Settings Experimental interface for AreBrowserAcceleratorKeysEnabled.
title: WebView2 Win32 C++ ICoreWebView2ExperimentalSettings2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/23/2021
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, webview, win32 apps, win32, edge, ICoreWebView2, ICoreWebView2Controller, browser control, edge html, ICoreWebView2ExperimentalSettings2
---

# interface ICoreWebView2ExperimentalSettings2

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]

[!INCLUDE [prerelease-note](../includes/prerelease-note.md)]

```
interface ICoreWebView2ExperimentalSettings2
  : public IUnknown
```

The [ICoreWebView2Settings](icorewebview2settings.md) Experimental interface for AreBrowserAcceleratorKeysEnabled.

## Summary

 Members                        | Descriptions
--------------------------------|---------------------------------------------
[get_AreBrowserAcceleratorKeysEnabled](#get_arebrowseracceleratorkeysenabled) | When this setting is set to FALSE, it disables all accelerator keys that access features specific to a web browser, including but not limited to:
[put_AreBrowserAcceleratorKeysEnabled](#put_arebrowseracceleratorkeysenabled) | Sets the `AreBrowserAcceleratorKeysEnabled` property.

## Applies to

Product                         | Introduced
--------------------------------|---------------------------------------------
WebView2 Win32            |    N/A
WebView2 Win32 Prerelease |    1.0.824

## Members

#### get_AreBrowserAcceleratorKeysEnabled

When this setting is set to FALSE, it disables all accelerator keys that access features specific to a web browser, including but not limited to:

> public HRESULT [get_AreBrowserAcceleratorKeysEnabled](#get_arebrowseracceleratorkeysenabled)(BOOL * areBrowserAcceleratorKeysEnabled)

* Ctrl-F and F3 for Find on Page

* Ctrl-P for Print

* Ctrl-R and F5 for Reload

* Ctrl-Plus and Ctrl-Minus for zooming

* Ctrl-Shift-C and F12 for DevTools

* Special keys for browser functions, such as Back, Forward, and Search

It does not disable accelerator keys related to movement and text editing, such as:

* Home, End, Page Up, and Page Down

* Ctrl-X, Ctrl-C, Ctrl-V

* Ctrl-A for Select All

* Ctrl-Z for Undo

Those accelerator keys will always be enabled unless they are handled in the `AcceleratorKeyPressed` event.

This setting has no effect on the `AcceleratorKeyPressed` event. The event will be fired for all accelerator keys, whether they are enabled or not.

The default value for `AreBrowserAcceleratorKeysEnabled` is TRUE.

```cpp
            auto experimental_settings = m_settings.try_query<ICoreWebView2ExperimentalSettings2>();
            CHECK_FEATURE_RETURN(experimental_settings);
            BOOL enabled;
            CHECK_FAILURE(experimental_settings->get_AreBrowserAcceleratorKeysEnabled(&enabled));
            if (enabled)
            {
                CHECK_FAILURE(experimental_settings->put_AreBrowserAcceleratorKeysEnabled(FALSE));
                MessageBox(
                    nullptr, L"Browser-specific accelerator keys will be disabled after the next navigation.",
                    L"Settings change", MB_OK);
            }
            else
            {
                CHECK_FAILURE(experimental_settings->put_AreBrowserAcceleratorKeysEnabled(TRUE));
                MessageBox(
                    nullptr, L"Browser-specific accelerator keys will be enabled after the next navigation.",
                    L"Settings change", MB_OK);
            }
```

#### put_AreBrowserAcceleratorKeysEnabled

Sets the `AreBrowserAcceleratorKeysEnabled` property.

> public HRESULT [put_AreBrowserAcceleratorKeysEnabled](#put_arebrowseracceleratorkeysenabled)(BOOL areBrowserAcceleratorKeysEnabled)

