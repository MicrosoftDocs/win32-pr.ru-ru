---
description: Извлекает заголовки HTTP-ответа.
ms.assetid: 3d59ee83-280c-4074-82e1-ded203fa1049
title: 'Метод Ивинхттпрекуест:: Жетреспонсехеадер'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWinHttpRequest.GetResponseHeader
- WinHttpRequest.GetResponseHeader
api_type:
- COM
api_location:
- Winhttp.dll
ms.openlocfilehash: 6e51b0973c7b078c7de592565db19bf6e029c5a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702889"
---
# <a name="iwinhttprequestgetresponseheader-method"></a><span data-ttu-id="8f1cd-103">Метод Ивинхттпрекуест:: Жетреспонсехеадер</span><span class="sxs-lookup"><span data-stu-id="8f1cd-103">IWinHttpRequest::GetResponseHeader method</span></span>

<span data-ttu-id="8f1cd-104">Метод **жетреспонсехеадер** извлекает заголовки HTTP-ответа.</span><span class="sxs-lookup"><span data-stu-id="8f1cd-104">The **GetResponseHeader** method retrieves the HTTP response headers.</span></span>

## <a name="syntax"></a><span data-ttu-id="8f1cd-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8f1cd-105">Syntax</span></span>


```C++
HRESULT GetResponseHeader(
  [in]          BSTR Header,
  [out, retval] BSTR *Value
);
```



## <a name="parameters"></a><span data-ttu-id="8f1cd-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="8f1cd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8f1cd-107">*Заголовок* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8f1cd-107">*Header* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8f1cd-108">Указывает имя заголовка без учета регистра.</span><span class="sxs-lookup"><span data-stu-id="8f1cd-108">Specifies the case-insensitive header name.</span></span>

</dd> <dt>

<span data-ttu-id="8f1cd-109">*Значение* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="8f1cd-109">*Value* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="8f1cd-110">Получает сведения о результирующем заголовке.</span><span class="sxs-lookup"><span data-stu-id="8f1cd-110">Receives the resulting header information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8f1cd-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8f1cd-111">Return value</span></span>

<span data-ttu-id="8f1cd-112">В случае успешного выполнения возвращается значение **S \_** , а в противном случае — значение ошибки.</span><span class="sxs-lookup"><span data-stu-id="8f1cd-112">The return value is **S\_OK** on success or an error value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="8f1cd-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8f1cd-113">Remarks</span></span>

<span data-ttu-id="8f1cd-114">Этот метод возвращает значение заголовка ответа с именем в *заголовке*.</span><span class="sxs-lookup"><span data-stu-id="8f1cd-114">This method returns the value of the response header named in *Header*.</span></span> <span data-ttu-id="8f1cd-115">Имейте в виду, что клиенты автоматизации, такие как скрипт, получают данные заголовка в качестве возвращаемого значения вызова функции, а не через параметр функции.</span><span class="sxs-lookup"><span data-stu-id="8f1cd-115">Be aware that automation clients, such as script, get the header data as the return value of the function call, not through a function parameter.</span></span> <span data-ttu-id="8f1cd-116">Вызывайте этот метод только после вызова метода [**Send**](iwinhttprequest-send.md) .</span><span class="sxs-lookup"><span data-stu-id="8f1cd-116">Invoke this method only after the [**Send**](iwinhttprequest-send.md) method has been called.</span></span>

> [!Note]  
> <span data-ttu-id="8f1cd-117">Для Windows XP и Windows 2000 см. раздел [требования к времени выполнения](winhttp-start-page.md) на начальной странице WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="8f1cd-117">For Windows XP and Windows 2000, see the [Run-Time Requirements](winhttp-start-page.md) section of the WinHTTP Start Page.</span></span>

 

## <a name="examples"></a><span data-ttu-id="8f1cd-118">Примеры</span><span class="sxs-lookup"><span data-stu-id="8f1cd-118">Examples</span></span>

<span data-ttu-id="8f1cd-119">В следующем примере показано, как открыть HTTP-соединение, отправить HTTP-запрос и получить заголовок даты из ответа.</span><span class="sxs-lookup"><span data-stu-id="8f1cd-119">The following example shows how to open an HTTP connection, send an HTTP request, and get the date header from the response.</span></span> <span data-ttu-id="8f1cd-120">Этот пример необходимо запустить из командной строки.</span><span class="sxs-lookup"><span data-stu-id="8f1cd-120">This example must be run from a command prompt.</span></span>


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

    // Initialize COM
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

    hr = CLSIDFromProgID(L"WinHttp.WinHttpRequest.5.1",
                         &clsid);

    if (SUCCEEDED(hr))
    {
        hr = CoCreateInstance(clsid,
                              NULL,
                              CLSCTX_INPROC_SERVER,
                              IID_IWinHttpRequest,
                              (void **)&pIWinHttpRequest);
    }
    if (SUCCEEDED(hr))
    {
        // Open WinHttpRequest.
        BSTR bstrMethod  = SysAllocString(L"GET");
        BSTR bstrUrl = SysAllocString(L"https://microsoft.com");
        hr = pIWinHttpRequest->Open(bstrMethod,
                                    bstrUrl,
                                    varFalse);
        SysFreeString(bstrMethod);
        SysFreeString(bstrUrl);
    }
    if (SUCCEEDED(hr))
    {
        // Send Request.
        hr = pIWinHttpRequest->Send(varEmpty);
    }
    if (SUCCEEDED(hr))
    {
        // Get Response text.
        BSTR bstrName = SysAllocString(L"Date");
        hr = pIWinHttpRequest->GetResponseHeader(bstrName,
                                             &bstrResponse);
    }
    if (SUCCEEDED(hr))
    {
        // Print response to console.
        wprintf(L"%.256s",bstrResponse);
    }

    // Release memory.
    if (pIWinHttpRequest)
        pIWinHttpRequest->Release();
    if (bstrResponse)
        SysFreeString(bstrResponse);

    CoUninitialize();
    return 0;
}

```



<span data-ttu-id="8f1cd-121">В следующем примере сценария показано, как открыть HTTP-соединение, отправить HTTP-запрос и получить заголовок даты из ответа.</span><span class="sxs-lookup"><span data-stu-id="8f1cd-121">The following scripting example shows how to open an HTTP connection, send an HTTP request, and get the date header from the response.</span></span>


```JScript
// Instantiate a WinHttpRequest object.
var WinHttpReq = new ActiveXObject("WinHttp.WinHttpRequest.5.1");

// Initialize an HTTP request.  
WinHttpReq.Open("GET", 
                "https://www.microsoft.com", 
                 false);

// Send the HTTP request.
WinHttpReq.Send(); 

// Display the date header.
WScript.Echo( WinHttpReq.GetResponseHeader("Date"));
```



## <a name="requirements"></a><span data-ttu-id="8f1cd-122">Требования</span><span class="sxs-lookup"><span data-stu-id="8f1cd-122">Requirements</span></span>



| <span data-ttu-id="8f1cd-123">Требование</span><span class="sxs-lookup"><span data-stu-id="8f1cd-123">Requirement</span></span> | <span data-ttu-id="8f1cd-124">Значение</span><span class="sxs-lookup"><span data-stu-id="8f1cd-124">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="8f1cd-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8f1cd-125">Minimum supported client</span></span><br/> | <span data-ttu-id="8f1cd-126">Windows XP, Windows 2000 Professional с пакетом обновления 3 (SP3), \[ только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="8f1cd-126">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="8f1cd-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8f1cd-127">Minimum supported server</span></span><br/> | <span data-ttu-id="8f1cd-128">Windows Server 2003, Windows 2000 Server с пакетом обновления 3 (SP3), \[ только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="8f1cd-128">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>         |
| <span data-ttu-id="8f1cd-129">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="8f1cd-129">Redistributable</span></span><br/>          | <span data-ttu-id="8f1cd-130">WinHTTP 5,0 и Internet Explorer 5,01 или более поздней версии в Windows XP и Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="8f1cd-130">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span><br/> |
| <span data-ttu-id="8f1cd-131">IDL</span><span class="sxs-lookup"><span data-stu-id="8f1cd-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="8f1cd-132"><dt>HttpRequest. idl</dt></span><span class="sxs-lookup"><span data-stu-id="8f1cd-132"><dt>HttpRequest.idl</dt></span></span> </dl> |
| <span data-ttu-id="8f1cd-133">Библиотека</span><span class="sxs-lookup"><span data-stu-id="8f1cd-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="8f1cd-134"><dt>WinHTTP. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8f1cd-134"><dt>Winhttp.lib</dt></span></span> </dl>     |
| <span data-ttu-id="8f1cd-135">DLL</span><span class="sxs-lookup"><span data-stu-id="8f1cd-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8f1cd-136"><dt>Winhttp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8f1cd-136"><dt>Winhttp.dll</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="8f1cd-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8f1cd-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f1cd-138">**ивинхттпрекуест**</span><span class="sxs-lookup"><span data-stu-id="8f1cd-138">**IWinHttpRequest**</span></span>](iwinhttprequest-interface.md)
</dt> <dt>

[<span data-ttu-id="8f1cd-139">**WinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="8f1cd-139">**WinHttpRequest**</span></span>](winhttprequest.md)
</dt> <dt>

[<span data-ttu-id="8f1cd-140">**жеталлреспонсехеадерс**</span><span class="sxs-lookup"><span data-stu-id="8f1cd-140">**GetAllResponseHeaders**</span></span>](iwinhttprequest-getallresponseheaders.md)
</dt> <dt>

[<span data-ttu-id="8f1cd-141">Версии WinHTTP</span><span class="sxs-lookup"><span data-stu-id="8f1cd-141">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

 




