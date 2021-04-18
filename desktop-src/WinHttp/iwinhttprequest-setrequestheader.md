---
description: Добавляет, изменяет или удаляет заголовок HTTP-запроса.
ms.assetid: 8cb4891d-0bdb-4dea-8ebe-d6ed26a50e41
title: 'Метод Ивинхттпрекуест:: Сетрекуессеадер'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWinHttpRequest.SetRequestHeader
- WinHttpRequest.SetRequestHeader
api_type:
- COM
api_location:
- Winhttp.dll
ms.openlocfilehash: 9bc2ae6df420f38d11fb2f0f19d5fcbd0bcc0909
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674417"
---
# <a name="iwinhttprequestsetrequestheader-method"></a><span data-ttu-id="1fe40-103">Метод Ивинхттпрекуест:: Сетрекуессеадер</span><span class="sxs-lookup"><span data-stu-id="1fe40-103">IWinHttpRequest::SetRequestHeader method</span></span>

<span data-ttu-id="1fe40-104">Метод **сетрекуессеадер** добавляет, изменяет или удаляет заголовок HTTP-запроса.</span><span class="sxs-lookup"><span data-stu-id="1fe40-104">The **SetRequestHeader** method adds, changes, or deletes an HTTP request header.</span></span>

## <a name="syntax"></a><span data-ttu-id="1fe40-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1fe40-105">Syntax</span></span>


```C++
HRESULT SetRequestHeader(
  [in] BSTR Header,
  [in] BSTR Value
);
```



## <a name="parameters"></a><span data-ttu-id="1fe40-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="1fe40-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1fe40-107">*Заголовок* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1fe40-107">*Header* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1fe40-108">Задает имя заголовков, которые необходимо задать, например "Depth".</span><span class="sxs-lookup"><span data-stu-id="1fe40-108">Specifies the name of the header to be set, for example, "depth".</span></span> <span data-ttu-id="1fe40-109">Этот параметр не должен содержать двоеточие и должен быть фактическим текстом заголовка HTTP.</span><span class="sxs-lookup"><span data-stu-id="1fe40-109">This parameter should not contain a colon and must be the actual text of the HTTP header.</span></span>

</dd> <dt>

<span data-ttu-id="1fe40-110">*Значение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1fe40-110">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1fe40-111">Задает значение заголовка, например "Infinity".</span><span class="sxs-lookup"><span data-stu-id="1fe40-111">Specifies the value of the header, for example, "infinity".</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1fe40-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1fe40-112">Return value</span></span>

<span data-ttu-id="1fe40-113">В случае успешного выполнения возвращается значение **S \_** , а в противном случае — значение ошибки.</span><span class="sxs-lookup"><span data-stu-id="1fe40-113">The return value is **S\_OK** on success or an error value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="1fe40-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1fe40-114">Remarks</span></span>

<span data-ttu-id="1fe40-115">Заголовки передаются по перенаправлениям.</span><span class="sxs-lookup"><span data-stu-id="1fe40-115">Headers are transferred across redirects.</span></span> <span data-ttu-id="1fe40-116">Это может создать уязвимость системы безопасности.</span><span class="sxs-lookup"><span data-stu-id="1fe40-116">This can create a security vulnerability.</span></span> <span data-ttu-id="1fe40-117">Чтобы избежать переноса заголовков при перенаправлении, используйте обратный [*вызов \_ \_ обратного вызова состояния WinHTTP*](/windows/win32/api/winhttp/nc-winhttp-winhttp_status_callback) для исправления конкретных заголовков при перенаправлении.</span><span class="sxs-lookup"><span data-stu-id="1fe40-117">To avoid having headers transferred if a redirect occurs, use the [*WINHTTP\_STATUS\_CALLBACK*](/windows/win32/api/winhttp/nc-winhttp-winhttp_status_callback) callback to correct the specific headers when a redirect occurs.</span></span>

<span data-ttu-id="1fe40-118">Метод **сетрекуессеадер** позволяет вызывающему приложению добавить или удалить заголовок HTTP-запроса перед отправкой запроса.</span><span class="sxs-lookup"><span data-stu-id="1fe40-118">The **SetRequestHeader** method enables the calling application to add or delete an HTTP request header prior to sending the request.</span></span> <span data-ttu-id="1fe40-119">Имя заголовка задается в *заголовке*, а маркер или значение заголовка задается в *значении*.</span><span class="sxs-lookup"><span data-stu-id="1fe40-119">The header name is given in *Header*, and the header token or value is given in *Value*.</span></span> <span data-ttu-id="1fe40-120">Чтобы добавить заголовок, укажите имя и значение заголовка.</span><span class="sxs-lookup"><span data-stu-id="1fe40-120">To add a header, supply a header name and value.</span></span> <span data-ttu-id="1fe40-121">Если другой заголовок с таким именем уже существует, он будет заменен.</span><span class="sxs-lookup"><span data-stu-id="1fe40-121">If another header already exists with this name, it is replaced.</span></span> <span data-ttu-id="1fe40-122">Чтобы удалить заголовок, присвойте параметру *Header* имя заголовка, которое нужно удалить, и задайте для него *значение* **null**.</span><span class="sxs-lookup"><span data-stu-id="1fe40-122">To delete a header, set *Header* to the name of the header to delete and set *Value* to **NULL**.</span></span>

<span data-ttu-id="1fe40-123">Проверяется имя и значение заголовков запросов, добавленных с помощью этого метода.</span><span class="sxs-lookup"><span data-stu-id="1fe40-123">The name and value of request headers added with this method are validated.</span></span> <span data-ttu-id="1fe40-124">Заголовки должны иметь правильный формат.</span><span class="sxs-lookup"><span data-stu-id="1fe40-124">Headers must be well formed.</span></span> <span data-ttu-id="1fe40-125">Дополнительные сведения о допустимых заголовках HTTP см. в [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt).</span><span class="sxs-lookup"><span data-stu-id="1fe40-125">For more information about valid HTTP headers, see [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt).</span></span> <span data-ttu-id="1fe40-126">Если используется недопустимый заголовок, возникает ошибка и заголовок не добавляется.</span><span class="sxs-lookup"><span data-stu-id="1fe40-126">If an invalid header is used, an error occurs and the header is not added.</span></span>

> [!Note]  
> <span data-ttu-id="1fe40-127">Для Windows XP и Windows 2000 см. раздел [требования к времени выполнения](winhttp-start-page.md) на начальной странице WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="1fe40-127">For Windows XP and Windows 2000, see the [Run-Time Requirements](winhttp-start-page.md) section of the WinHTTP Start Page.</span></span>

 

## <a name="examples"></a><span data-ttu-id="1fe40-128">Примеры</span><span class="sxs-lookup"><span data-stu-id="1fe40-128">Examples</span></span>

<span data-ttu-id="1fe40-129">В следующем примере показано, как открыть HTTP-соединение, задать заголовок запроса, отправить HTTP-запрос и прочитать текст ответа.</span><span class="sxs-lookup"><span data-stu-id="1fe40-129">The following example shows how to open an HTTP connection, set a request header, send an HTTP request, and read the response text.</span></span> <span data-ttu-id="1fe40-130">Этот пример необходимо запустить из командной строки.</span><span class="sxs-lookup"><span data-stu-id="1fe40-130">This example must be run from a command prompt.</span></span>


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
    {    // Open WinHttpRequest.
        BSTR bstrMethod  = SysAllocString(L"GET");
        BSTR bstrUrl = SysAllocString(L"https://microsoft.com");
        hr = pIWinHttpRequest->Open(bstrMethod, bstrUrl, varFalse);
        SysFreeString(bstrMethod);
        SysFreeString(bstrUrl);
    }
    if (SUCCEEDED(hr))
    {    // Set request header.
        BSTR bstrName  = SysAllocString(L"Date");
        BSTR bstrValue = SysAllocString(L"Fri, 16 Mar 2001 00:25:54 GMT");
        hr = pIWinHttpRequest->SetRequestHeader(bstrName, bstrValue);
        SysFreeString(bstrName);
        SysFreeString(bstrValue);
    }
    if (SUCCEEDED(hr))
    {    // Send Request.
        hr = pIWinHttpRequest->Send(varEmpty);
    }
    if (SUCCEEDED(hr))
    {    // Get Response headers.
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



<span data-ttu-id="1fe40-131">В следующем примере скрипта показано, как открыть HTTP-соединение, задать заголовок запроса и отправить HTTP-запрос.</span><span class="sxs-lookup"><span data-stu-id="1fe40-131">The following scripting example shows how to open an HTTP connection, set a request header, and send an HTTP request.</span></span>


```JScript
// Instantiate a WinHttpRequest object.
var WinHttpReq = new ActiveXObject("WinHttp.WinHttpRequest.5.1");

// Initialize an HTTP request.  
WinHttpReq.Open("GET", "https://www.microsoft.com", false);

// Add/replace a request header.
WinHttpReq.SetRequestHeader("Date", Date());

// Send the HTTP request.
WinHttpReq.Send();
```



## <a name="requirements"></a><span data-ttu-id="1fe40-132">Требования</span><span class="sxs-lookup"><span data-stu-id="1fe40-132">Requirements</span></span>



| <span data-ttu-id="1fe40-133">Требование</span><span class="sxs-lookup"><span data-stu-id="1fe40-133">Requirement</span></span> | <span data-ttu-id="1fe40-134">Значение</span><span class="sxs-lookup"><span data-stu-id="1fe40-134">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="1fe40-135">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1fe40-135">Minimum supported client</span></span><br/> | <span data-ttu-id="1fe40-136">Windows XP, Windows 2000 Professional с пакетом обновления 3 (SP3), \[ только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="1fe40-136">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="1fe40-137">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1fe40-137">Minimum supported server</span></span><br/> | <span data-ttu-id="1fe40-138">Windows Server 2003, Windows 2000 Server с пакетом обновления 3 (SP3), \[ только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="1fe40-138">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>         |
| <span data-ttu-id="1fe40-139">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="1fe40-139">Redistributable</span></span><br/>          | <span data-ttu-id="1fe40-140">WinHTTP 5,0 и Internet Explorer 5,01 или более поздней версии в Windows XP и Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="1fe40-140">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span><br/> |
| <span data-ttu-id="1fe40-141">IDL</span><span class="sxs-lookup"><span data-stu-id="1fe40-141">IDL</span></span><br/>                      | <dl> <span data-ttu-id="1fe40-142"><dt>HttpRequest. idl</dt></span><span class="sxs-lookup"><span data-stu-id="1fe40-142"><dt>HttpRequest.idl</dt></span></span> </dl> |
| <span data-ttu-id="1fe40-143">Библиотека</span><span class="sxs-lookup"><span data-stu-id="1fe40-143">Library</span></span><br/>                  | <dl> <span data-ttu-id="1fe40-144"><dt>WinHTTP. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1fe40-144"><dt>Winhttp.lib</dt></span></span> </dl>     |
| <span data-ttu-id="1fe40-145">DLL</span><span class="sxs-lookup"><span data-stu-id="1fe40-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1fe40-146"><dt>Winhttp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1fe40-146"><dt>Winhttp.dll</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="1fe40-147">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1fe40-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1fe40-148">**ивинхттпрекуест**</span><span class="sxs-lookup"><span data-stu-id="1fe40-148">**IWinHttpRequest**</span></span>](iwinhttprequest-interface.md)
</dt> <dt>

[<span data-ttu-id="1fe40-149">**WinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="1fe40-149">**WinHttpRequest**</span></span>](winhttprequest.md)
</dt> <dt>

[<span data-ttu-id="1fe40-150">Версии WinHTTP</span><span class="sxs-lookup"><span data-stu-id="1fe40-150">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

