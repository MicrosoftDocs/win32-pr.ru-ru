---
description: предоставляет события для служб Microsoft Windows HTTP (WinHTTP).
ms.assetid: 0721d7f9-2e84-41a9-be52-89c8d638eb90
title: Интерфейс Ивинхттпрекуестевентс
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWinHttpRequestEvents
api_type:
- COM
api_location:
- HttpRequest.idl
ms.openlocfilehash: 42b8355de57ada064e57a129c77ba507a72028b1c38ce115e58db110f2ce976b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117744352"
---
# <a name="iwinhttprequestevents-interface"></a>Интерфейс Ивинхттпрекуестевентс

интерфейс **ивинхттпрекуестевентс** предоставляет события для [служб Microsoft Windows HTTP (WinHTTP)](about-winhttp.md). В нем используются только методы событий.

## <a name="members"></a>Элементы

Интерфейс **ивинхттпрекуестевентс** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **Ивинхттпрекуестевентс** также имеет следующие типы членов:

-   [Методы](#methods)

### <a name="methods"></a>Методы

Интерфейс **ивинхттпрекуестевентс** содержит следующие методы.



| Метод                                                                           | Описание                                                          |
|:---------------------------------------------------------------------------------|:---------------------------------------------------------------------|
| [**OnError**](iwinhttprequestevents-onerror.md)                                 | Происходит при возникновении ошибки времени выполнения в приложении.<br/> |
| [**онреспонседатааваилабле**](iwinhttprequestevents-onresponsedataavailable.md) | Происходит при доступе к данным из ответа.<br/>          |
| [**онреспонсефинишед**](iwinhttprequestevents-onresponsefinished.md)           | Происходит при завершении данных ответа.<br/>                |
| [**онреспонсестарт**](iwinhttprequestevents-onresponsestart.md)                 | Происходит при начале получения данных ответа.<br/>      |



 

## <a name="remarks"></a>Remarks

В следующей процедуре описывается регистрация для получения уведомлений.

1.  Получите интерфейс [IConnectionPointContainer](/windows/win32/api/ocidl/nn-ocidl-iconnectionpointcontainer) путем вызова **QueryInterface** для объекта [**ивинхттпрекуест**](iwinhttprequest-interface.md) .
2.  Вызовите [финдконнектионпоинт](/windows/win32/api/ocidl/nf-ocidl-iconnectionpointcontainer-findconnectionpoint) в возвращенном интерфейсе и передайте **IID \_ ивинхттпрекуестевентс** в *riid*.
3.  Вызовите [advise](/windows/win32/api/ocidl/nf-ocidl-iconnectionpoint-advise) в возвращенной точке соединения и передайте указатель на интерфейс **IUnknown** для объекта, который реализует **ивинхттпрекуестевентс** для *Punk*.

Уведомления могут быть завершены путем вызова команды [unadvise](/windows/win32/api/ocidl/nf-ocidl-iconnectionpoint-unadvise) на точке соединения, возвращенной на шаге 2.

Чтобы просмотреть код, регистрирующий для COM-уведомлений, см. раздел клиент в статье [точки подключения COM](/archive/msdn-magazine/2007/september/clr-inside-out-com-connection-points) .

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

[**ивинхттпрекуест**](iwinhttprequest-interface.md)
</dt> <dt>

[Версии WinHTTP](winhttp-versions.md)
</dt> </dl>

 

