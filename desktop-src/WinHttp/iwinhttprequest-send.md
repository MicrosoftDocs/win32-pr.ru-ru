---
description: Метод Send отправляет HTTP-запрос серверу HTTP.
ms.assetid: 4f30d6b7-d1c3-43f1-9829-260b7c84518f
title: 'Метод Ивинхттпрекуест:: send'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWinHttpRequest.Send
- WinHttpRequest.Send
api_type:
- COM
api_location:
- Winhttp.dll
ms.openlocfilehash: 0040ed6c09814a2b2112a91173d84430b8130a30
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103816129"
---
# <a name="iwinhttprequestsend-method"></a><span data-ttu-id="052f3-103">Метод Ивинхттпрекуест:: send</span><span class="sxs-lookup"><span data-stu-id="052f3-103">IWinHttpRequest::Send method</span></span>

<span data-ttu-id="052f3-104">Метод **Send** отправляет HTTP-запрос серверу HTTP.</span><span class="sxs-lookup"><span data-stu-id="052f3-104">The **Send** method sends an HTTP request to an HTTP server.</span></span>

## <a name="syntax"></a><span data-ttu-id="052f3-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="052f3-105">Syntax</span></span>


```C++
HRESULT Send(
  [in, optional] VARIANT Body
);
```



## <a name="parameters"></a><span data-ttu-id="052f3-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="052f3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="052f3-107">*Текст сообщения* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="052f3-107">*Body* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="052f3-108">Данные, отправляемые на сервер.</span><span class="sxs-lookup"><span data-stu-id="052f3-108">Data to be sent to the server.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="052f3-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="052f3-109">Return value</span></span>

<span data-ttu-id="052f3-110">В случае успешного выполнения возвращается значение **S \_** , а в противном случае — значение ошибки.</span><span class="sxs-lookup"><span data-stu-id="052f3-110">The return value is **S\_OK** on success or an error value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="052f3-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="052f3-111">Remarks</span></span>

<span data-ttu-id="052f3-112">Отправляемый запрос был определен в предыдущем вызове метода [**Open**](iwinhttprequest-open.md) .</span><span class="sxs-lookup"><span data-stu-id="052f3-112">The request to be sent was defined in a prior call to the [**Open**](iwinhttprequest-open.md) method.</span></span> <span data-ttu-id="052f3-113">Вызывающее приложение может предоставлять данные, отправляемые на сервер с помощью параметра *Body* .</span><span class="sxs-lookup"><span data-stu-id="052f3-113">The calling application can provide data to be sent to the server through the *Body* parameter.</span></span> <span data-ttu-id="052f3-114">Если [*HTTP-команда*](glossary.md) [**открытого**](iwinhttprequest-open.md) объекта имеет значение Get, этот метод отправляет запрос без *тела*, даже если он предоставляется вызывающим приложением.</span><span class="sxs-lookup"><span data-stu-id="052f3-114">If the [*HTTP verb*](glossary.md) of the object's [**Open**](iwinhttprequest-open.md) is "GET", this method sends the request without *Body*, even if it is provided by the calling application.</span></span>

> [!Note]  
> <span data-ttu-id="052f3-115">Для Windows XP и Windows 2000 см. раздел [требования к времени выполнения](winhttp-start-page.md) на начальной странице WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="052f3-115">For Windows XP and Windows 2000, see the [Run-Time Requirements](winhttp-start-page.md) section of the WinHttp start page.</span></span>

 

## <a name="examples"></a><span data-ttu-id="052f3-116">Примеры</span><span class="sxs-lookup"><span data-stu-id="052f3-116">Examples</span></span>

<span data-ttu-id="052f3-117">В следующем примере показано, как открыть HTTP-соединение, отправить HTTP-запрос и прочитать текст ответа.</span><span class="sxs-lookup"><span data-stu-id="052f3-117">The following example shows how to open an HTTP connection, send an HTTP request, and read the response text.</span></span>


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
    // variable for return value
    HRESULT    hr;

    // initialize COM
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
        hr = pIWinHttpRequest->get_ResponseText(&bstrResponse);
    }

    // Print response to console.
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



<span data-ttu-id="052f3-118">В следующем примере скрипта показано, как открыть HTTP-соединение, отправить HTTP-запрос и прочитать текст ответа.</span><span class="sxs-lookup"><span data-stu-id="052f3-118">The following scripting example shows how to open an HTTP connection, send an HTTP request, and read the response text.</span></span>


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



<span data-ttu-id="052f3-119">В следующем примере сценария показано, как отправлять данные на HTTP-сервер.</span><span class="sxs-lookup"><span data-stu-id="052f3-119">The following scripting example shows how to post data to an HTTP server.</span></span>


```JScript
// Instantiate a WinHttpRequest object.
var WinHttpReq = new ActiveXObject("WinHttp.WinHttpRequest.5.1");

// Initialize an HTTP request.  
WinHttpReq.Open("PUT", "https://postserver/newdoc.htm", false);

// Post data to the HTTP server.
WinHttpReq.Send("Post data");
```



## <a name="requirements"></a><span data-ttu-id="052f3-120">Требования</span><span class="sxs-lookup"><span data-stu-id="052f3-120">Requirements</span></span>



| <span data-ttu-id="052f3-121">Требование</span><span class="sxs-lookup"><span data-stu-id="052f3-121">Requirement</span></span> | <span data-ttu-id="052f3-122">Значение</span><span class="sxs-lookup"><span data-stu-id="052f3-122">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="052f3-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="052f3-123">Minimum supported client</span></span><br/> | <span data-ttu-id="052f3-124">Windows XP, Windows 2000 Professional с пакетом обновления 3 (SP3), \[ только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="052f3-124">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="052f3-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="052f3-125">Minimum supported server</span></span><br/> | <span data-ttu-id="052f3-126">Windows Server 2003, Windows 2000 Server с пакетом обновления 3 (SP3), \[ только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="052f3-126">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>         |
| <span data-ttu-id="052f3-127">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="052f3-127">Redistributable</span></span><br/>          | <span data-ttu-id="052f3-128">WinHTTP 5,0 и Internet Explorer 5,01 или более поздней версии в Windows XP и Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="052f3-128">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span><br/> |
| <span data-ttu-id="052f3-129">IDL</span><span class="sxs-lookup"><span data-stu-id="052f3-129">IDL</span></span><br/>                      | <dl> <span data-ttu-id="052f3-130"><dt>HttpRequest. idl</dt></span><span class="sxs-lookup"><span data-stu-id="052f3-130"><dt>HttpRequest.idl</dt></span></span> </dl> |
| <span data-ttu-id="052f3-131">Библиотека</span><span class="sxs-lookup"><span data-stu-id="052f3-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="052f3-132"><dt>WinHTTP. lib</dt></span><span class="sxs-lookup"><span data-stu-id="052f3-132"><dt>Winhttp.lib</dt></span></span> </dl>     |
| <span data-ttu-id="052f3-133">DLL</span><span class="sxs-lookup"><span data-stu-id="052f3-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="052f3-134"><dt>Winhttp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="052f3-134"><dt>Winhttp.dll</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="052f3-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="052f3-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="052f3-136">**ивинхттпрекуест**</span><span class="sxs-lookup"><span data-stu-id="052f3-136">**IWinHttpRequest**</span></span>](iwinhttprequest-interface.md)
</dt> <dt>

[<span data-ttu-id="052f3-137">**WinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="052f3-137">**WinHttpRequest**</span></span>](winhttprequest.md)
</dt> <dt>

[<span data-ttu-id="052f3-138">Версии WinHTTP</span><span class="sxs-lookup"><span data-stu-id="052f3-138">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

 




