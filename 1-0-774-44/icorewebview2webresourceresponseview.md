---
description: View of the HTTP representation for a web resource response.
title: WebView2 Win32 C++ ICoreWebView2WebResourceResponseView
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/08/2021
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, webview, win32 apps, win32, edge, ICoreWebView2, ICoreWebView2Controller, browser control, edge html, ICoreWebView2WebResourceResponseView
---

# interface ICoreWebView2WebResourceResponseView 

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]

```
interface ICoreWebView2WebResourceResponseView
  : public IUnknown
```

View of the HTTP representation for a web resource response.

## Summary

 Members                        | Descriptions
--------------------------------|---------------------------------------------
[get_Headers](#get_headers) | The HTTP response headers as received.
[get_ReasonPhrase](#get_reasonphrase) | The HTTP response reason phrase.
[get_StatusCode](#get_statuscode) | The HTTP response status code.
[GetContent](#getcontent) | Get the response content asynchronously.

The properties of this object are not mutable. This response view is used with the WebResourceResponseReceived event.

## Applies to

Product                         | Introduced
--------------------------------|---------------------------------------------
WebView2 Win32            |    1.0.705.50
WebView2 Win32 Prerelease |    1.0.721

## Members

#### get_Headers 

The HTTP response headers as received.

> public HRESULT [get_Headers](#get_headers)([ICoreWebView2HttpResponseHeaders](icorewebview2httpresponseheaders.md) ** headers)

#### get_ReasonPhrase 

The HTTP response reason phrase.

> public HRESULT [get_ReasonPhrase](#get_reasonphrase)(LPWSTR * reasonPhrase)

#### get_StatusCode 

The HTTP response status code.

> public HRESULT [get_StatusCode](#get_statuscode)(int * statusCode)

#### GetContent 

Get the response content asynchronously.

> public HRESULT [GetContent](#getcontent)([ICoreWebView2WebResourceResponseViewGetContentCompletedHandler](icorewebview2webresourceresponseviewgetcontentcompletedhandler.md) * handler)

The handler will receive the response content stream. If this method is being called again before a first call has completed, the handler will be invoked at the same time the handlers from prior calls are invoked. If this method is being called after a first call has completed, the handler will be invoked immediately. 
```cpp
                    webResourceResponse->GetContent(
                        Callback<
                            ICoreWebView2WebResourceResponseViewGetContentCompletedHandler>(
                            [this, webResourceRequest,
                             webResourceResponse](HRESULT result, IStream* content) {
                                std::wstring message =
                                    L"{ \"kind\": \"event\", \"name\": "
                                    L"\"WebResourceResponseReceived\", \"args\": {"
                                    L"\"request\": " +
                                    RequestToJsonString(webResourceRequest.get()) +
                                    L", "
                                    L"\"response\": " +
                                    ResponseToJsonString(webResourceResponse.get(), content) +
                                    L"}";

                                message +=
                                    WebViewPropertiesToJsonString(m_webviewEventSource.get());
                                message += L"}";
                                PostEventMessage(message);
                                return S_OK;
                            })
                            .Get());
```

