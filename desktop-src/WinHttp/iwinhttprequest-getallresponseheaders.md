---
description: Извлекает все заголовки ответа HTTP.
ms.assetid: 68b13d4c-5afd-486d-8b78-a7eef0f59a24
title: 'Метод Ивинхттпрекуест:: Жеталлреспонсехеадерс'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWinHttpRequest.GetAllResponseHeaders
- WinHttpRequest.GetAllResponseHeaders
api_type:
- COM
api_location:
- Winhttp.dll
ms.openlocfilehash: 74c113216cf41e2f9816176dd28ba5e84208c635
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105651088"
---
# <a name="iwinhttprequestgetallresponseheaders-method"></a><span data-ttu-id="2ea13-103">Метод Ивинхттпрекуест:: Жеталлреспонсехеадерс</span><span class="sxs-lookup"><span data-stu-id="2ea13-103">IWinHttpRequest::GetAllResponseHeaders method</span></span>

<span data-ttu-id="2ea13-104">Метод **жеталлреспонсехеадерс** извлекает все заголовки ответа HTTP.</span><span class="sxs-lookup"><span data-stu-id="2ea13-104">The **GetAllResponseHeaders** method retrieves all HTTP response headers.</span></span>

## <a name="syntax"></a><span data-ttu-id="2ea13-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2ea13-105">Syntax</span></span>


```C++
HRESULT GetAllResponseHeaders(
  [out, retval] BSTR *Headers
);
```



## <a name="parameters"></a><span data-ttu-id="2ea13-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="2ea13-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2ea13-107">*Заголовки* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="2ea13-107">*Headers* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="2ea13-108">Получает сведения о результирующем заголовке.</span><span class="sxs-lookup"><span data-stu-id="2ea13-108">Receives the resulting header information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2ea13-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2ea13-109">Return value</span></span>

<span data-ttu-id="2ea13-110">В случае успешного выполнения возвращается значение **S \_** , а в противном случае — значение ошибки.</span><span class="sxs-lookup"><span data-stu-id="2ea13-110">The return value is **S\_OK** on success or an error value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="2ea13-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2ea13-111">Remarks</span></span>

<span data-ttu-id="2ea13-112">Этот метод возвращает все заголовки, содержащиеся в последнем ответе сервера.</span><span class="sxs-lookup"><span data-stu-id="2ea13-112">This method returns all of the headers contained in the most recent server response.</span></span> <span data-ttu-id="2ea13-113">Отдельные заголовки разделяются сочетанием символов возврата каретки и перевода строки (ASCII 13 и 10).</span><span class="sxs-lookup"><span data-stu-id="2ea13-113">The individual headers are delimited by a carriage return and line feed combination (ASCII 13 and 10).</span></span> <span data-ttu-id="2ea13-114">За последней записью следуют два разделителя (13, 10, 13, 10).</span><span class="sxs-lookup"><span data-stu-id="2ea13-114">The last entry is followed by two delimiters (13, 10, 13, 10).</span></span> <span data-ttu-id="2ea13-115">Вызывайте этот метод только после вызова метода [**Send**](iwinhttprequest-send.md) .</span><span class="sxs-lookup"><span data-stu-id="2ea13-115">Invoke this method only after the [**Send**](iwinhttprequest-send.md) method has been called.</span></span>

> [!Note]  
> <span data-ttu-id="2ea13-116">Для Windows XP и Windows 2000 см. раздел [требования к времени выполнения](winhttp-start-page.md) на начальной странице WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="2ea13-116">For Windows XP and Windows 2000, see the [Run-Time Requirements](winhttp-start-page.md) section of the WinHTTP Start Page.</span></span>

 

## <a name="examples"></a><span data-ttu-id="2ea13-117">Примеры</span><span class="sxs-lookup"><span data-stu-id="2ea13-117">Examples</span></span>

<span data-ttu-id="2ea13-118">В следующем примере показано, как открыть HTTP-соединение, отправить HTTP-запрос и получить все заголовки из ответа.</span><span class="sxs-lookup"><span data-stu-id="2ea13-118">The following example shows how to open an HTTP connection, send an HTTP request, and get all of the headers from the response.</span></span> <span data-ttu-id="2ea13-119">Этот пример следует запускать из командной строки.</span><span class="sxs-lookup"><span data-stu-id="2ea13-119">This example should be run from a command prompt.</span></span>


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

int main(int argc, char* argv[])
{
    UNREFERENCED_PARAMETER(argc);
    UNREFERENCED_PARAMETER(argv);

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
    {    // Get Response text.
        hr = pIWinHttpRequest->GetAllResponseHeaders(&bstrResponse);
    }
    if (SUCCEEDED(hr))
    {    // Print the response to a console.
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



<span data-ttu-id="2ea13-120">В следующем примере сценария показано, как открыть HTTP-соединение, отправить HTTP-запрос и получить все заголовки из ответа.</span><span class="sxs-lookup"><span data-stu-id="2ea13-120">The following scripting example shows how to open an HTTP connection, send an HTTP request, and get all of the headers from the response.</span></span>


```JScript
// Instantiate a WinHttpRequest object.
var WinHttpReq = new ActiveXObject("WinHttp.WinHttpRequest.5.1");

// Initialize an HTTP request.  
WinHttpReq.Open("GET", "https://www.microsoft.com", false);

// Send the HTTP request.
WinHttpReq.Send(); 

// Get all response headers.
WScript.Echo( WinHttpReq.GetAllResponseHeaders());
```



## <a name="requirements"></a><span data-ttu-id="2ea13-121">Требования</span><span class="sxs-lookup"><span data-stu-id="2ea13-121">Requirements</span></span>



| <span data-ttu-id="2ea13-122">Требование</span><span class="sxs-lookup"><span data-stu-id="2ea13-122">Requirement</span></span> | <span data-ttu-id="2ea13-123">Значение</span><span class="sxs-lookup"><span data-stu-id="2ea13-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="2ea13-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2ea13-124">Minimum supported client</span></span><br/> | <span data-ttu-id="2ea13-125">Windows XP, Windows 2000 Professional с пакетом обновления 3 (SP3), \[ только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="2ea13-125">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="2ea13-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2ea13-126">Minimum supported server</span></span><br/> | <span data-ttu-id="2ea13-127">Windows Server 2003, Windows 2000 Server с пакетом обновления 3 (SP3), \[ только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="2ea13-127">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>         |
| <span data-ttu-id="2ea13-128">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="2ea13-128">Redistributable</span></span><br/>          | <span data-ttu-id="2ea13-129">WinHTTP 5,0 и Internet Explorer 5,01 или более поздней версии в Windows XP и Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="2ea13-129">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span><br/> |
| <span data-ttu-id="2ea13-130">IDL</span><span class="sxs-lookup"><span data-stu-id="2ea13-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="2ea13-131"><dt>HttpRequest. idl</dt></span><span class="sxs-lookup"><span data-stu-id="2ea13-131"><dt>HttpRequest.idl</dt></span></span> </dl> |
| <span data-ttu-id="2ea13-132">Библиотека</span><span class="sxs-lookup"><span data-stu-id="2ea13-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="2ea13-133"><dt>WinHTTP. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2ea13-133"><dt>Winhttp.lib</dt></span></span> </dl>     |
| <span data-ttu-id="2ea13-134">DLL</span><span class="sxs-lookup"><span data-stu-id="2ea13-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2ea13-135"><dt>Winhttp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2ea13-135"><dt>Winhttp.dll</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="2ea13-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2ea13-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ea13-137">**ивинхттпрекуест**</span><span class="sxs-lookup"><span data-stu-id="2ea13-137">**IWinHttpRequest**</span></span>](iwinhttprequest-interface.md)
</dt> <dt>

[<span data-ttu-id="2ea13-138">**WinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="2ea13-138">**WinHttpRequest**</span></span>](winhttprequest.md)
</dt> <dt>

[<span data-ttu-id="2ea13-139">**жетреспонсехеадер**</span><span class="sxs-lookup"><span data-stu-id="2ea13-139">**GetResponseHeader**</span></span>](iwinhttprequest-getresponseheader.md)
</dt> <dt>

[<span data-ttu-id="2ea13-140">Версии WinHTTP</span><span class="sxs-lookup"><span data-stu-id="2ea13-140">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

 




