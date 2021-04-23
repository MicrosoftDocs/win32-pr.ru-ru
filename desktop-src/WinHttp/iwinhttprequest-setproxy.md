---
description: Задает сведения о прокси-сервере.
ms.assetid: 279d0557-2718-4c50-b84c-cc7c8def57a6
title: 'Метод Ивинхттпрекуест:: Сетпрокси'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWinHttpRequest.SetProxy
- WinHttpRequest.SetProxy
api_type:
- COM
api_location:
- Winhttp.dll
ms.openlocfilehash: 7af3c7c33b17e14c3adbdd70f3d2031e7438747a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105713117"
---
# <a name="iwinhttprequestsetproxy-method"></a><span data-ttu-id="e177a-103">Метод Ивинхттпрекуест:: Сетпрокси</span><span class="sxs-lookup"><span data-stu-id="e177a-103">IWinHttpRequest::SetProxy method</span></span>

<span data-ttu-id="e177a-104">Метод **сетпрокси** задает сведения о прокси-сервере.</span><span class="sxs-lookup"><span data-stu-id="e177a-104">The **SetProxy** method sets proxy server information.</span></span>

## <a name="syntax"></a><span data-ttu-id="e177a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e177a-105">Syntax</span></span>


```C++
HRESULT SetProxy(
  [in]           HTTPREQUEST_PROXY_SETTING ProxySetting,
  [in, optional] VARIANT                   ProxyServer,
  [in, optional] VARIANT                   BypassList
);
```



## <a name="parameters"></a><span data-ttu-id="e177a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e177a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e177a-107">*Проксисеттинг* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e177a-107">*ProxySetting* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e177a-108">Флаги, управляющие этим методом.</span><span class="sxs-lookup"><span data-stu-id="e177a-108">The flags that control this method.</span></span> <span data-ttu-id="e177a-109">Может принимать одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="e177a-109">Can be one of the following values.</span></span>



| <span data-ttu-id="e177a-110">Значение</span><span class="sxs-lookup"><span data-stu-id="e177a-110">Value</span></span>                                                                                                           | <span data-ttu-id="e177a-111">Значение</span><span class="sxs-lookup"><span data-stu-id="e177a-111">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                               |
|-----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e177a-112"><dt>HTTPREQUEST \_ проксисеттинг \_ по умолчанию</dt></span><span class="sxs-lookup"><span data-stu-id="e177a-112"><dt>HTTPREQUEST\_PROXYSETTING\_DEFAULT</dt></span></span> </dl>   | <span data-ttu-id="e177a-113">Параметр прокси-сервера по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="e177a-113">Default proxy setting.</span></span> <span data-ttu-id="e177a-114">Эквивалентно **\_ \_ onconfig проксисеттинг HTTPREQUEST**.</span><span class="sxs-lookup"><span data-stu-id="e177a-114">Equivalent to **HTTPREQUEST\_PROXYSETTING\_PRECONFIG**.</span></span><br/>                                                                                                                                                                                                                                                             |
| <dl> <span data-ttu-id="e177a-115"><dt>HTTPREQUEST \_ проксисеттинг, \_ Преднастройка</dt></span><span class="sxs-lookup"><span data-stu-id="e177a-115"><dt>HTTPREQUEST\_PROXYSETTING\_PRECONFIG</dt></span></span> </dl> | <span data-ttu-id="e177a-116">Указывает, что параметры прокси-сервера должны быть получены из реестра.</span><span class="sxs-lookup"><span data-stu-id="e177a-116">Indicates that the proxy settings should be obtained from the registry.</span></span> <span data-ttu-id="e177a-117">Предполагается, что [Proxycfg.exe](proxycfg-exe--a-proxy-configuration-tool.md) был запущен.</span><span class="sxs-lookup"><span data-stu-id="e177a-117">This assumes that [Proxycfg.exe](proxycfg-exe--a-proxy-configuration-tool.md) has been run.</span></span> <span data-ttu-id="e177a-118">Если Proxycfg.exe не было запущено и указан параметр **HttpRequest \_ проксисеттинг \_** , то поведение эквивалентно **HttpRequest \_ проксисеттинг \_ Direct**.</span><span class="sxs-lookup"><span data-stu-id="e177a-118">If Proxycfg.exe has not been run and **HTTPREQUEST\_PROXYSETTING\_PRECONFIG** is specified, then the behavior is equivalent to **HTTPREQUEST\_PROXYSETTING\_DIRECT**.</span></span><br/> |
| <dl> <span data-ttu-id="e177a-119"><dt>HTTPREQUEST \_ проксисеттинг \_ Direct</dt></span><span class="sxs-lookup"><span data-stu-id="e177a-119"><dt>HTTPREQUEST\_PROXYSETTING\_DIRECT</dt></span></span> </dl>    | <span data-ttu-id="e177a-120">Указывает, что доступ к всем серверам HTTP и HTTPS должен осуществляться напрямую.</span><span class="sxs-lookup"><span data-stu-id="e177a-120">Indicates that all HTTP and HTTPS servers should be accessed directly.</span></span> <span data-ttu-id="e177a-121">Используйте эту команду, если нет прокси-сервера.</span><span class="sxs-lookup"><span data-stu-id="e177a-121">Use this command if there is no proxy server.</span></span><br/>                                                                                                                                                                                                                       |
| <dl> <span data-ttu-id="e177a-122"><dt>\_ \_ прокси-сервер HTTPREQUEST проксисеттинг</dt></span><span class="sxs-lookup"><span data-stu-id="e177a-122"><dt>HTTPREQUEST\_PROXYSETTING\_PROXY</dt></span></span> </dl>     | <span data-ttu-id="e177a-123">Если **указан \_ \_ прокси-сервер HTTPREQUEST проксисеттинг** , для параметра *варпроксисервер* следует задать строку прокси-сервера, а для *варбипасслист* — строку списка обхода домена.</span><span class="sxs-lookup"><span data-stu-id="e177a-123">When **HTTPREQUEST\_PROXYSETTING\_PROXY** is specified, *varProxyServer* should be set to a proxy server string and *varBypassList* should be set to a domain bypass list string.</span></span> <span data-ttu-id="e177a-124">Эта конфигурация прокси-сервера применяется только к текущему экземпляру объекта [**WinHttpRequest**](winhttprequest.md) .</span><span class="sxs-lookup"><span data-stu-id="e177a-124">This proxy configuration applies only to the current instance of the [**WinHttpRequest**](winhttprequest.md) object.</span></span><br/>                                    |



 

</dd> <dt>

<span data-ttu-id="e177a-125">*Proxyserver* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="e177a-125">*ProxyServer* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e177a-126">Задайте в качестве значения строки прокси-сервера, если *проксисеттинг* равен **HTTPREQUEST \_ проксисеттинг \_ proxy**.</span><span class="sxs-lookup"><span data-stu-id="e177a-126">Set to a proxy server string when *ProxySetting* equals **HTTPREQUEST\_PROXYSETTING\_PROXY**.</span></span>

</dd> <dt>

<span data-ttu-id="e177a-127">*Бипасслист* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="e177a-127">*BypassList* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e177a-128">Задайте для параметра значение Строка обхода домена, если *проксисеттинг* равен **HTTPREQUEST \_ проксисеттинг \_ proxy**.</span><span class="sxs-lookup"><span data-stu-id="e177a-128">Set to a domain bypass list string when *ProxySetting* equals **HTTPREQUEST\_PROXYSETTING\_PROXY**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e177a-129">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e177a-129">Return value</span></span>

<span data-ttu-id="e177a-130">В случае успешного выполнения возвращается значение **S \_** , а в противном случае — значение ошибки.</span><span class="sxs-lookup"><span data-stu-id="e177a-130">The return value is **S\_OK** on success or an error value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="e177a-131">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e177a-131">Remarks</span></span>

<span data-ttu-id="e177a-132">Позволяет вызывающему приложению указать использование сведений о прокси-сервере по умолчанию (настроенных средством настройки прокси-сервера) или переопределить [Proxycfg.exe](proxycfg-exe--a-proxy-configuration-tool.md).</span><span class="sxs-lookup"><span data-stu-id="e177a-132">Enables the calling application to specify use of default proxy information (configured by the proxy configuration tool) or to override [Proxycfg.exe](proxycfg-exe--a-proxy-configuration-tool.md).</span></span> <span data-ttu-id="e177a-133">Этот метод должен быть вызван перед вызовом метода [**Send**](iwinhttprequest-send.md) .</span><span class="sxs-lookup"><span data-stu-id="e177a-133">This method must be called before calling the [**Send**](iwinhttprequest-send.md) method.</span></span> <span data-ttu-id="e177a-134">Если этот метод вызывается после метода [**Send**](iwinhttprequest-send.md) , он не действует.</span><span class="sxs-lookup"><span data-stu-id="e177a-134">If this method is called after the [**Send**](iwinhttprequest-send.md) method, it has no effect.</span></span>

<span data-ttu-id="e177a-135">[**Ивинхттпрекуест**](iwinhttprequest-interface.md) передает эти параметры службам Microsoft Windows HTTP (WinHTTP).</span><span class="sxs-lookup"><span data-stu-id="e177a-135">[**IWinHttpRequest**](iwinhttprequest-interface.md) passes these parameters to Microsoft Windows HTTP Services (WinHTTP).</span></span>

> [!Note]  
> <span data-ttu-id="e177a-136">Для Windows XP и Windows 2000 см. раздел [требования к времени выполнения](winhttp-start-page.md) на начальной странице WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="e177a-136">For Windows XP and Windows 2000, see the [Run-Time Requirements](winhttp-start-page.md) section of the WinHTTP Start Page.</span></span>

 

## <a name="examples"></a><span data-ttu-id="e177a-137">Примеры</span><span class="sxs-lookup"><span data-stu-id="e177a-137">Examples</span></span>

<span data-ttu-id="e177a-138">В следующем примере показано, как задать параметры прокси для конкретного прокси-сервера, открыть HTTP-соединение, отправить HTTP-запрос и прочитать текст ответа.</span><span class="sxs-lookup"><span data-stu-id="e177a-138">The following example shows how to set the proxy settings for a particular proxy server, open an HTTP connection, send an HTTP request, and read the response text.</span></span> <span data-ttu-id="e177a-139">Этот пример необходимо запустить из командной строки.</span><span class="sxs-lookup"><span data-stu-id="e177a-139">This example must be run from a command prompt.</span></span> <span data-ttu-id="e177a-140">Эти параметры прокси-сервера работают, только если у вас есть прокси-сервер с именем "прокси- \_ сервер", использующий порт 80, и компьютер может обходить прокси-сервер, если имя узла заканчивается на ". Microsoft.com".</span><span class="sxs-lookup"><span data-stu-id="e177a-140">These proxy settings work only if you have a proxy server named "proxy\_server" that uses port 80 and your computer can bypass the proxy server when the host name ends with ".microsoft.com".</span></span>


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
    VARIANT         varProxy;
    VARIANT         varUrl;
    
    CLSID           clsid;

    VariantInit(&varFalse);
    V_VT(&varFalse)   = VT_BOOL;
    V_BOOL(&varFalse) = VARIANT_FALSE;

    VariantInit(&varEmpty);
    V_VT(&varEmpty) = VT_ERROR;

    VariantInit(&varProxy);
    VariantInit(&varUrl);

    hr = CLSIDFromProgID(L"WinHttp.WinHttpRequest.5.1", &clsid);

    if (SUCCEEDED(hr))
    {
        hr = CoCreateInstance(clsid, NULL, 
                              CLSCTX_INPROC_SERVER, 
                              IID_IWinHttpRequest, 
                              (void **)&pIWinHttpRequest);
    }
    if (SUCCEEDED(hr))
    {   // Specify proxy and URL.
                varProxy.vt = VT_BSTR;
                varProxy.bstrVal = SysAllocString(L"proxy_server:80");
                varUrl.vt = VT_BSTR;
                varUrl.bstrVal = SysAllocString(L"*.microsoft.com");
                hr = pIWinHttpRequest->SetProxy(HTTPREQUEST_PROXYSETTING_PROXY,
                                    varProxy, varUrl); 
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
    if (SUCCEEDED(hr))
    {   // Print the response to a console.
                wprintf(L"%.256s",bstrResponse);
    }
        
        // Release memory.
    if (pIWinHttpRequest)
        pIWinHttpRequest->Release();
        if (varProxy.bstrVal)
                SysFreeString(varProxy.bstrVal);
        if (varUrl.bstrVal)
                SysFreeString(varUrl.bstrVal);
    if (bstrResponse)
        SysFreeString(bstrResponse);
        
        CoUninitialize();
        return 0;
}
```



<span data-ttu-id="e177a-141">В следующем примере скрипта показано, как задать параметры прокси для конкретного прокси-сервера, открыть HTTP-соединение, отправить HTTP-запрос и прочитать текст ответа.</span><span class="sxs-lookup"><span data-stu-id="e177a-141">The following scripting example shows how to set the proxy settings for a particular proxy server, open an HTTP connection, send an HTTP request, and read the response text.</span></span> <span data-ttu-id="e177a-142">Эти параметры прокси-сервера работают, только если у вас есть прокси-сервер с именем "прокси- \_ сервер", использующий порт 80, и компьютер может обходить прокси-сервер, если имя узла заканчивается на ". Microsoft.com".</span><span class="sxs-lookup"><span data-stu-id="e177a-142">These proxy settings work only if you have a proxy server named "proxy\_server" that uses port 80 and your computer can bypass the proxy server when the host name ends with ".microsoft.com".</span></span>


```JScript
// HttpRequest SetCredentials flags.
HTTPREQUEST_PROXYSETTING_DEFAULT   = 0;
HTTPREQUEST_PROXYSETTING_PRECONFIG = 0;
HTTPREQUEST_PROXYSETTING_DIRECT    = 1;
HTTPREQUEST_PROXYSETTING_PROXY     = 2;

// Instantiate a WinHttpRequest object.
var WinHttpReq = new ActiveXObject("WinHttp.WinHttpRequest.5.1");

// Use proxy_server for all requests outside of 
// the microsoft.com domain.
WinHttpReq.SetProxy( HTTPREQUEST_PROXYSETTING_PROXY, 
                     "proxy_server:80", 
                     "*.microsoft.com");

// Initialize an HTTP request.  
WinHttpReq.Open("GET", "https://www.microsoft.com", false);

// Send the HTTP request.
WinHttpReq.Send(); 

// Display the response text.
WScript.Echo( WinHttpReq.ResponseText);
```



## <a name="requirements"></a><span data-ttu-id="e177a-143">Требования</span><span class="sxs-lookup"><span data-stu-id="e177a-143">Requirements</span></span>



| <span data-ttu-id="e177a-144">Требование</span><span class="sxs-lookup"><span data-stu-id="e177a-144">Requirement</span></span> | <span data-ttu-id="e177a-145">Значение</span><span class="sxs-lookup"><span data-stu-id="e177a-145">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="e177a-146">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e177a-146">Minimum supported client</span></span><br/> | <span data-ttu-id="e177a-147">Windows XP, Windows 2000 Professional с пакетом обновления 3 (SP3), \[ только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="e177a-147">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="e177a-148">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e177a-148">Minimum supported server</span></span><br/> | <span data-ttu-id="e177a-149">Windows Server 2003, Windows 2000 Server с пакетом обновления 3 (SP3), \[ только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="e177a-149">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>         |
| <span data-ttu-id="e177a-150">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="e177a-150">Redistributable</span></span><br/>          | <span data-ttu-id="e177a-151">WinHTTP 5,0 и Internet Explorer 5,01 или более поздней версии в Windows XP и Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="e177a-151">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span><br/> |
| <span data-ttu-id="e177a-152">IDL</span><span class="sxs-lookup"><span data-stu-id="e177a-152">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e177a-153"><dt>HttpRequest. idl</dt></span><span class="sxs-lookup"><span data-stu-id="e177a-153"><dt>HttpRequest.idl</dt></span></span> </dl> |
| <span data-ttu-id="e177a-154">Библиотека</span><span class="sxs-lookup"><span data-stu-id="e177a-154">Library</span></span><br/>                  | <dl> <span data-ttu-id="e177a-155"><dt>WinHTTP. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e177a-155"><dt>Winhttp.lib</dt></span></span> </dl>     |
| <span data-ttu-id="e177a-156">DLL</span><span class="sxs-lookup"><span data-stu-id="e177a-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e177a-157"><dt>Winhttp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e177a-157"><dt>Winhttp.dll</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="e177a-158">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e177a-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e177a-159">**ивинхттпрекуест**</span><span class="sxs-lookup"><span data-stu-id="e177a-159">**IWinHttpRequest**</span></span>](iwinhttprequest-interface.md)
</dt> <dt>

[<span data-ttu-id="e177a-160">**WinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="e177a-160">**WinHttpRequest**</span></span>](winhttprequest.md)
</dt> <dt>

[<span data-ttu-id="e177a-161">Версии WinHTTP</span><span class="sxs-lookup"><span data-stu-id="e177a-161">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

 




