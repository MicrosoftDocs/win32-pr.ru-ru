---
description: Происходит при завершении данных ответа.
ms.assetid: 0df2031e-826f-436e-a689-201fa8b5c38f
title: 'Событие Ивинхттпрекуестевентс:: Онреспонсефинишед'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2114135c17f3e2eb2f9d60a7044f7441271f257fe099de31ea70c6030de769df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117744254"
---
# <a name="iwinhttprequesteventsonresponsefinished-event"></a>Событие Ивинхттпрекуестевентс:: Онреспонсефинишед

Событие **онреспонсефинишед** возникает при завершении данных ответа.

## <a name="syntax"></a>Синтаксис


```C++
void OnResponseFinished();
```



## <a name="parameters"></a>Параметры

У этого события нет параметров.

## <a name="return-value"></a>Возвращаемое значение

Это событие не возвращает значение.

## <a name="remarks"></a>Remarks

Это событие сигнализирует о получении всех данных ответа, относящихся к последнему запросу. [**Онреспонседатааваилабле**](iwinhttprequestevents-onresponsedataavailable.md) не повторяется до следующего запроса.

> [!Note]  
> сведения о Windows XP и Windows 2000 см. в разделе [требования к времени выполнения](winhttp-start-page.md) на начальной странице WinHTTP.

 

## <a name="requirements"></a>Требования



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

 

 




