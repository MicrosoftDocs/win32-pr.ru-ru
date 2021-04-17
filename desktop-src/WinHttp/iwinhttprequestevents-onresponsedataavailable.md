---
description: Происходит при доступе к данным из ответа.
ms.assetid: 62d02e3b-466a-4d3d-994b-0a1ae12049e1
title: 'Событие Ивинхттпрекуестевентс:: Онреспонседатааваилабле'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41cb2fbc680b1f6739a66bb68565188c8a5d78b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105673957"
---
# <a name="iwinhttprequesteventsonresponsedataavailable-event"></a>Событие Ивинхттпрекуестевентс:: Онреспонседатааваилабле

Событие **онреспонседатааваилабле** возникает при доступе к данным из ответа.

## <a name="syntax"></a>Синтаксис


```C++
void OnResponseDataAvailable(
  [in] SAFEARRAY(unsigned char) *Data
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Данные* \[ окне\]
</dt> <dd>

Отсчитываемый от нуля массив байтов, который получает данные ответа, полученные службами Microsoft Windows HTTP (WinHTTP) вплоть до момента возникновения этого события. Это **вариант** типа VT \_ array \| VT \_ UI1.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Это событие не возвращает значение.

## <a name="remarks"></a>Комментарии

Поскольку данные находятся в байтах, их необходимо преобразовать в широкие символы при помещении в строку расширенных символов (Юникод).

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

 

 




