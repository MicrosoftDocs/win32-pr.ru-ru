---
description: Происходит при доступе к данным из ответа.
ms.assetid: 62d02e3b-466a-4d3d-994b-0a1ae12049e1
title: 'Событие Ивинхттпрекуестевентс:: Онреспонседатааваилабле'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12b55f87584164a47b47920caf961f02f0bd9cc6596c4c90f76f381027af545e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118114248"
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

отсчитываемый от нуля массив байтов, который получает данные ответа, полученные службами Microsoft Windows HTTP (WinHTTP) вплоть до момента возникновения этого события. Это **вариант** типа VT \_ array \| VT \_ UI1.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Это событие не возвращает значение.

## <a name="remarks"></a>Remarks

Поскольку данные находятся в байтах, их необходимо преобразовать в широкие символы при помещении в строку расширенных символов (Юникод).

> [!Note]  
> сведения о Windows XP и Windows 2000 см. в разделе [требования к времени выполнения](winhttp-start-page.md) на начальной странице WinHTTP.

 

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows XP, Windows 2000 Professional с SP3 \[ только для настольных приложений\]<br/>            |
| Минимальная версия сервера<br/> | Windows сервер 2003, Windows 2000 server с пакетом обновления 3 (SP3), \[ только классические приложения\]<br/>         |
| Распространяемые компоненты<br/>          | WinHTTP 5,0 и Internet Explorer 5,01 или более поздней версии в Windows XP и Windows 2000.<br/> |
| IDL<br/>                      | <dl> <dt>HttpRequest. idl</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**ивинхттпрекуестевентс**](iwinhttprequestevents-interface.md)
</dt> <dt>

[**WinHttpRequest**](winhttprequest.md)
</dt> <dt>

[Версии WinHTTP](winhttp-versions.md)
</dt> </dl>

 

 




