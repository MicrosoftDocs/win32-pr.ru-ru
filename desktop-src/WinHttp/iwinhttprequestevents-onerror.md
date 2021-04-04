---
description: Происходит при возникновении ошибки времени выполнения в приложении.
ms.assetid: d99400a4-3661-4162-bfd6-8c2a27e0f328
title: 'Событие Ивинхттпрекуестевентс:: OnError'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8582deec90eb6bfc2985460f3127d5c7ee9c01b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999451"
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

## <a name="remarks"></a>Комментарии

> [!Note]  
> Для Windows XP и Windows 2000 см. раздел [требования к времени выполнения](winhttp-start-page.md) на начальной странице WinHTTP.

 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows XP, Windows 2000 Professional с пакетом обновления 3 (SP3), \[ только классические приложения\]<br/>            |
| Минимальная версия сервера<br/> | Windows Server 2003, Windows 2000 Server с пакетом обновления 3 (SP3), \[ только классические приложения\]<br/>         |
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

 

 




