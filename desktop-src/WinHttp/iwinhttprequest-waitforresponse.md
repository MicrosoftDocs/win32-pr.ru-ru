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
ms.openlocfilehash: e4f72edf2a3532c6d0f2641d979885e6d294c2ad923a28f19b71b348ea3a6377
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119052002"
---
# <a name="iwinhttprequestwaitforresponse-method"></a>Метод Ивинхттпрекуест:: Ваитфорреспонсе

Метод **ваитфорреспонсе** ожидает завершения асинхронного метода [**Send**](iwinhttprequest-send.md) с необязательным значением времени ожидания в секундах.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT WaitForResponse(
  [in, optional] VARIANT      Timeout,
  [out, retval]  VARIANT_BOOL *Succeeded
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Время ожидания* \[ в необязательное\]
</dt> <dd>

Значение времени ожидания в секундах. Время ожидания по умолчанию — Infinite. Чтобы явно задать бесконечное время ожидания, используйте значение-1.

</dd> <dt>

*Прошло* \[ out, retval\]
</dt> <dd>

Получает одно из следующих значений.



| Значение                                                                                                                                                         | Значение                                                |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <span id="VARIANT_TRUE"></span><span id="variant_true"></span><dl> <dt>**ВАРИАНТ \_ true**</dt> </dl>    | Получен ответ.<br/>               |
| <span id="VARIANT_FALSE"></span><span id="variant_false"></span><dl> <dt>**ВАРИАНТ \_ false**</dt> </dl> | Был превышен указанный период ожидания.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

В случае успешного выполнения возвращается значение **S \_** , а в противном случае — значение ошибки.

## <a name="remarks"></a>Remarks

Этот метод приостанавливает выполнение при ожидании ответа на асинхронный запрос. Этот метод должен вызываться после [**отправки**](iwinhttprequest-send.md). Вызывающие приложения могут задавать необязательное значение *времени ожидания* в секундах. Если этот метод истечет из-за истечения времени ожидания, запрос не прерывается. Таким образом, вызывающее приложение может продолжить ожидание запроса (при необходимости) при последующем вызове этого метода.

Вызов этого свойства после того, как синхронный метод [**Send**](iwinhttprequest-send.md) немедленно возвращает результат и не оказывает никакого влияния.

> [!Note]  
> сведения о Windows XP и Windows 2000 см. в разделе [требования к времени выполнения](winhttp-start-page.md) на начальной странице WinHTTP.

 

## <a name="examples"></a>Примеры

В следующем примере показано, как открыть асинхронное HTTP-соединение, отправить HTTP-запрос, дождаться ответа и прочитать текст ответа.


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



В следующем примере скрипта показано, как открыть асинхронное HTTP-соединение, отправить HTTP-запрос, подождать ответа и прочитать текст ответа.


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



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows XP, Windows 2000 Professional с SP3 \[ только для настольных приложений\]<br/>            |
| Минимальная версия сервера<br/> | Windows сервер 2003, Windows 2000 server с пакетом обновления 3 (SP3), \[ только классические приложения\]<br/>         |
| Распространяемые компоненты<br/>          | WinHTTP 5,0 и Internet Explorer 5,01 или более поздней версии в Windows XP и Windows 2000.<br/> |
| IDL<br/>                      | <dl> <dt>HttpRequest. idl</dt> </dl> |
| Библиотека<br/>                  | <dl> <dt>WinHTTP. lib</dt> </dl>     |
| DLL<br/>                      | <dl> <dt>Winhttp.dll</dt> </dl>     |



## <a name="see-also"></a>См. также

<dl> <dt>

[**ивинхттпрекуест**](iwinhttprequest-interface.md)
</dt> <dt>

[**WinHttpRequest**](winhttprequest.md)
</dt> <dt>

[**Открыть**](iwinhttprequest-open.md)
</dt> <dt>

[Версии WinHTTP](winhttp-versions.md)
</dt> </dl>

 

 




