---
description: Извлекает текст состояния HTTP.
ms.assetid: 480babbd-432c-4722-98df-a73ba5928e1f
title: 'Свойство Ивинхттпрекуест:: StatusText'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWinHttpRequest.StatusText
- IWinHttpRequest.get_StatusText
- WinHttpRequest.StatusText
api_type:
- COM
api_location:
- Winhttp.dll
ms.openlocfilehash: 41288d87b8194caf3a2a14cc89cd5acbffec902c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104081603"
---
# <a name="iwinhttprequeststatustext-property"></a><span data-ttu-id="68aba-103">Свойство Ивинхттпрекуест:: StatusText</span><span class="sxs-lookup"><span data-stu-id="68aba-103">IWinHttpRequest::StatusText property</span></span>

<span data-ttu-id="68aba-104">Свойство **StatusText** извлекает текст состояния HTTP.</span><span class="sxs-lookup"><span data-stu-id="68aba-104">The **StatusText** property retrieves the HTTP status text.</span></span>

<span data-ttu-id="68aba-105">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="68aba-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="68aba-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="68aba-106">Syntax</span></span>


```C++
HRESULT get_StatusText(
  [out, retval] BSTR *Status
);
```


```JScript

StatusText = WinHttpRequest.StatusText
```





## <a name="property-value"></a><span data-ttu-id="68aba-107">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="68aba-107">Property value</span></span>

<span data-ttu-id="68aba-108">**BSTR** , получающий текст состояния HTTP.</span><span class="sxs-lookup"><span data-stu-id="68aba-108">**BSTR** that receives the HTTP status text.</span></span>

## <a name="error-codes"></a><span data-ttu-id="68aba-109">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="68aba-109">Error codes</span></span>

<span data-ttu-id="68aba-110">В случае успешного выполнения возвращается значение **S \_** , а в противном случае — значение ошибки.</span><span class="sxs-lookup"><span data-stu-id="68aba-110">The return value is **S\_OK** on success or an error value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="68aba-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="68aba-111">Remarks</span></span>

<span data-ttu-id="68aba-112">Извлекает текстовую часть строки ответа сервера, делая доступным "понятный" для пользователя эквивалент числового кода состояния HTTP.</span><span class="sxs-lookup"><span data-stu-id="68aba-112">Retrieves the text portion of the server response line, making available the "user-friendly" equivalent to the numeric HTTP status code.</span></span> <span data-ttu-id="68aba-113">Результаты этого свойства действительны только после успешного завершения метода [**Send**](iwinhttprequest-send.md) .</span><span class="sxs-lookup"><span data-stu-id="68aba-113">The results of this property are valid only after the [**Send**](iwinhttprequest-send.md) method has successfully completed.</span></span>

> [!Note]  
> <span data-ttu-id="68aba-114">Для Windows XP и Windows 2000 см. раздел [требования к времени выполнения](winhttp-start-page.md) на начальной странице WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="68aba-114">For Windows XP and Windows 2000, see the [Run-Time Requirements](winhttp-start-page.md) section of the WinHTTP Start Page.</span></span>

 

## <a name="examples"></a><span data-ttu-id="68aba-115">Примеры</span><span class="sxs-lookup"><span data-stu-id="68aba-115">Examples</span></span>

<span data-ttu-id="68aba-116">В следующем примере показано, как открыть HTTP-соединение, отправить HTTP-запрос, отобразить [**состояние**](iwinhttprequest-status.md) и **StatusText**, а также прочитать текст ответа.</span><span class="sxs-lookup"><span data-stu-id="68aba-116">The following example shows how to open an HTTP connection, send an HTTP request, display the [**Status**](iwinhttprequest-status.md) and **StatusText**, and read the response text.</span></span> <span data-ttu-id="68aba-117">Этот пример необходимо запустить из командной строки.</span><span class="sxs-lookup"><span data-stu-id="68aba-117">This example must be run from a command prompt.</span></span>


```C++
#include <windows.h>
#include <stdio.h>
#include <objbase.h>

#include "httprequest.h"

#pragma comment(lib, "ole32.lib")
#pragma comment(lib, "oleaut32.lib")

// IID for IWinHttpRequest.
const IID IID_IWinHttpRequest =
{
  0x06f29373,
  0x5c5a,
  0x4b54,
  {0xb0, 0x25, 0x6e, 0xf1, 0xbf, 0x8a, 0xbf, 0x0e}
};

int main()
{
    // Variable for return value
    HRESULT    hr;

    // Initialize COM.
    hr = CoInitialize( NULL );

    IWinHttpRequest *  pIWinHttpRequest = NULL;

    BSTR            bstrResponse = NULL;
    VARIANT         varFalse;
    VARIANT         varEmpty;
    LONG            lStatus = 0;
    BSTR            bstrStatusText = NULL;

    CLSID           clsid;

    VariantInit(&varFalse);
    V_VT(&varFalse)   = VT_BOOL;
    V_BOOL(&varFalse) = VARIANT_FALSE;

    VariantInit(&varEmpty);
    V_VT(&varEmpty) = VT_ERROR;

    hr = CLSIDFromProgID(L"WinHttp.WinHttpRequest.5.1", &clsid);

    if (SUCCEEDED(hr))
    {
        hr = CoCreateInstance(clsid, NULL,
                              CLSCTX_INPROC_SERVER,
                              IID_IWinHttpRequest,
                              (void **)&pIWinHttpRequest);
    }
    if (SUCCEEDED(hr))
    {    // Open WinHttpRequest.
        BSTR bstrMethod  = SysAllocString(L"GET");
        BSTR bstrUrl = SysAllocString(L"https://microsoft.com");
        hr = pIWinHttpRequest->Open(bstrMethod, bstrUrl, varFalse);
        SysFreeString(bstrMethod);
        SysFreeString(bstrUrl);
    }
    if (SUCCEEDED(hr))
    {    // Send Request.
        hr = pIWinHttpRequest->Send(varEmpty);
    }
    if (SUCCEEDED(hr))
    {    // Send Request.
        hr = pIWinHttpRequest->get_Status(&lStatus);
        hr = pIWinHttpRequest->get_StatusText(&bstrStatusText);
    }
    if (SUCCEEDED(hr))
    {    // Get Response text.
        hr = pIWinHttpRequest->GetAllResponseHeaders(&bstrResponse);
    }
    if (SUCCEEDED(hr))
    {    // Print response to console.
        wprintf(L"%s\n\n", bstrResponse);
        wprintf(L"%u - %s\n\n", lStatus, bstrStatusText);
    }

    // Release memory.
    if (pIWinHttpRequest)
        pIWinHttpRequest->Release();
    if (bstrStatusText)
        SysFreeString(bstrStatusText);
    if (bstrResponse)
        SysFreeString(bstrResponse);

    CoUninitialize();
    return 0;
}

```



<span data-ttu-id="68aba-118">В следующем примере скрипта показано, как открыть HTTP-соединение, отправить HTTP-запрос, отобразить [**состояние**](iwinhttprequest-status.md) и **StatusText**, а также прочитать заголовки ответа.</span><span class="sxs-lookup"><span data-stu-id="68aba-118">The following scripting example shows how to open an HTTP connection, send an HTTP request, display the [**Status**](iwinhttprequest-status.md) and **StatusText**, and read the response headers.</span></span>


```JScript
// Instantiate a WinHttpRequest object.
var WinHttpReq = new ActiveXObject("WinHttp.WinHttpRequest.5.1");

// Initialize an HTTP request.  
WinHttpReq.Open("GET", "https://www.microsoft.com", false);

// Send the HTTP request.
WinHttpReq.Send(); 

// Display the status.
WScript.Echo( WinHttpReq.Status + " - " + WinHttpReq.StatusText);

// Display the date header.
WScript.Echo( WinHttpReq.GetAllResponseHeaders());
```



## <a name="requirements"></a><span data-ttu-id="68aba-119">Требования</span><span class="sxs-lookup"><span data-stu-id="68aba-119">Requirements</span></span>



| <span data-ttu-id="68aba-120">Требование</span><span class="sxs-lookup"><span data-stu-id="68aba-120">Requirement</span></span> | <span data-ttu-id="68aba-121">Значение</span><span class="sxs-lookup"><span data-stu-id="68aba-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="68aba-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="68aba-122">Minimum supported client</span></span><br/> | <span data-ttu-id="68aba-123">Windows XP, Windows 2000 Professional с пакетом обновления 3 (SP3), \[ только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="68aba-123">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="68aba-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="68aba-124">Minimum supported server</span></span><br/> | <span data-ttu-id="68aba-125">Windows Server 2003, Windows 2000 Server с пакетом обновления 3 (SP3), \[ только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="68aba-125">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>         |
| <span data-ttu-id="68aba-126">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="68aba-126">Redistributable</span></span><br/>          | <span data-ttu-id="68aba-127">WinHTTP 5,0 и Internet Explorer 5,01 или более поздней версии в Windows XP и Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="68aba-127">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span><br/> |
| <span data-ttu-id="68aba-128">IDL</span><span class="sxs-lookup"><span data-stu-id="68aba-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="68aba-129"><dt>HttpRequest. idl</dt></span><span class="sxs-lookup"><span data-stu-id="68aba-129"><dt>HttpRequest.idl</dt></span></span> </dl> |
| <span data-ttu-id="68aba-130">Библиотека</span><span class="sxs-lookup"><span data-stu-id="68aba-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="68aba-131"><dt>WinHTTP. lib</dt></span><span class="sxs-lookup"><span data-stu-id="68aba-131"><dt>Winhttp.lib</dt></span></span> </dl>     |
| <span data-ttu-id="68aba-132">DLL</span><span class="sxs-lookup"><span data-stu-id="68aba-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="68aba-133"><dt>Winhttp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="68aba-133"><dt>Winhttp.dll</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="68aba-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="68aba-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68aba-135">**ивинхттпрекуест**</span><span class="sxs-lookup"><span data-stu-id="68aba-135">**IWinHttpRequest**</span></span>](iwinhttprequest-interface.md)
</dt> <dt>

[<span data-ttu-id="68aba-136">**WinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="68aba-136">**WinHttpRequest**</span></span>](winhttprequest.md)
</dt> <dt>

[<span data-ttu-id="68aba-137">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="68aba-137">**Status**</span></span>](iwinhttprequest-status.md)
</dt> <dt>

[<span data-ttu-id="68aba-138">Версии WinHTTP</span><span class="sxs-lookup"><span data-stu-id="68aba-138">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

 




