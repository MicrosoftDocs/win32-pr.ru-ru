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
# <a name="iwinhttprequestsetrequestheader-method"></a>Метод Ивинхттпрекуест:: Сетрекуессеадер

Метод **сетрекуессеадер** добавляет, изменяет или удаляет заголовок HTTP-запроса.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT SetRequestHeader(
  [in] BSTR Header,
  [in] BSTR Value
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Заголовок* \[ окне\]
</dt> <dd>

Задает имя заголовков, которые необходимо задать, например "Depth". Этот параметр не должен содержать двоеточие и должен быть фактическим текстом заголовка HTTP.

</dd> <dt>

*Значение* \[ окне\]
</dt> <dd>

Задает значение заголовка, например "Infinity".

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

В случае успешного выполнения возвращается значение **S \_** , а в противном случае — значение ошибки.

## <a name="remarks"></a>Комментарии

Заголовки передаются по перенаправлениям. Это может создать уязвимость системы безопасности. Чтобы избежать переноса заголовков при перенаправлении, используйте обратный [*вызов \_ \_ обратного вызова состояния WinHTTP*](/windows/win32/api/winhttp/nc-winhttp-winhttp_status_callback) для исправления конкретных заголовков при перенаправлении.

Метод **сетрекуессеадер** позволяет вызывающему приложению добавить или удалить заголовок HTTP-запроса перед отправкой запроса. Имя заголовка задается в *заголовке*, а маркер или значение заголовка задается в *значении*. Чтобы добавить заголовок, укажите имя и значение заголовка. Если другой заголовок с таким именем уже существует, он будет заменен. Чтобы удалить заголовок, присвойте параметру *Header* имя заголовка, которое нужно удалить, и задайте для него *значение* **null**.

Проверяется имя и значение заголовков запросов, добавленных с помощью этого метода. Заголовки должны иметь правильный формат. Дополнительные сведения о допустимых заголовках HTTP см. в [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt). Если используется недопустимый заголовок, возникает ошибка и заголовок не добавляется.

> [!Note]  
> Для Windows XP и Windows 2000 см. раздел [требования к времени выполнения](winhttp-start-page.md) на начальной странице WinHTTP.

 

## <a name="examples"></a>Примеры

В следующем примере показано, как открыть HTTP-соединение, задать заголовок запроса, отправить HTTP-запрос и прочитать текст ответа. Этот пример необходимо запустить из командной строки.


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



В следующем примере скрипта показано, как открыть HTTP-соединение, задать заголовок запроса и отправить HTTP-запрос.


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

 

