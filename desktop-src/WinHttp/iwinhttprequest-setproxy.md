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
# <a name="iwinhttprequestsetproxy-method"></a>Метод Ивинхттпрекуест:: Сетпрокси

Метод **сетпрокси** задает сведения о прокси-сервере.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT SetProxy(
  [in]           HTTPREQUEST_PROXY_SETTING ProxySetting,
  [in, optional] VARIANT                   ProxyServer,
  [in, optional] VARIANT                   BypassList
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Проксисеттинг* \[ окне\]
</dt> <dd>

Флаги, управляющие этим методом. Может принимать одно из следующих значений.



| Значение                                                                                                           | Значение                                                                                                                                                                                                                                                                                                                                               |
|-----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>HTTPREQUEST \_ проксисеттинг \_ по умолчанию</dt> </dl>   | Параметр прокси-сервера по умолчанию. Эквивалентно **\_ \_ onconfig проксисеттинг HTTPREQUEST**.<br/>                                                                                                                                                                                                                                                             |
| <dl> <dt>HTTPREQUEST \_ проксисеттинг, \_ Преднастройка</dt> </dl> | Указывает, что параметры прокси-сервера должны быть получены из реестра. Предполагается, что [Proxycfg.exe](proxycfg-exe--a-proxy-configuration-tool.md) был запущен. Если Proxycfg.exe не было запущено и указан параметр **HttpRequest \_ проксисеттинг \_** , то поведение эквивалентно **HttpRequest \_ проксисеттинг \_ Direct**.<br/> |
| <dl> <dt>HTTPREQUEST \_ проксисеттинг \_ Direct</dt> </dl>    | Указывает, что доступ к всем серверам HTTP и HTTPS должен осуществляться напрямую. Используйте эту команду, если нет прокси-сервера.<br/>                                                                                                                                                                                                                       |
| <dl> <dt>\_ \_ прокси-сервер HTTPREQUEST проксисеттинг</dt> </dl>     | Если **указан \_ \_ прокси-сервер HTTPREQUEST проксисеттинг** , для параметра *варпроксисервер* следует задать строку прокси-сервера, а для *варбипасслист* — строку списка обхода домена. Эта конфигурация прокси-сервера применяется только к текущему экземпляру объекта [**WinHttpRequest**](winhttprequest.md) .<br/>                                    |



 

</dd> <dt>

*Proxyserver* \[ в необязательное\]
</dt> <dd>

Задайте в качестве значения строки прокси-сервера, если *проксисеттинг* равен **HTTPREQUEST \_ проксисеттинг \_ proxy**.

</dd> <dt>

*Бипасслист* \[ в необязательное\]
</dt> <dd>

Задайте для параметра значение Строка обхода домена, если *проксисеттинг* равен **HTTPREQUEST \_ проксисеттинг \_ proxy**.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

В случае успешного выполнения возвращается значение **S \_** , а в противном случае — значение ошибки.

## <a name="remarks"></a>Комментарии

Позволяет вызывающему приложению указать использование сведений о прокси-сервере по умолчанию (настроенных средством настройки прокси-сервера) или переопределить [Proxycfg.exe](proxycfg-exe--a-proxy-configuration-tool.md). Этот метод должен быть вызван перед вызовом метода [**Send**](iwinhttprequest-send.md) . Если этот метод вызывается после метода [**Send**](iwinhttprequest-send.md) , он не действует.

[**Ивинхттпрекуест**](iwinhttprequest-interface.md) передает эти параметры службам Microsoft Windows HTTP (WinHTTP).

> [!Note]  
> Для Windows XP и Windows 2000 см. раздел [требования к времени выполнения](winhttp-start-page.md) на начальной странице WinHTTP.

 

## <a name="examples"></a>Примеры

В следующем примере показано, как задать параметры прокси для конкретного прокси-сервера, открыть HTTP-соединение, отправить HTTP-запрос и прочитать текст ответа. Этот пример необходимо запустить из командной строки. Эти параметры прокси-сервера работают, только если у вас есть прокси-сервер с именем "прокси- \_ сервер", использующий порт 80, и компьютер может обходить прокси-сервер, если имя узла заканчивается на ". Microsoft.com".


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



В следующем примере скрипта показано, как задать параметры прокси для конкретного прокси-сервера, открыть HTTP-соединение, отправить HTTP-запрос и прочитать текст ответа. Эти параметры прокси-сервера работают, только если у вас есть прокси-сервер с именем "прокси- \_ сервер", использующий порт 80, и компьютер может обходить прокси-сервер, если имя узла заканчивается на ". Microsoft.com".


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



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows XP, Windows 2000 Professional с пакетом обновления 3 (SP3), \[ только классические приложения\]<br/>            |
| Минимальная версия сервера<br/> | Windows Server 2003, Windows 2000 Server с пакетом обновления 3 (SP3), \[ только классические приложения\]<br/>         |
| Распространяемые компоненты<br/>          | WinHTTP 5,0 и Internet Explorer 5,01 или более поздней версии в Windows XP и Windows 2000.<br/> |
| IDL<br/>                      | <dl> <dt>HttpRequest. idl</dt> </dl> |
| Библиотека<br/>                  | <dl> <dt>WinHTTP. lib</dt> </dl>     |
| DLL<br/>                      | <dl> <dt>Winhttp.dll</dt> </dl>     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ивинхттпрекуест**](iwinhttprequest-interface.md)
</dt> <dt>

[**WinHttpRequest**](winhttprequest.md)
</dt> <dt>

[Версии WinHTTP](winhttp-versions.md)
</dt> </dl>

 

 




