---
description: The shared buffer object.
title: WebView2 Win32 C++ ICoreWebView2ExperimentalSharedBuffer
ms.date: 10/31/2022
keywords: IWebView2, IWebView2WebView, webview2, webview, win32 apps, win32, edge, ICoreWebView2, ICoreWebView2Controller, browser control, edge html, ICoreWebView2ExperimentalSharedBuffer
---

# interface ICoreWebView2ExperimentalSharedBuffer

[!INCLUDE [prerelease-note](../includes/prerelease-note.md)]

```
interface ICoreWebView2ExperimentalSharedBuffer
  : public IUnknown
```

The shared buffer object.

## Summary

 Members                        | Descriptions
--------------------------------|---------------------------------------------
[Close](#close) | Release the backing shared memory.
[get_Buffer](#get_buffer) | The memory address of the shared buffer.
[get_FileMappingHandle](#get_filemappinghandle) | Returns a handle to the file mapping object that backs this shared buffer.
[get_Size](#get_size) | The size of the shared buffer in bytes.
[OpenStream](#openstream) | Get an IStream object that can be used to access the shared buffer.

## Applies to

Product                         | Introduced
--------------------------------|---------------------------------------------
WebView2 Win32            |    N/A
WebView2 Win32 Prerelease |    

## Members

#### Close

Release the backing shared memory.

> public HRESULT [Close](#close)()

The application should call this API when no access to the buffer is needed any more, to ensure that the underlying resources are released timely even if the shared buffer object itself is not released due to some leaked reference. After the shared buffer is closed, the buffer address and file mapping handle previously obtained becomes invalid and cannot be used anymore. Accessing properties of the object will fail with `RO_E_CLOSED`. Operations like Read or Write on the IStream objects returned from `OpenStream` will fail with `RO_E_CLOSED`. `PostSharedBufferToScript` will also fail with `RO_E_CLOSED`.

The script code should call `chrome.webview.releaseBuffer` with the shared buffer as the parameter to release underlying resources as soon as it does not need access the shared buffer any more. When script tries to access the buffer after calling `chrome.webview.releaseBuffer`, JavaScript `TypeError` exception will be raised complaining about accessing a detached ArrayBuffer, the same exception when trying to access a transferred ArrayBuffer.

Closing the buffer object on native side doesn't impact access from Script and releasing the buffer from script doesn't impact access to the buffer from native side. The underlying shared memory will be released by the OS when both native and script side release the buffer.

#### get_Buffer

The memory address of the shared buffer.

> public HRESULT [get_Buffer](#get_buffer)(BYTE ** value)

#### get_FileMappingHandle

Returns a handle to the file mapping object that backs this shared buffer.

> public HRESULT [get_FileMappingHandle](#get_filemappinghandle)(HANDLE * value)

The returned handle is owned by the shared buffer object. You should not call CloseHandle on it. Normal app should use `Buffer` or `OpenStream` to get memory address or IStream object to access the buffer. For advanced scenarios, you could use file mapping APIs to obtain other views or duplicate this handle to another application process and create a view from the duplicated handle in that process to access the buffer from that separate process.

#### get_Size

The size of the shared buffer in bytes.

> public HRESULT [get_Size](#get_size)(UINT64 * value)

#### OpenStream

Get an IStream object that can be used to access the shared buffer.

> public HRESULT [OpenStream](#openstream)(IStream ** value)

