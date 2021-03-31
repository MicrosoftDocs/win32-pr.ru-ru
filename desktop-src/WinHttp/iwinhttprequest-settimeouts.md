---
description: Метод Сеттимеаутс задает отдельные компоненты времени ожидания операции отправки и получения в миллисекундах.
ms.assetid: c2b6c432-5f3b-4361-8026-1b843c6697ae
title: 'Метод Ивинхттпрекуест:: Сеттимеаутс'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWinHttpRequest.SetTimeouts
- WinHttpRequest.SetTimeouts
api_type:
- COM
api_location:
- Winhttp.dll
ms.openlocfilehash: 3f2f81585fdf444b6b5ab1795f183897687732ed
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/10/2021
ms.locfileid: "104273679"
---
# <a name="iwinhttprequestsettimeouts-method"></a><span data-ttu-id="dd2bc-103">Метод Ивинхттпрекуест:: Сеттимеаутс</span><span class="sxs-lookup"><span data-stu-id="dd2bc-103">IWinHttpRequest::SetTimeouts method</span></span>

<span data-ttu-id="dd2bc-104">Метод **сеттимеаутс** задает отдельные компоненты времени ожидания операции отправки и получения в миллисекундах.</span><span class="sxs-lookup"><span data-stu-id="dd2bc-104">The **SetTimeouts** method specifies the individual time-out components of a send/receive operation, in milliseconds.</span></span>

## <a name="syntax"></a><span data-ttu-id="dd2bc-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dd2bc-105">Syntax</span></span>


```C++
HRESULT SetTimeouts(
  [in] long ResolveTimeout,
  [in] long ConnectTimeout,
  [in] long SendTimeout,
  [in] long ReceiveTimeout
);
```



## <a name="parameters"></a><span data-ttu-id="dd2bc-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="dd2bc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dd2bc-107">*Ресолветимеаут* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="dd2bc-107">*ResolveTimeout* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dd2bc-108">Значение времени ожидания, применяемое при разрешении имени узла (например, `www.microsoft.com` ) в IP-адрес (например, 192.168.131.199), в миллисекундах.</span><span class="sxs-lookup"><span data-stu-id="dd2bc-108">Time-out value applied when resolving a host name (such as `www.microsoft.com`) to an IP address (such as 192.168.131.199), in milliseconds.</span></span> <span data-ttu-id="dd2bc-109">Значение по умолчанию равно нулю, что означает отсутствие времени ожидания (бесконечно).</span><span class="sxs-lookup"><span data-stu-id="dd2bc-109">The default value is zero, meaning no time-out (infinite).</span></span> <span data-ttu-id="dd2bc-110">Если время ожидания DNS задано с \_ помощью \_ времени ожидания разрешения имен, то для каждого запроса взимается дополнительная нагрузка по одному потоку.</span><span class="sxs-lookup"><span data-stu-id="dd2bc-110">If DNS timeout is specified using NAME\_RESOLUTION\_TIMEOUT, there is an overhead of one thread per request.</span></span>

</dd> <dt>

<span data-ttu-id="dd2bc-111">*ConnectTimeout* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="dd2bc-111">*ConnectTimeout* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dd2bc-112">Значение времени ожидания, применяемое при установлении сокета связи с целевым сервером, в миллисекундах.</span><span class="sxs-lookup"><span data-stu-id="dd2bc-112">Time-out value applied when establishing a communication socket with the target server, in milliseconds.</span></span> <span data-ttu-id="dd2bc-113">По умолчанию установлено значение 60000 (60 секунд).</span><span class="sxs-lookup"><span data-stu-id="dd2bc-113">The default value is 60,000 (60 seconds).</span></span>

</dd> <dt>

<span data-ttu-id="dd2bc-114">*SendTimeout* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="dd2bc-114">*SendTimeout* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dd2bc-115">Значение времени ожидания, применяемое при отправке отдельного пакета данных запроса на сокете связи на целевой сервер в миллисекундах.</span><span class="sxs-lookup"><span data-stu-id="dd2bc-115">Time-out value applied when sending an individual packet of request data on the communication socket to the target server, in milliseconds.</span></span> <span data-ttu-id="dd2bc-116">Большой запрос, отправленный на HTTP-сервер, обычно разбивается на несколько пакетов. время ожидания отправки применяется для отправки каждого пакета по отдельности.</span><span class="sxs-lookup"><span data-stu-id="dd2bc-116">A large request sent to an HTTP server are normally be broken up into multiple packets; the send time-out applies to sending each packet individually.</span></span> <span data-ttu-id="dd2bc-117">Значение по умолчанию — 30 000 (30 секунд).</span><span class="sxs-lookup"><span data-stu-id="dd2bc-117">The default value is 30,000 (30 seconds).</span></span>

</dd> <dt>

<span data-ttu-id="dd2bc-118">*ReceiveTimeout равен* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="dd2bc-118">*ReceiveTimeout* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dd2bc-119">Значение времени ожидания, применяемое при получении пакета данных ответа от целевого сервера, в миллисекундах.</span><span class="sxs-lookup"><span data-stu-id="dd2bc-119">Time-out value applied when receiving a packet of response data from the target server, in milliseconds.</span></span> <span data-ttu-id="dd2bc-120">Большие ответы разбиваются на несколько пакетов; время ожидания получения применяется для выборки каждого пакета данных за пределами сокета.</span><span class="sxs-lookup"><span data-stu-id="dd2bc-120">Large responses are be broken up into multiple packets; the receive time-out applies to fetching each packet of data off the socket.</span></span> <span data-ttu-id="dd2bc-121">Значение по умолчанию — 30 000 (30 секунд).</span><span class="sxs-lookup"><span data-stu-id="dd2bc-121">The default value is 30,000 (30 seconds).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dd2bc-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="dd2bc-122">Return value</span></span>

<span data-ttu-id="dd2bc-123">В случае успешного выполнения возвращается значение **S \_** , а в противном случае — значение ошибки.</span><span class="sxs-lookup"><span data-stu-id="dd2bc-123">The return value is **S\_OK** on success or an error value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="dd2bc-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="dd2bc-124">Remarks</span></span>

<span data-ttu-id="dd2bc-125">Все параметры обязательные.</span><span class="sxs-lookup"><span data-stu-id="dd2bc-125">All parameters are required.</span></span> <span data-ttu-id="dd2bc-126">Значение 0 или-1 задает время ожидания бесконечно.</span><span class="sxs-lookup"><span data-stu-id="dd2bc-126">A value of 0 or -1 sets a time-out to wait infinitely.</span></span> <span data-ttu-id="dd2bc-127">Значение больше 0 задает значение времени ожидания в миллисекундах.</span><span class="sxs-lookup"><span data-stu-id="dd2bc-127">A value greater than 0 sets the time-out value in milliseconds.</span></span> <span data-ttu-id="dd2bc-128">Например, 30 000 устанавливает время ожидания равным 30 секундам.</span><span class="sxs-lookup"><span data-stu-id="dd2bc-128">For example, 30,000 would set the time-out to 30 seconds.</span></span> <span data-ttu-id="dd2bc-129">Все отрицательные значения, отличные от-1, приводят к сбою этого метода.</span><span class="sxs-lookup"><span data-stu-id="dd2bc-129">All negative values other than -1 cause this method to fail.</span></span>

<span data-ttu-id="dd2bc-130">Значения времени ожидания применяются на уровне Winsock.</span><span class="sxs-lookup"><span data-stu-id="dd2bc-130">Time-out values are applied at the Winsock layer.</span></span>

> [!Note]  
> <span data-ttu-id="dd2bc-131">Для Windows XP и Windows 2000 см. раздел [требования к времени выполнения](winhttp-start-page.md) на начальной странице WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="dd2bc-131">For Windows XP and Windows 2000, see the [Run-Time Requirements](winhttp-start-page.md) section of the WinHttp start page.</span></span>

 

## <a name="examples"></a><span data-ttu-id="dd2bc-132">Примеры</span><span class="sxs-lookup"><span data-stu-id="dd2bc-132">Examples</span></span>

<span data-ttu-id="dd2bc-133">В следующем примере показано, как настроить время ожидания WinHTTP до 30 секунд, открыть HTTP-соединение, отправить HTTP-запрос и прочитать текст ответа.</span><span class="sxs-lookup"><span data-stu-id="dd2bc-133">The following example shows how to set all WinHTTP time-outs to 30 seconds, open an HTTP connection, send an HTTP request, and read the response text.</span></span>


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
    {    // Set Time-outs.
        hr = pIWinHttpRequest->SetTimeouts(30000, 30000,
                                           30000, 30000);
    }
    if (SUCCEEDED(hr))
    {    // Open WinHttpRequest.
        BSTR bstrMethod  = SysAllocString(L"GET");
        BSTR bstrUrl = SysAllocString(L"https://microsoft.com");
        hr = pIWinHttpRequest->Open(bstrMethod,
                                    bstrUrl,
                                    varFalse);
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
    {    // Print response to console.
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



<span data-ttu-id="dd2bc-134">В следующем примере сценария показано, как настроить время ожидания WinHTTP до 30 секунд, открыть HTTP-соединение и отправить HTTP-запрос.</span><span class="sxs-lookup"><span data-stu-id="dd2bc-134">The following scripting example shows how to set all WinHTTP time-outs to 30 seconds, open an HTTP connection, and send an HTTP request.</span></span>


```JScript
// Instantiate a WinHttpRequest object.
var WinHttpReq = new ActiveXObject("WinHttp.WinHttpRequest.5.1");

// Set time-outs. If time-outs are set, they must 
// be set before open.
WinHttpReq.SetTimeouts(30000, 30000, 30000, 30000);

// Initialize an HTTP request.  
WinHttpReq.Open("GET", "https://www.microsoft.com", false);

// Send the HTTP request.
WinHttpReq.Send();
```



## <a name="requirements"></a><span data-ttu-id="dd2bc-135">Требования</span><span class="sxs-lookup"><span data-stu-id="dd2bc-135">Requirements</span></span>



| <span data-ttu-id="dd2bc-136">Требование</span><span class="sxs-lookup"><span data-stu-id="dd2bc-136">Requirement</span></span> | <span data-ttu-id="dd2bc-137">Значение</span><span class="sxs-lookup"><span data-stu-id="dd2bc-137">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="dd2bc-138">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="dd2bc-138">Minimum supported client</span></span><br/> | <span data-ttu-id="dd2bc-139">Windows XP, Windows 2000 Professional с пакетом обновления 3 (SP3), \[ только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="dd2bc-139">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="dd2bc-140">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="dd2bc-140">Minimum supported server</span></span><br/> | <span data-ttu-id="dd2bc-141">Windows Server 2003, Windows 2000 Server с пакетом обновления 3 (SP3), \[ только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="dd2bc-141">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>         |
| <span data-ttu-id="dd2bc-142">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="dd2bc-142">Redistributable</span></span><br/>          | <span data-ttu-id="dd2bc-143">WinHTTP 5,0 и Internet Explorer 5,01 или более поздней версии в Windows XP и Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="dd2bc-143">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span><br/> |
| <span data-ttu-id="dd2bc-144">IDL</span><span class="sxs-lookup"><span data-stu-id="dd2bc-144">IDL</span></span><br/>                      | <dl> <span data-ttu-id="dd2bc-145"><dt>HttpRequest. idl</dt></span><span class="sxs-lookup"><span data-stu-id="dd2bc-145"><dt>HttpRequest.idl</dt></span></span> </dl> |
| <span data-ttu-id="dd2bc-146">Библиотека</span><span class="sxs-lookup"><span data-stu-id="dd2bc-146">Library</span></span><br/>                  | <dl> <span data-ttu-id="dd2bc-147"><dt>WinHTTP. lib</dt></span><span class="sxs-lookup"><span data-stu-id="dd2bc-147"><dt>Winhttp.lib</dt></span></span> </dl>     |
| <span data-ttu-id="dd2bc-148">DLL</span><span class="sxs-lookup"><span data-stu-id="dd2bc-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dd2bc-149"><dt>Winhttp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dd2bc-149"><dt>Winhttp.dll</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="dd2bc-150">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="dd2bc-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd2bc-151">**ивинхттпрекуест**</span><span class="sxs-lookup"><span data-stu-id="dd2bc-151">**IWinHttpRequest**</span></span>](iwinhttprequest-interface.md)
</dt> <dt>

[<span data-ttu-id="dd2bc-152">**WinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="dd2bc-152">**WinHttpRequest**</span></span>](winhttprequest.md)
</dt> <dt>

[<span data-ttu-id="dd2bc-153">Версии WinHTTP</span><span class="sxs-lookup"><span data-stu-id="dd2bc-153">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

 




