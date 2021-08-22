---
description: Извлекает тело объекта ответа в виде массива байтов без знака.
ms.assetid: 557913e0-9f19-42fc-bfca-9ed248972b4b
title: 'Свойство Ивинхттпрекуест:: Респонсебоди'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWinHttpRequest.ResponseBody
- IWinHttpRequest.get_ResponseBody
- WinHttpRequest.ResponseBody
api_type:
- COM
api_location:
- Winhttp.dll
ms.openlocfilehash: 56eac42d41054cf7c01ff0c69ffcb82353db7182acf15765b25149560d5f7391
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118563232"
---
# <a name="iwinhttprequestresponsebody-property"></a>Свойство Ивинхттпрекуест:: Респонсебоди

Свойство **респонсебоди** извлекает тело объекта ответа в виде массива байтов без знака.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT get_ResponseBody(
  [out, retval] VARIANT *Body
);
```


```JScript

vtResponseBody = WinHttpRequest.ResponseBody
```





## <a name="property-value"></a>Значение свойства

Значение **типа Variant** , которое получает тело сущности ответа в виде массива беззнаковых байтов. Этот массив содержит необработанные данные, полученные непосредственно с сервера.

## <a name="error-codes"></a>Коды ошибок

В случае успешного выполнения возвращается значение **S \_** , а в противном случае — значение ошибки.

## <a name="remarks"></a>Remarks

Это свойство возвращает данные ответа в массиве беззнаковых байтов. Если ответ не имеет текста ответа, возвращается пустой вариант. Это свойство может быть вызвано только после вызова метода [**Send**](iwinhttprequest-send.md) .

> [!Note]  
> дополнительные сведения о реализации Windows XP и Windows 2000 см. в разделе [требования к времени выполнения](winhttp-start-page.md).

 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows XP, Windows 2000 Professional с SP3 \[ только для настольных приложений\]<br/>            |
| Минимальная версия сервера<br/> | Windows сервер 2003, Windows 2000 server с пакетом обновления 3 (SP3), \[ только классические приложения\]<br/>         |
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

[**ResponseStream**](iwinhttprequest-responsestream.md)
</dt> <dt>

[**респонсетекст**](iwinhttprequest-responsetext.md)
</dt> <dt>

[Версии WinHTTP](winhttp-versions.md)
</dt> </dl>

 

 




