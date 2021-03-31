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
# <a name="iwinhttprequestsettimeouts-method"></a>Метод Ивинхттпрекуест:: Сеттимеаутс

Метод **сеттимеаутс** задает отдельные компоненты времени ожидания операции отправки и получения в миллисекундах.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT SetTimeouts(
  [in] long ResolveTimeout,
  [in] long ConnectTimeout,
  [in] long SendTimeout,
  [in] long ReceiveTimeout
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Ресолветимеаут* \[ окне\]
</dt> <dd>

Значение времени ожидания, применяемое при разрешении имени узла (например, `www.microsoft.com` ) в IP-адрес (например, 192.168.131.199), в миллисекундах. Значение по умолчанию равно нулю, что означает отсутствие времени ожидания (бесконечно). Если время ожидания DNS задано с \_ помощью \_ времени ожидания разрешения имен, то для каждого запроса взимается дополнительная нагрузка по одному потоку.

</dd> <dt>

*ConnectTimeout* \[ окне\]
</dt> <dd>

Значение времени ожидания, применяемое при установлении сокета связи с целевым сервером, в миллисекундах. По умолчанию установлено значение 60000 (60 секунд).

</dd> <dt>

*SendTimeout* \[ окне\]
</dt> <dd>

Значение времени ожидания, применяемое при отправке отдельного пакета данных запроса на сокете связи на целевой сервер в миллисекундах. Большой запрос, отправленный на HTTP-сервер, обычно разбивается на несколько пакетов. время ожидания отправки применяется для отправки каждого пакета по отдельности. Значение по умолчанию — 30 000 (30 секунд).

</dd> <dt>

*ReceiveTimeout равен* \[ окне\]
</dt> <dd>

Значение времени ожидания, применяемое при получении пакета данных ответа от целевого сервера, в миллисекундах. Большие ответы разбиваются на несколько пакетов; время ожидания получения применяется для выборки каждого пакета данных за пределами сокета. Значение по умолчанию — 30 000 (30 секунд).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

В случае успешного выполнения возвращается значение **S \_** , а в противном случае — значение ошибки.

## <a name="remarks"></a>Комментарии

Все параметры обязательные. Значение 0 или-1 задает время ожидания бесконечно. Значение больше 0 задает значение времени ожидания в миллисекундах. Например, 30 000 устанавливает время ожидания равным 30 секундам. Все отрицательные значения, отличные от-1, приводят к сбою этого метода.

Значения времени ожидания применяются на уровне Winsock.

> [!Note]  
> Для Windows XP и Windows 2000 см. раздел [требования к времени выполнения](winhttp-start-page.md) на начальной странице WinHTTP.

 

## <a name="examples"></a>Примеры

В следующем примере показано, как настроить время ожидания WinHTTP до 30 секунд, открыть HTTP-соединение, отправить HTTP-запрос и прочитать текст ответа.


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



В следующем примере сценария показано, как настроить время ожидания WinHTTP до 30 секунд, открыть HTTP-соединение и отправить HTTP-запрос.


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

 

 




