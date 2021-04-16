---
description: Выполняет запрос для получения событий. Вызов немедленно возвращает значение.
ms.assetid: 3e1bb428-5395-4e90-9713-6d96242fef4e
ms.tgt_platform: multiple
title: SWbemServices.Exeметод Кнотификатионкуери (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.ExecNotificationQuery
- ISWbemServices.ExecNotificationQuery
- ISWbemServices.ExecNotificationQuery
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 44279d16e180d776dc4433c6d5246eab2419fca6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712102"
---
# <a name="swbemservicesexecnotificationquery-method"></a>SWbemServices.Exeметод Кнотификатионкуери

Метод **ексекнотификатионкуери** объекта [**SwbemServices**](swbemservices.md) выполняет запрос для получения событий. Вызов немедленно возвращает значение. Пользователь может опросить возвращенный перечислитель для событий по мере их поступления.

Метод вызывается в режиме семисинчронаус. Дополнительные сведения см. [в разделе вызов метода](calling-a-method.md).

Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Синтаксис


```VB
objwbemEventsource = .ExecNotificationQuery( _
  ByVal strQuery, _
  [ ByVal strQueryLanguage ], _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ] _
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*стркуери* 
</dt> <dd>

Обязательный. Строка, содержащая текст запроса, связанного с событием. Этот параметр не может быть пустым. Дополнительные сведения о создании строк запросов WMI см. в разделе [запросы с помощью WQL](querying-with-wql.md) и Справочник по [WQL](wql-sql-for-wmi.md) .

</dd> <dt>

*стркуерилангуаже* \[ используемых\]
</dt> <dd>

Строка, содержащая используемый язык запросов. Если указано, это значение должно быть "WQL".

</dd> <dt>

*ифлагс* \[ используемых\]
</dt> <dd>

Это целое число, определяющее поведение запроса. Значение по умолчанию — **вбемфлагретурниммедиатели**  +  **вбемфлагфорвардонли**. Если указан этот параметр, для этого параметра необходимо задать значение **вбемфлагретурниммедиатели** и **вбемфлагфорвардонли** , иначе вызов завершится неудачей. Этот параметр может принимать следующие значения.

<dt>

<span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>

<span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>Вбемфлагфорвардонли * * * * (32 (0x20))


</dt> <dd>

Вызывает возврат перечислителя "только вперед". Перечислители "только вперед" обычно выполняются гораздо быстрее и используют меньше памяти, чем обычные перечислители, но они не допускают вызовов [**SWbemObject. Clone \_**](swbemobject-clone-.md).

</dd> <dt>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>Вбемфлагретурниммедиатели * * * * (16 (0x10))


</dt> <dd>

Приводит к немедленному возврату вызова.

</dd> </dl> </dd> <dt>

*обжвбемнамедвалуесет* \[ используемых\]
</dt> <dd>

Как правило, это не определено. В противном случае это объект [**свбемнамедвалуесет**](swbemnamedvalueset.md) , элементы которого представляют сведения о контексте, которые могут использоваться поставщиком, обслуживающим запрос. Поставщик, который поддерживает или требует такую информацию, должен документировать распознанные имена значений, тип данных значения, допустимые значения и семантику.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если ошибка не возникает, этот метод возвращает объект [**свбемевентсаурце**](swbemeventsource.md) . Вы можете вызвать метод [**свбемевентсаурце. некстевент**](swbemeventsource-nextevent.md) , чтобы получить события по мере их поступления.

## <a name="error-codes"></a>Коды ошибок

После завершения метода **ексекнотификатионкуери** объект [Err](/previous-versions//sbf5ze0e(v=vs.85)) может содержать один из кодов ошибок из следующего списка.

<dl> <dt>

**вбемерракцессдениед** -2147749891 (0x80041003)
</dt> <dd>

Текущий пользователь не имеет права на Просмотр результирующего набора.

</dd> <dt>

**вбемеррфаилед** -2147749889 (0x80041001)
</dt> <dd>

Незаданная ошибка.

</dd> <dt>

**вбемерринвалидпараметер** -2147749896 (0x80041008)
</dt> <dd>

Указан недопустимый параметр.

</dd> <dt>

**вбемерринвалидкуери** -2147749911 (0x80041017)
</dt> <dd>

Недопустимый синтаксис запроса.

</dd> <dt>

**вбемерринвалидкуеритипе** -2147749912 (0x80041018)
</dt> <dd>

Запрошенный язык запросов не поддерживается.

</dd> <dt>

**вбемерраутофмемори** -2147749894 (0x80041006)
</dt> <dd>

Недостаточно памяти для завершения операции.

</dd> </dl>

## <a name="remarks"></a>Комментарии

В отличие от метода [**SWbemServices.Exeккуерясинк**](swbemservices-execqueryasync.md) , **ексекнотификатионкуери** возвращает объекты типа события, которые создаются в будущих событиях, а не в существующих объектах. Объекты событий, **ексекнотификатионкуери** запросы, могут быть встроенными (например, [**\_ \_ инстанцекреатионевент**](--instancecreationevent.md)) или внешние (например, события поставщика реестра, такие как [**регистрикэйчанжеевент**](/previous-versions/windows/desktop/regprov/registrykeychangeevent) или SNMP). Дополнительные сведения см. в разделе [Определение типа события для получения](determining-the-type-of-event-to-receive.md) и [получения уведомлений о событиях](receiving-event-notifications.md).

Существует ряд ограничений на количество ключевых слов **and** и **or** , которые могут использоваться в запросах WQL. Большое количество ключевых слов WQL, используемых в сложном запросе, может привести к тому, что WMI вернет код ошибки **\_ \_ \_ нарушения квоты WBEM E** как значение **HRESULT** . Ограничение ключевых слов WQL зависит от того, насколько сложным является запрос.

## <a name="examples"></a>Примеры

В следующем примере кода VBScript отслеживаются изменения в томах на локальном компьютере. Обратите внимание, что [**Win32 \_ волумечанжеевент**](/windows/desktop/CIMWin32Prov/win32-volumechangeevent) — это внешнее событие, определяемое поставщиком, а не встроенное событие, определяемое WMI. Дополнительные сведения см. [в разделе Определение типа получаемого события](determining-the-type-of-event-to-receive.md).


```VB
Set colMonitoredEvents = _
   GetObject("Winmgmts:").ExecNotificationQuery_
      ("Select * from Win32_VolumeChangeEvent")

Do While i = 0
   Set strLatestEvent = colMonitoredEvents.NextEvent
   Wscript.Echo strLatestEvent.DriveName & "Time Created = " _
      & strLatestEvent.Time_Created

    Select Case strLatestEvent.EventType 
       Case 1        
            WScript.Echo "EventType = Configuration Changed"
       Case 2
            WScript.Echo "EventType = Device Arrival"
       Case 3
            WScript.Echo "EventType = Device Removal"
       Case 4
            WScript.Echo "EventType = Docking"

       Case Else
            WScript.Echo "Unrecognized EventType"
       End Select
Loop
```



В следующем примере кода VBScript отслеживается Удаление процесса. При удалении процесса в диспетчере задач или закрытии приложения сценарий отображает сообщение. Обратите внимание, что этот скрипт запрашивает внутреннее событие, определенное WMI- [**\_ \_ инстанцеделетионевент**](--instancedeletionevent.md).


```VB
Set objWMIService = GetObject( _
    "Winmgmts:{impersonationLevel=impersonate}" )
Set colMonitoredProcesses = _
    objWMIService.ExecNotificationQuery( _
    "SELECT * FROM __InstanceDeletionEvent WITHIN 10 WHERE " _
    & "TargetInstance ISA 'Win32_Process'")
i = 0
Do While i < 11
    Set strLatestProcess = colMonitoredProcesses.NextEvent
    WScript.Echo strLatestProcess.TargetInstance.Name
    WScript.Sleep 10000
    i= i + 1
Loop
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Библиотека типов<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | \_SWBEMSERVICES CLSID<br/>                                                         |
| IID<br/>                      | IID \_ исвбемсервицес<br/>                                                          |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**SWbemServices**](swbemservices.md)
</dt> <dt>

[**Свбемевентсаурце. Некстевент**](swbemeventsource-nextevent.md)
</dt> <dt>

[**SWbemServices.ExeКкуери**](swbemservices-execquery.md)
</dt> <dt>

[Получение события WMI](receiving-a-wmi-event.md)
</dt> <dt>

[Запросы с помощью WQL](querying-with-wql.md)
</dt> <dt>

[WQL (SQL для WMI)](wql-sql-for-wmi.md)
</dt> <dt>

[Определение типа получаемого события](determining-the-type-of-event-to-receive.md)
</dt> </dl>

 

