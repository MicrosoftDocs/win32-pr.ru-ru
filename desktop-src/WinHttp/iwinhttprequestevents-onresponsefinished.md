---
description: Происходит при завершении данных ответа.
ms.assetid: 0df2031e-826f-436e-a689-201fa8b5c38f
title: 'Событие Ивинхттпрекуестевентс:: Онреспонсефинишед'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 19d3a596e23028cec0401a21a1ee866ef6e51d9d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702515"
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

## <a name="remarks"></a>Комментарии

Это событие сигнализирует о получении всех данных ответа, относящихся к последнему запросу. [**Онреспонседатааваилабле**](iwinhttprequestevents-onresponsedataavailable.md) не повторяется до следующего запроса.

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

 

 




