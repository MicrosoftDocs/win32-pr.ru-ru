---
description: Объект Свбемевентсаурце извлекает события из запроса события в сочетании с SWbemServices.ExeКнотификатионкуери.
ms.assetid: 7efd5e6a-4311-4d20-8b05-e9208eec098a
ms.tgt_platform: multiple
title: Объект Свбемевентсаурце (Wbemdisp. h)
ms.topic: reference
ms.date: 09/25/2020
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemEventSource
- ISWbemEventSource
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 8da55a7b6722c263fe9a3fb0af7a8db07d672e12
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701970"
---
# <a name="swbemeventsource-object"></a>Объект Свбемевентсаурце

Объект **свбемевентсаурце** извлекает события из запроса события в сочетании с [**SWbemServices.Exeкнотификатионкуери**](swbemservices-execnotificationquery.md). При вызове **SWbemServices.Exeкнотификатионкуери** для создания запроса события вы получаете объект **свбемевентсаурце** . Затем можно использовать метод [**некстевент**](swbemeventsource-nextevent.md) для получения событий по мере их поступления. Не удается создать этот объект с [помощью вызова функции](/previous-versions//xzysf6hc(v=vs.85)) VBScript.

## <a name="members"></a>Элементы

Объект **свбемевентсаурце** имеет следующие типы членов:

-   [Методы](#methods)
-   [Свойства](#properties)

### <a name="methods"></a>Методы

Объект **свбемевентсаурце** содержит эти методы.



| Метод                                          | Описание                                                                                                                                  |
|:------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------|
| [**некстевент**](swbemeventsource-nextevent.md) | Используется для получения события в сочетании с [**SWbemServices.Exeкнотификатионкуери**](swbemservices-execnotificationquery.md).<br/> |



 

### <a name="properties"></a>Свойства

Объект **свбемевентсаурце** имеет следующие свойства.



| Свойство                                                    | Тип доступа          | Описание                                              |
|:------------------------------------------------------------|:---------------------|:---------------------------------------------------------|
| [**Безопасность\_**](swbemeventsource-security-.md)<br/> | Только для чтения<br/> | Используется для чтения или изменения параметров безопасности.<br/> |



 

## <a name="examples"></a>Примеры

Этот скрипт использует методы класса **свбемевентсаурце** и класс [**SwbemServices**](swbemservices.md) в сочетании с WQL-запросом для событий приложения. Дополнительные сведения об уведомлениях о событиях WMI и запросах см. в разделе [мониторинг событий](monitoring-events.md), [выполнение сценария на основе события](running-a-script-based-on-an-event.md)и [Получение асинхронных уведомлений о событиях](receiving-asynchronous-event-notifications.md).


```VB
' Connect to WMI, obtaining an SWbemServices object
set svc = _
CreateObject("Wbemscripting.SWbemLocator")._
   ConnectServer(,"root\cimv2")

' Obtain an SWbemEventSource object from the 
' SWbemServices.ExecNotificationQuery method to specify the 
' event source as "Application" events in a Win32_NTLogEvent
set evtsrc = svc.ExecNotificationQuery("SELECT * " _
   & "FROM __InstanceCreationEvent " _
   & "WHERE TargetInstance ISA 'Win32_NTLogEvent'" _
   & "AND TargetInstance.Logfile ='Application'")

' Wait for an event by executing the NextEvent method on the 
' SWbemEventSource object.
while (num < 5)
    set inst = evtsrc.NextEvent(-1)
    Wscript.echo inst.TargetInstance.Logfile
    num = num + 1
wend
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Библиотека типов<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | \_СВБЕМЕВЕНТСАУРЦЕ CLSID<br/>                                                      |
| IID<br/>                      | IID \_ исвбемевентсаурце<br/>                                                       |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Создание скриптов для объектов API](scripting-api-objects.md)
</dt> </dl>

 

