---
description: Выполняет запрос для получения событий.
ms.assetid: 0b0e8313-4ffd-4d4a-8965-d2c6743e7573
ms.tgt_platform: multiple
title: SWbemServices.Exeметод Кнотификатионкуерясинк (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.ExecNotificationQueryAsync
- ISWbemServices.ExecNotificationQueryAsync
- ISWbemServices.ExecNotificationQueryAsync
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 8e2ecddf290d83583b3108620b8b4bb23be7c957
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711624"
---
# <a name="swbemservicesexecnotificationqueryasync-method"></a>SWbemServices.Exeметод Кнотификатионкуерясинк

Метод **ExecNotificationQueryAsync** объекта [**SwbemServices**](swbemservices.md) выполняет запрос для получения событий. Этот вызов возвращает немедленно, а результаты и состояние возвращаются вызывающему через события, доставляемые в приемник, указанный в *обжвбемсинк*.

События, указанные в запросе, могут быть встроенными событиями инструментарий управления Windows (WMI) (WMI), такими как [**\_ \_ инстанцекреатионевент**](--instancecreationevent.md)или внешние события, такие как [**Win32 \_ IP4RouteTableEvent**](/previous-versions/windows/desktop/wmiiprouteprov/win32-ip4routetableevent) или [**регистрикэйчанжеевент**](/previous-versions/windows/desktop/regprov/registrykeychangeevent). Дополнительные сведения см. [в разделе Определение типа получаемого события](determining-the-type-of-event-to-receive.md).

Метод вызывается в асинхронном режиме. Дополнительные сведения см. [в разделе вызов метода](calling-a-method.md).

Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Синтаксис


```VB
SWbemServices.ExecNotificationQueryAsync( _
  ByVal objWbemSink, _
  ByVal strQuery, _
  [ ByVal strQueryLanguage ], _
  [ ByVal iFlags ], _
  [ ByVal objwbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*обжвбемсинк* 
</dt> <dd>

Обязательный. Приемник объекта, который асинхронно получает уведомления о событиях. Создайте объект [**свбемсинк**](swbemsink.md) для получения объектов.

</dd> <dt>

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

Целое число, определяющее поведение запроса. Для этого параметра можно задать следующие значения.

<dt>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>Вбемфлагсендстатус * * * * (128 (0x80))


</dt> <dd>

Вызывает асинхронные вызовы для отправки обновлений состояния обработчику событий [**OnProgress**](swbemsink-onprogress.md) для приемника объекта.

</dd> <dt>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>Вбемфлагдонтсендстатус * * * * (0 (0x0))


</dt> <dd>

Не позволяет асинхронным вызовам отправлять обновления состояния в обработчик событий [**OnProgress**](swbemsink-onprogress.md) для приемника объекта.

</dd> </dl> </dd> <dt>

*обжвбемнамедвалуесет* \[ используемых\]
</dt> <dd>

Как правило, это не определено. В противном случае это объект [**свбемнамедвалуесет**](swbemnamedvalueset.md) , элементы которого представляют сведения о контексте, которые могут использоваться поставщиком, который служб запрашивает. Поставщик, который поддерживает или требует такую информацию, должен документировать распознанные имена значений, тип данных значения, допустимые значения и семантику.

</dd> <dt>

*обжвбемасинкконтекст* \[ используемых\]
</dt> <dd>

Это объект [**свбемнамедвалуесет**](swbemnamedvalueset.md) , который возвращает приемнику объекта, чтобы узнать источник исходного асинхронного вызова. Этот параметр используется для выполнения нескольких асинхронных вызовов с использованием одного и того же приемника объекта. Чтобы использовать этот параметр, создайте объект **свбемнамедвалуесет** и используйте метод [**свбемнамедвалуесет. Add**](swbemnamedvalueset-add.md) , чтобы добавить значение, идентифицирующее выполняемый асинхронный вызов. Объект **свбемнамедвалуесет** возвращается в приемник объекта, и источник вызова можно извлечь с помощью метода [**свбемнамедвалуесет. Item**](swbemnamedvalueset-item.md) . Дополнительные сведения см. [в разделе вызов метода](calling-a-method.md).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение. В случае успешного выполнения приемник получает событие [**онобжектреади**](swbemsink-onobjectready.md) для каждого экземпляра. После последнего экземпляра приемник объекта получает событие [**Oncompleteed**](swbemsink-oncompleted.md) .

## <a name="error-codes"></a>Коды ошибок

После завершения метода **ExecNotificationQueryAsync** объект [Err](/previous-versions//sbf5ze0e(v=vs.85)) может содержать один из кодов ошибок, указанных в следующем списке.

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

Метод **ExecNotificationQueryAsync** возвращает объекты типа события, создаваемые будущими событиями. Объекты событий, **ExecNotificationQueryAsync** запросы, могут быть встроенными (например, [**\_ \_ инстанцекреатионевент**](--instancecreationevent.md)) или внешние (например, события [**регистрикэйчанжеевент**](/previous-versions/windows/desktop/regprov/registrykeychangeevent) или SNMP). Дополнительные сведения см. [в разделе Определение типа получаемого события](determining-the-type-of-event-to-receive.md).

Вызов **ExecNotificationQueryAsync** немедленно возвращает значение. Запрошенные объекты и состояние возвращаются вызывающему объекту через обратные вызовы, доставляемые в приемник, указанный в *обжвбемсинк*. Чтобы обработать каждый объект при его возвращении, создайте *обжвбемсинк*. Подпрограммы события [**онобжектреади**](swbemsink-onobjectready.md) . После возврата всех объектов выполните окончательную обработку для реализации *обжвбемсинк*. Событие [**Oncompleteed**](swbemsink-oncompleted.md) .

Асинхронный обратный вызов позволяет пользователю без проверки подлинности предоставлять данные в приемник. Это создает угрозы безопасности для сценариев и приложений. Сведения об устранении рисков см. в разделе [Настройка безопасности при асинхронном вызове](setting-security-on-an-asynchronous-call.md).

Существует ряд ограничений на количество ключевых слов **and** и **or** , которые могут использоваться в запросах WQL. Большое количество ключевых слов WQL, используемых в сложном запросе, может привести к тому, что инструментарий WMI возвращает значение **HRESULT** с кодом ошибки **\_ \_ \_ нарушения квоты E** Асан. Ограничение ключевых слов WQL зависит от того, насколько сложным является запрос.

## <a name="examples"></a>Примеры

В следующем примере кода VBScript показан скрипт, ожидающий уведомления о событии WMI, указывающий на завершение процесса. Он ожидает встроенного события WMI, экземпляра класса событий [**\_ \_ инстанцеделетионевент**](--instancedeletionevent.md). **\_ \_ Инстанцеделетионевент** должен представлять удаление экземпляра [**\_ процесса Win32**](/windows/desktop/CIMWin32Prov/win32-process). Дополнительные сведения о встроенных событиях WMI см. [в разделе Определение типа получаемого события](determining-the-type-of-event-to-receive.md).

Следующий скрипт выполняется неограниченно до перезагрузки компьютера, Инструментарий WMI остановлен или сценарий остановлен. Чтобы прерывать выполнение скрипта вручную, используйте диспетчер задач, чтобы прерывать процесс. Чтобы остановить его программно, используйте метод [**Terminate**](/windows/desktop/CIMWin32Prov/terminate-method-in-class-win32-process) в \_ классе процесса Win32.


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:\\" & _strComputer & "\root\CIMV2") 
Set MySink = WScript.CreateObject("WbemScripting.SWbemSink","SINK_")

objWMIservice.ExecNotificationQueryAsync MySink, "SELECT * FROM __InstanceCreationEvent WITHIN 1 " _
                                               & "WHERE TargetInstance ISA 'Win32_Process'"

WScript.Echo "Waiting for events..."

While (True)
    Wscript.Sleep(1000)
Wend

Sub SINK_OnObjectReady(objObject, objAsyncContext)
    WScript.Echo "Event occurred."
End Sub

Sub SINK_OnCompleted(objObject, objAsyncContext)
    WScript.Echo "Event call complete."
End Sub
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

[**SWbemServices.ExeКкуери**](swbemservices-execquery.md)
</dt> <dt>

[**SWbemServices.ExeКкуерясинк**](swbemservices-execqueryasync.md)
</dt> <dt>

[Регистрация для событий системного реестра](registering-for-system-registry-events.md)
</dt> <dt>

[Определение типа получаемого события](determining-the-type-of-event-to-receive.md)
</dt> <dt>

[Вызов метода](calling-a-method.md)
</dt> <dt>

[Настройка безопасности при асинхронном вызове](setting-security-on-an-asynchronous-call.md)
</dt> </dl>

 

