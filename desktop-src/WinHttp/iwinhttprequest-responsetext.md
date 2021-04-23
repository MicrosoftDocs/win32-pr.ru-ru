---
description: Извлекает текст объекта ответа в виде текста.
ms.assetid: 87caf64f-be11-45c9-af1e-997a55c5e76e
title: 'Свойство Ивинхттпрекуест:: Респонсетекст'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWinHttpRequest.ResponseText
- IWinHttpRequest.get_ResponseText
- WinHttpRequest.ResponseText
api_type:
- COM
api_location:
- Winhttp.dll
ms.openlocfilehash: 93e0a9b17ba356f9ce6b038be114f5f2c9804eab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712550"
---
# <a name="iwinhttprequestresponsetext-property"></a><span data-ttu-id="b8f43-103">Свойство Ивинхттпрекуест:: Респонсетекст</span><span class="sxs-lookup"><span data-stu-id="b8f43-103">IWinHttpRequest::ResponseText property</span></span>

<span data-ttu-id="b8f43-104">Свойство **респонсетекст** извлекает текст сущности ответа в виде текста.</span><span class="sxs-lookup"><span data-stu-id="b8f43-104">The **ResponseText** property retrieves the response entity body as text.</span></span>

<span data-ttu-id="b8f43-105">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="b8f43-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8f43-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b8f43-106">Syntax</span></span>


```C++
HRESULT get_ResponseText(
  [out, retval] BSTR *Body
);
```


```JScript

strResponseText = WinHttpRequest.ResponseText
```





## <a name="property-value"></a><span data-ttu-id="b8f43-107">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="b8f43-107">Property value</span></span>

<span data-ttu-id="b8f43-108">**BSTR** , получающий текст сущности ответа в виде текста.</span><span class="sxs-lookup"><span data-stu-id="b8f43-108">**BSTR** that receives the entity body of the response as text.</span></span>

## <a name="error-codes"></a><span data-ttu-id="b8f43-109">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="b8f43-109">Error codes</span></span>

<span data-ttu-id="b8f43-110">В случае успешного выполнения возвращается значение **S \_** , а в противном случае — значение ошибки.</span><span class="sxs-lookup"><span data-stu-id="b8f43-110">The return value is **S\_OK** on success or an error value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="b8f43-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b8f43-111">Remarks</span></span>

<span data-ttu-id="b8f43-112">Это свойство может быть вызвано только после вызова метода [**Send**](iwinhttprequest-send.md) .</span><span class="sxs-lookup"><span data-stu-id="b8f43-112">This property can only be invoked after the [**Send**](iwinhttprequest-send.md) method has been called.</span></span>

<span data-ttu-id="b8f43-113">При использовании этого свойства в синхронном режиме ограничение числа возвращаемых символов составляет примерно 2 169 895.</span><span class="sxs-lookup"><span data-stu-id="b8f43-113">When using this property in synchronous mode, the limit to the number of characters it returns is approximately 2,169,895.</span></span>

> [!Note]  
> <span data-ttu-id="b8f43-114">Для Windows XP и Windows 2000 см. раздел [требования к времени выполнения](winhttp-start-page.md) на начальной странице WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="b8f43-114">For Windows XP and Windows 2000, see the [Run-Time Requirements](winhttp-start-page.md) section of the WinHTTP Start Page.</span></span>

 

## <a name="examples"></a><span data-ttu-id="b8f43-115">Примеры</span><span class="sxs-lookup"><span data-stu-id="b8f43-115">Examples</span></span>

<span data-ttu-id="b8f43-116">В следующем примере показано, как открыть HTTP-соединение, отправить HTTP-запрос и прочитать текст ответа.</span><span class="sxs-lookup"><span data-stu-id="b8f43-116">The following example shows how to open an HTTP connection, send an HTTP request, and read the response text.</span></span> <span data-ttu-id="b8f43-117">Этот пример необходимо запустить из командной строки.</span><span class="sxs-lookup"><span data-stu-id="b8f43-117">This example must be run from a command prompt.</span></span>


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
    {   // Open WinHttpRequest.
        BSTR bstrMethod  = SysAllocString(L"GET");
        BSTR bstrUrl = SysAllocString(L"https://microsoft.com");
        hr = pIWinHttpRequest->Open(bstrMethod, bstrUrl, varFalse);
        SysFreeString(bstrMethod);
        SysFreeString(bstrUrl);
    }
    if (SUCCEEDED(hr))
    {   // Send Request.
        hr = pIWinHttpRequest->Send(varEmpty);
    }
    if (SUCCEEDED(hr))
    {   // Get Response text.
        hr = pIWinHttpRequest->get_ResponseText(&bstrResponse);
    }

    // Print the response to a console.
    wprintf(L"%.256s",bstrResponse);

    // Release memory.
    if (pIWinHttpRequest)
        pIWinHttpRequest->Release();
    if (bstrResponse)
        SysFreeString(bstrResponse);

    CoUninitialize();
    return 0;
}

```



<span data-ttu-id="b8f43-118">В следующем примере скрипта показано, как открыть HTTP-соединение, отправить HTTP-запрос и прочитать текст ответа.</span><span class="sxs-lookup"><span data-stu-id="b8f43-118">The following scripting example shows how to open an HTTP connection, send an HTTP request, and read the response text.</span></span>


```JScript
// Instantiate a WinHttpRequest object.
var WinHttpReq = new ActiveXObject("WinHttp.WinHttpRequest.5.1");

// Initialize an HTTP request.  
WinHttpReq.Open("GET", "https://www.microsoft.com", false);

// Send the HTTP request.
WinHttpReq.Send(); 

// Display the response text.
WScript.Echo( WinHttpReq.ResponseText);
```



## <a name="requirements"></a><span data-ttu-id="b8f43-119">Требования</span><span class="sxs-lookup"><span data-stu-id="b8f43-119">Requirements</span></span>



| <span data-ttu-id="b8f43-120">Требование</span><span class="sxs-lookup"><span data-stu-id="b8f43-120">Requirement</span></span> | <span data-ttu-id="b8f43-121">Значение</span><span class="sxs-lookup"><span data-stu-id="b8f43-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="b8f43-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b8f43-122">Minimum supported client</span></span><br/> | <span data-ttu-id="b8f43-123">Windows XP, Windows 2000 Professional с пакетом обновления 3 (SP3), \[ только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b8f43-123">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="b8f43-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b8f43-124">Minimum supported server</span></span><br/> | <span data-ttu-id="b8f43-125">Windows Server 2003, Windows 2000 Server с пакетом обновления 3 (SP3), \[ только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b8f43-125">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>         |
| <span data-ttu-id="b8f43-126">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="b8f43-126">Redistributable</span></span><br/>          | <span data-ttu-id="b8f43-127">WinHTTP 5,0 и Internet Explorer 5,01 или более поздней версии в Windows XP и Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="b8f43-127">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span><br/> |
| <span data-ttu-id="b8f43-128">IDL</span><span class="sxs-lookup"><span data-stu-id="b8f43-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b8f43-129"><dt>HttpRequest. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b8f43-129"><dt>HttpRequest.idl</dt></span></span> </dl> |
| <span data-ttu-id="b8f43-130">Библиотека</span><span class="sxs-lookup"><span data-stu-id="b8f43-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="b8f43-131"><dt>WinHTTP. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b8f43-131"><dt>Winhttp.lib</dt></span></span> </dl>     |
| <span data-ttu-id="b8f43-132">DLL</span><span class="sxs-lookup"><span data-stu-id="b8f43-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b8f43-133"><dt>Winhttp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b8f43-133"><dt>Winhttp.dll</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="b8f43-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b8f43-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8f43-135">**ивинхттпрекуест**</span><span class="sxs-lookup"><span data-stu-id="b8f43-135">**IWinHttpRequest**</span></span>](iwinhttprequest-interface.md)
</dt> <dt>

[<span data-ttu-id="b8f43-136">**WinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="b8f43-136">**WinHttpRequest**</span></span>](winhttprequest.md)
</dt> <dt>

[<span data-ttu-id="b8f43-137">**респонсебоди**</span><span class="sxs-lookup"><span data-stu-id="b8f43-137">**ResponseBody**</span></span>](iwinhttprequest-responsebody.md)
</dt> <dt>

[<span data-ttu-id="b8f43-138">**ResponseStream**</span><span class="sxs-lookup"><span data-stu-id="b8f43-138">**ResponseStream**</span></span>](iwinhttprequest-responsestream.md)
</dt> <dt>

[<span data-ttu-id="b8f43-139">Версии WinHTTP</span><span class="sxs-lookup"><span data-stu-id="b8f43-139">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

 




