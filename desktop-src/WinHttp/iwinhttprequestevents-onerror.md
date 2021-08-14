---
description: Происходит при возникновении ошибки времени выполнения в приложении.
ms.assetid: d99400a4-3661-4162-bfd6-8c2a27e0f328
title: 'Событие Ивинхттпрекуестевентс:: OnError'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31127dcc3155b804bbda1c3ab94ee8a410c73f5a96c3ecfc6f787479ccd51539
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117744342"
---
# <a name="iwinhttprequesteventsonerror-event"></a>Событие Ивинхттпрекуестевентс:: OnError

Событие **OnError** возникает при возникновении ошибки времени выполнения в приложении.

## <a name="syntax"></a>Синтаксис


```C++
void OnError(
  [in] long ErrorNumber,
  [in] BSTR ErrorDescription
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Номер ошибки* \[ окне\]
</dt> <dd>

Получает числовое значение ошибки. Младшие 16 разрядов этого номера ошибки соответствуют одной из ошибок, перечисленных в [**сообщениях об ошибках**](error-messages.md).

</dd> <dt>

*ErrorDescription* \[ окне\]
</dt> <dd>

Указывает краткое описание возникшей ошибки.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Это событие не возвращает значение.

## <a name="remarks"></a>Remarks

> [!Note]  
> сведения о Windows XP и Windows 2000 см. в разделе [требования к времени выполнения](winhttp-start-page.md) на начальной странице WinHTTP.

 

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows XP, Windows 2000 Professional с SP3 \[ только для настольных приложений\]<br/>            |
| Минимальная версия сервера<br/> | Windows сервер 2003, Windows 2000 server с пакетом обновления 3 (SP3), \[ только классические приложения\]<br/>         |
| Распространяемые компоненты<br/>          | WinHTTP 5,0 и Internet Explorer 5,01 или более поздней версии в Windows XP и Windows 2000.<br/> |
| IDL<br/>                      | <dl> <dt>HttpRequest. idl</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ивинхттпрекуестевентс**](iwinhttprequestevents-interface.md)
</dt> <dt>

[**WinHttpRequest**](winhttprequest.md)
</dt> <dt>

[Версии WinHTTP](winhttp-versions.md)
</dt> </dl>

 

 




