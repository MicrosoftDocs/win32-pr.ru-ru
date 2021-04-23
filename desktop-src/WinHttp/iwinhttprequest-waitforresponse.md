---
description: Метод Ваитфорреспонсе ожидает завершения асинхронного метода Send с необязательным значением времени ожидания в секундах.
ms.assetid: 33265710-ecdc-4eae-8822-161dffbd03fc
title: 'Метод Ивинхттпрекуест:: Ваитфорреспонсе'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWinHttpRequest.WaitForResponse
- WinHttpRequest.WaitForResponse
api_type:
- COM
api_location:
- Winhttp.dll
ms.openlocfilehash: fe9e3508273a3ee52d72ede65fd6575d72decb8f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674200"
---
# <a name="iwinhttprequestwaitforresponse-method"></a><span data-ttu-id="9a477-103">Метод Ивинхттпрекуест:: Ваитфорреспонсе</span><span class="sxs-lookup"><span data-stu-id="9a477-103">IWinHttpRequest::WaitForResponse method</span></span>

<span data-ttu-id="9a477-104">Метод **ваитфорреспонсе** ожидает завершения асинхронного метода [**Send**](iwinhttprequest-send.md) с необязательным значением времени ожидания в секундах.</span><span class="sxs-lookup"><span data-stu-id="9a477-104">The **WaitForResponse** method waits for an asynchronous [**Send**](iwinhttprequest-send.md) method to complete, with optional time-out value, in seconds.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a477-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9a477-105">Syntax</span></span>


```C++
HRESULT WaitForResponse(
  [in, optional] VARIANT      Timeout,
  [out, retval]  VARIANT_BOOL *Succeeded
);
```



## <a name="parameters"></a><span data-ttu-id="9a477-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="9a477-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9a477-107">*Время ожидания* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="9a477-107">*Timeout* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9a477-108">Значение времени ожидания в секундах.</span><span class="sxs-lookup"><span data-stu-id="9a477-108">Time-out value, in seconds.</span></span> <span data-ttu-id="9a477-109">Время ожидания по умолчанию — Infinite.</span><span class="sxs-lookup"><span data-stu-id="9a477-109">Default time-out is infinite.</span></span> <span data-ttu-id="9a477-110">Чтобы явно задать бесконечное время ожидания, используйте значение-1.</span><span class="sxs-lookup"><span data-stu-id="9a477-110">To explicitly set time-out to infinite, use the value -1.</span></span>

</dd> <dt>

<span data-ttu-id="9a477-111">*Прошло* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="9a477-111">*Succeeded* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="9a477-112">Получает одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="9a477-112">Receives one of the following values.</span></span>



| <span data-ttu-id="9a477-113">Значение</span><span class="sxs-lookup"><span data-stu-id="9a477-113">Value</span></span>                                                                                                                                                         | <span data-ttu-id="9a477-114">Значение</span><span class="sxs-lookup"><span data-stu-id="9a477-114">Meaning</span></span>                                                |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <span id="VARIANT_TRUE"></span><span id="variant_true"></span><dl> <span data-ttu-id="9a477-115"><dt>**ВАРИАНТ \_ true**</dt></span><span class="sxs-lookup"><span data-stu-id="9a477-115"><dt>**VARIANT\_TRUE**</dt></span></span> </dl>    | <span data-ttu-id="9a477-116">Получен ответ.</span><span class="sxs-lookup"><span data-stu-id="9a477-116">A response has been received.</span></span><br/>               |
| <span id="VARIANT_FALSE"></span><span id="variant_false"></span><dl> <span data-ttu-id="9a477-117"><dt>**ВАРИАНТ \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="9a477-117"><dt>**VARIANT\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="9a477-118">Был превышен указанный период ожидания.</span><span class="sxs-lookup"><span data-stu-id="9a477-118">The specified time-out period was exceeded.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9a477-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9a477-119">Return value</span></span>

<span data-ttu-id="9a477-120">В случае успешного выполнения возвращается значение **S \_** , а в противном случае — значение ошибки.</span><span class="sxs-lookup"><span data-stu-id="9a477-120">The return value is **S\_OK** on success or an error value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="9a477-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9a477-121">Remarks</span></span>

<span data-ttu-id="9a477-122">Этот метод приостанавливает выполнение при ожидании ответа на асинхронный запрос.</span><span class="sxs-lookup"><span data-stu-id="9a477-122">This method suspends execution while waiting for a response to an asynchronous request.</span></span> <span data-ttu-id="9a477-123">Этот метод должен вызываться после [**отправки**](iwinhttprequest-send.md).</span><span class="sxs-lookup"><span data-stu-id="9a477-123">This method should be called after a [**Send**](iwinhttprequest-send.md).</span></span> <span data-ttu-id="9a477-124">Вызывающие приложения могут задавать необязательное значение *времени ожидания* в секундах.</span><span class="sxs-lookup"><span data-stu-id="9a477-124">Calling applications can specify an optional *Timeout* value, in seconds.</span></span> <span data-ttu-id="9a477-125">Если этот метод истечет из-за истечения времени ожидания, запрос не прерывается.</span><span class="sxs-lookup"><span data-stu-id="9a477-125">If this method times out, the request is not aborted.</span></span> <span data-ttu-id="9a477-126">Таким образом, вызывающее приложение может продолжить ожидание запроса (при необходимости) при последующем вызове этого метода.</span><span class="sxs-lookup"><span data-stu-id="9a477-126">This way, the calling application can continue to wait for the request, if desired, in a subsequent call to this method.</span></span>

<span data-ttu-id="9a477-127">Вызов этого свойства после того, как синхронный метод [**Send**](iwinhttprequest-send.md) немедленно возвращает результат и не оказывает никакого влияния.</span><span class="sxs-lookup"><span data-stu-id="9a477-127">Calling this property after a synchronous [**Send**](iwinhttprequest-send.md) method returns immediately and has no effect.</span></span>

> [!Note]  
> <span data-ttu-id="9a477-128">Для Windows XP и Windows 2000 см. раздел [требования к времени выполнения](winhttp-start-page.md) на начальной странице WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="9a477-128">For Windows XP and Windows 2000, see the [Run-Time Requirements](winhttp-start-page.md) section of the WinHTTP Start Page.</span></span>

 

## <a name="examples"></a><span data-ttu-id="9a477-129">Примеры</span><span class="sxs-lookup"><span data-stu-id="9a477-129">Examples</span></span>

<span data-ttu-id="9a477-130">В следующем примере показано, как открыть асинхронное HTTP-соединение, отправить HTTP-запрос, дождаться ответа и прочитать текст ответа.</span><span class="sxs-lookup"><span data-stu-id="9a477-130">The following example shows how to open an asynchronous HTTP connection, send an HTTP request, wait for the response and read the response text.</span></span>


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
    VARIANT         varTrue;
    VARIANT         varEmpty;

    CLSID           clsid;

    VariantInit(&varTrue);
    V_VT(&varTrue)   = VT_BOOL;
    V_BOOL(&varTrue) = VARIANT_TRUE;

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
        hr = pIWinHttpRequest->Open(bstrMethod, bstrUrl, varTrue);
        SysFreeString(bstrMethod);
        SysFreeString(bstrUrl);
    }
    if (SUCCEEDED(hr))
    {    // Send Request.
        hr = pIWinHttpRequest->Send(varEmpty);
    }
    if (SUCCEEDED(hr))
    {    // Wait for response.
        VARIANT_BOOL varResult;
        hr = pIWinHttpRequest->WaitForResponse(varEmpty, &varResult);
    }
    if (SUCCEEDED(hr))
    {    // Get Response text.
        hr = pIWinHttpRequest->get_ResponseText(&bstrResponse);
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



<span data-ttu-id="9a477-131">В следующем примере скрипта показано, как открыть асинхронное HTTP-соединение, отправить HTTP-запрос, подождать ответа и прочитать текст ответа.</span><span class="sxs-lookup"><span data-stu-id="9a477-131">The following scripting example shows how to open an asynchronous HTTP connection, send an HTTP request, wait for a response, and read the response text.</span></span>


```JScript
// Instantiate a WinHttpRequest object.
var WinHttpReq = new ActiveXObject("WinHttp.WinHttpRequest.5.1");

// Initialize an HTTP request.  
WinHttpReq.Open("GET", "https://www.microsoft.com", true);

// Send the HTTP request.
WinHttpReq.Send(); 

// Wait for the response.
WinHttpReq.WaitForResponse();

// Display the response text.
WScript.Echo( WinHttpReq.ResponseText);
```



## <a name="requirements"></a><span data-ttu-id="9a477-132">Требования</span><span class="sxs-lookup"><span data-stu-id="9a477-132">Requirements</span></span>



| <span data-ttu-id="9a477-133">Требование</span><span class="sxs-lookup"><span data-stu-id="9a477-133">Requirement</span></span> | <span data-ttu-id="9a477-134">Значение</span><span class="sxs-lookup"><span data-stu-id="9a477-134">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="9a477-135">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9a477-135">Minimum supported client</span></span><br/> | <span data-ttu-id="9a477-136">Windows XP, Windows 2000 Professional с пакетом обновления 3 (SP3), \[ только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="9a477-136">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="9a477-137">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9a477-137">Minimum supported server</span></span><br/> | <span data-ttu-id="9a477-138">Windows Server 2003, Windows 2000 Server с пакетом обновления 3 (SP3), \[ только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="9a477-138">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>         |
| <span data-ttu-id="9a477-139">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="9a477-139">Redistributable</span></span><br/>          | <span data-ttu-id="9a477-140">WinHTTP 5,0 и Internet Explorer 5,01 или более поздней версии в Windows XP и Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="9a477-140">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span><br/> |
| <span data-ttu-id="9a477-141">IDL</span><span class="sxs-lookup"><span data-stu-id="9a477-141">IDL</span></span><br/>                      | <dl> <span data-ttu-id="9a477-142"><dt>HttpRequest. idl</dt></span><span class="sxs-lookup"><span data-stu-id="9a477-142"><dt>HttpRequest.idl</dt></span></span> </dl> |
| <span data-ttu-id="9a477-143">Библиотека</span><span class="sxs-lookup"><span data-stu-id="9a477-143">Library</span></span><br/>                  | <dl> <span data-ttu-id="9a477-144"><dt>WinHTTP. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9a477-144"><dt>Winhttp.lib</dt></span></span> </dl>     |
| <span data-ttu-id="9a477-145">DLL</span><span class="sxs-lookup"><span data-stu-id="9a477-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9a477-146"><dt>Winhttp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9a477-146"><dt>Winhttp.dll</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="9a477-147">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9a477-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a477-148">**ивинхттпрекуест**</span><span class="sxs-lookup"><span data-stu-id="9a477-148">**IWinHttpRequest**</span></span>](iwinhttprequest-interface.md)
</dt> <dt>

[<span data-ttu-id="9a477-149">**WinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="9a477-149">**WinHttpRequest**</span></span>](winhttprequest.md)
</dt> <dt>

[<span data-ttu-id="9a477-150">**Открыт**</span><span class="sxs-lookup"><span data-stu-id="9a477-150">**Open**</span></span>](iwinhttprequest-open.md)
</dt> <dt>

[<span data-ttu-id="9a477-151">Версии WinHTTP</span><span class="sxs-lookup"><span data-stu-id="9a477-151">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

 




