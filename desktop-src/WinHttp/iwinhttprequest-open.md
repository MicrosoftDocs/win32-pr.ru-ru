---
description: Открывает HTTP-соединение с HTTP-ресурсом.
ms.assetid: 5207e873-44c0-4eeb-9db8-d8b69432070c
title: 'Метод Ивинхттпрекуест:: Open'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWinHttpRequest.Open
- WinHttpRequest.Open
api_type:
- COM
api_location:
- Winhttp.dll
ms.openlocfilehash: 5543832eb1ebc3df210237eff71d415de14b2f62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693248"
---
# <a name="iwinhttprequestopen-method"></a><span data-ttu-id="39485-103">Метод Ивинхттпрекуест:: Open</span><span class="sxs-lookup"><span data-stu-id="39485-103">IWinHttpRequest::Open method</span></span>

<span data-ttu-id="39485-104">Метод **Open** открывает HTTP-соединение с HTTP-ресурсом.</span><span class="sxs-lookup"><span data-stu-id="39485-104">The **Open** method opens an HTTP connection to an HTTP resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="39485-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="39485-105">Syntax</span></span>


```C++
HRESULT Open(
  [in]           BSTR    Method,
  [in]           BSTR    Url,
  [in, optional] VARIANT Async
);
```



## <a name="parameters"></a><span data-ttu-id="39485-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="39485-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="39485-107">*Метод* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="39485-107">*Method* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="39485-108">Указывает [*HTTP-команду*](glossary.md) , используемую для метода **Open** , например Get или WHERE.</span><span class="sxs-lookup"><span data-stu-id="39485-108">Specifies the [*HTTP verb*](glossary.md) used for the **Open** method, such as "GET" or "PUT".</span></span> <span data-ttu-id="39485-109">Всегда используйте прописные буквы, так как некоторые серверы пропускают строчные *HTTP-команды*.</span><span class="sxs-lookup"><span data-stu-id="39485-109">Always use uppercase as some servers ignore lowercase *HTTP verb* s.</span></span>

</dd> <dt>

<span data-ttu-id="39485-110">*URL-адрес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="39485-110">*Url* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="39485-111">Указывает имя ресурса.</span><span class="sxs-lookup"><span data-stu-id="39485-111">Specifies the name of the resource.</span></span> <span data-ttu-id="39485-112">Это должен быть абсолютный URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="39485-112">This must be an absolute URL.</span></span>

</dd> <dt>

<span data-ttu-id="39485-113">*Асинхронный* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="39485-113">*Async* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="39485-114">Указывает, следует ли открывать в асинхронном режиме.</span><span class="sxs-lookup"><span data-stu-id="39485-114">Indicates whether to open in asynchronous mode.</span></span>



| <span data-ttu-id="39485-115">Значение</span><span class="sxs-lookup"><span data-stu-id="39485-115">Value</span></span>                                                                                                                                                         | <span data-ttu-id="39485-116">Значение</span><span class="sxs-lookup"><span data-stu-id="39485-116">Meaning</span></span>                                                                                                                                                                                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="VARIANT_FALSE"></span><span id="variant_false"></span><dl> <span data-ttu-id="39485-117"><dt>**ВАРИАНТ \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="39485-117"><dt>**VARIANT\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="39485-118">Открывает HTTP-соединение в синхронном режиме.</span><span class="sxs-lookup"><span data-stu-id="39485-118">Opens the HTTP connection in synchronous mode.</span></span> <span data-ttu-id="39485-119">Вызов [**Send**](iwinhttprequest-send.md) не возвращает, пока не будет полностью получен ответ центром [WinHTTP](about-winhttp.md) .</span><span class="sxs-lookup"><span data-stu-id="39485-119">A call to [**Send**](iwinhttprequest-send.md) does not return until [WinHTTP](about-winhttp.md) has completely received the response.</span></span><br/> |
| <span id="VARIANT_TRUE"></span><span id="variant_true"></span><dl> <span data-ttu-id="39485-120"><dt>**ВАРИАНТ \_ true**</dt></span><span class="sxs-lookup"><span data-stu-id="39485-120"><dt>**VARIANT\_TRUE**</dt></span></span> </dl>    | <span data-ttu-id="39485-121">Открывает HTTP-соединение в асинхронном режиме.</span><span class="sxs-lookup"><span data-stu-id="39485-121">Opens the HTTP connection in asynchronous mode.</span></span><br/>                                                                                                                                        |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="39485-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="39485-122">Return value</span></span>

<span data-ttu-id="39485-123">В случае успешного выполнения возвращается значение **S \_** , а в противном случае — значение ошибки.</span><span class="sxs-lookup"><span data-stu-id="39485-123">The return value is **S\_OK** on success or an error value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="39485-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="39485-124">Remarks</span></span>

<span data-ttu-id="39485-125">Этот метод открывает подключение к ресурсу, указанному в *URL-адресе* , с помощью [*HTTP-команды*](glossary.md) , заданной в *методе*.</span><span class="sxs-lookup"><span data-stu-id="39485-125">This method opens a connection to the resource identified in *Url* using the [*HTTP verb*](glossary.md) given in *Method*.</span></span>

> [!Note]  
> <span data-ttu-id="39485-126">Для Windows XP и Windows 2000 см. раздел [требования к времени выполнения](winhttp-start-page.md) на начальной странице WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="39485-126">For Windows XP and Windows 2000, see the [Run-Time Requirements](winhttp-start-page.md) section of the WinHTTP Start Page.</span></span>

 

## <a name="examples"></a><span data-ttu-id="39485-127">Примеры</span><span class="sxs-lookup"><span data-stu-id="39485-127">Examples</span></span>

<span data-ttu-id="39485-128">В следующем примере показано, как открыть HTTP-соединение, отправить HTTP-запрос и прочитать текст ответа.</span><span class="sxs-lookup"><span data-stu-id="39485-128">The following example shows how to open an HTTP connection, send an HTTP request, and read the response text.</span></span>


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
        hr = pIWinHttpRequest->get_ResponseText(&bstrResponse);
    }
    if (SUCCEEDED(hr))
    {
        // Print the response to a console.
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



<span data-ttu-id="39485-129">В следующем примере скрипта показано, как открыть HTTP-соединение, отправить HTTP-запрос и прочитать текст ответа.</span><span class="sxs-lookup"><span data-stu-id="39485-129">The following scripting example shows how to open an HTTP connection, send an HTTP request, and read the response text.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="39485-130">Требования</span><span class="sxs-lookup"><span data-stu-id="39485-130">Requirements</span></span>



| <span data-ttu-id="39485-131">Требование</span><span class="sxs-lookup"><span data-stu-id="39485-131">Requirement</span></span> | <span data-ttu-id="39485-132">Значение</span><span class="sxs-lookup"><span data-stu-id="39485-132">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="39485-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="39485-133">Minimum supported client</span></span><br/> | <span data-ttu-id="39485-134">Windows XP, Windows 2000 Professional с пакетом обновления 3 (SP3), \[ только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="39485-134">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="39485-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="39485-135">Minimum supported server</span></span><br/> | <span data-ttu-id="39485-136">Windows Server 2003, Windows 2000 Server с пакетом обновления 3 (SP3), \[ только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="39485-136">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>         |
| <span data-ttu-id="39485-137">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="39485-137">Redistributable</span></span><br/>          | <span data-ttu-id="39485-138">WinHTTP 5,0 и Internet Explorer 5,01 или более поздней версии в Windows XP и Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="39485-138">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span><br/> |
| <span data-ttu-id="39485-139">IDL</span><span class="sxs-lookup"><span data-stu-id="39485-139">IDL</span></span><br/>                      | <dl> <span data-ttu-id="39485-140"><dt>HttpRequest. idl</dt></span><span class="sxs-lookup"><span data-stu-id="39485-140"><dt>HttpRequest.idl</dt></span></span> </dl> |
| <span data-ttu-id="39485-141">Библиотека</span><span class="sxs-lookup"><span data-stu-id="39485-141">Library</span></span><br/>                  | <dl> <span data-ttu-id="39485-142"><dt>WinHTTP. lib</dt></span><span class="sxs-lookup"><span data-stu-id="39485-142"><dt>Winhttp.lib</dt></span></span> </dl>     |
| <span data-ttu-id="39485-143">DLL</span><span class="sxs-lookup"><span data-stu-id="39485-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="39485-144"><dt>Winhttp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="39485-144"><dt>Winhttp.dll</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="39485-145">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="39485-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39485-146">**ивинхттпрекуест**</span><span class="sxs-lookup"><span data-stu-id="39485-146">**IWinHttpRequest**</span></span>](iwinhttprequest-interface.md)
</dt> <dt>

[<span data-ttu-id="39485-147">**WinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="39485-147">**WinHttpRequest**</span></span>](winhttprequest.md)
</dt> <dt>

[<span data-ttu-id="39485-148">Версии WinHTTP</span><span class="sxs-lookup"><span data-stu-id="39485-148">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

 




