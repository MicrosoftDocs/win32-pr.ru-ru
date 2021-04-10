---
description: Инструментарий WMI содержит инфраструктуру событий, которая создает уведомления об изменениях в данных и службах WMI. Классы событий WMI предоставляют уведомления при возникновении конкретных событий.
ms.assetid: 347808a7-0f7b-4687-93f4-bea55c96795a
ms.tgt_platform: multiple
title: Получение события WMI
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 255f54f78bb64659d1cd07eddb72eae55b0263c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155862"
---
# <a name="receiving-a-wmi-event"></a>Получение события WMI

Инструментарий WMI содержит инфраструктуру событий, которая создает уведомления об изменениях в данных и службах WMI. [*Классы событий*](gloss-e.md) WMI предоставляют уведомления при возникновении конкретных событий.

В этом разделе обсуждаются следующие разделы:

-   [Запросы событий](#event-queries)
-   [Пример](#example)
-   [Потребители событий](#event-consumers)
-   [Предоставление событий](#providing-events)
-   [Квоты подписки](#subscription-quotas)
-   [См. также](#related-topics)

## <a name="event-queries"></a>Запросы событий

Можно создать [семисинчронаус](receiving-synchronous-and-semisynchronous-event-notifications.md) или [**асинхронный**](receiving-asynchronous-event-notifications.md) запрос для отслеживания изменений в журналах событий, создания процессов, состояния службы, доступности компьютера или свободного места на диске, а также других сущностях или событиях. В сценариях для подписки на события используется метод [**SWbemServices.Exeкнотификатионкуери**](swbemservices-execnotificationquery.md) . В C++ используется [**IWbemServices:: ексекнотификатионкуери**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery) . Дополнительные сведения см. [в разделе вызов метода](calling-a-method.md).

Уведомление об изменении в стандартной модели данных WMI называется [*встроенным событием*](gloss-i.md). [**\_ \_ Инстанцекреатионевент**](--instancecreationevent.md) или [**\_ \_ намеспацеделетионевент**](--namespacedeletionevent.md) являются примерами встроенных событий. Уведомление об изменении, которое поставщик делает для определения события поставщика, называется [*внешние события*](gloss-e.md). Например, поставщик [системного реестра](/previous-versions/windows/desktop/regprov/system-registry-provider), [поставщик событий управления питанием](/windows/desktop/CIMWin32Prov/power-management-event-provider)и [поставщик Win32](/windows/desktop/CIMWin32Prov/win32-provider) определяют собственные события. Дополнительные сведения см. [в разделе Определение типа получаемого события](determining-the-type-of-event-to-receive.md).

## <a name="example"></a>Пример

Следующий пример кода скрипта является запросом для встроенного [**\_ \_ инстанцекреатионевент**](--instancecreationevent.md) класса событий [**Win32 \_ нтложевент**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogevent). Вы можете запустить эту программу в фоновом режиме и при наличии события появится сообщение. Если закрыть диалоговое окно **Ожидание событий** , программа прекратит ожидание событий. Имейте в виду, что параметр **SeSecurityPrivilege** должен быть включен.


```VB
Sub SINK_OnObjectReady(objObject, objAsyncContext)
    WScript.Echo (objObject.TargetInstance.Message)
End Sub

Set objWMIServices = GetObject( _
    "WinMgmts:{impersonationLevel=impersonate, (security)}") 

' Create the event sink object that receives the events
Set sink = WScript.CreateObject("WbemScripting.SWbemSink","SINK_")
 
' Set up the event selection. SINK_OnObjectReady is called when
' a Win32_NTLogEvent event occurs
objWMIServices.ExecNotificationQueryAsync sink,"SELECT * FROM __InstanceCreationEvent " & "WHERE TargetInstance ISA 'Win32_NTLogEvent' "

WScript.Echo "Waiting for events"
```


```PowerShell

# Define event Query
$query = "SELECT * FROM __InstanceCreationEvent 
          WHERE TargetInstance ISA 'Win32_NTLogEvent' "

<# Register for event - also specify an action that
displays the log event when the event fires.#>

Register-WmiEvent -Source Demo1 -Query $query -Action {
                Write-Host "Log Event occured"
                $global:myevent = $event
                Write-Host "EVENT MESSAGE"
                Write-Host $event.SourceEventArgs.NewEvent.TargetInstance.Message}
<# So wait #>
"Waiting for events"
```





В следующем примере кода VBScript показано [ \_ \_ события registryvaluechangeevent](registering-for-system-registry-events.md) внешних событий, определяемое поставщиком реестра. Скрипт создает временный потребитель с помощью вызова [**SWbemServices.Exeкнотификатионкуерясинк**](swbemservices-execnotificationqueryasync.md)и получает события только при выполнении скрипта. Следующий скрипт выполняется неограниченно до перезагрузки компьютера, Инструментарий WMI остановлен или сценарий остановлен. Чтобы прерывать выполнение скрипта вручную, используйте диспетчер задач, чтобы прерывать процесс. Чтобы остановить его программно, используйте метод [**Terminate**](/windows/desktop/CIMWin32Prov/terminate-method-in-class-win32-process) в \_ классе процесса Win32. Дополнительные сведения см. [в разделе Настройка безопасности при асинхронном вызове](setting-security-on-an-asynchronous-call.md).


```VB
strComputer = "."

Set objWMIServices=GetObject( _
    "winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\default")

set objSink = WScript.CreateObject("WbemScripting.SWbemSink","SINK_")


objWMIServices.ExecNotificationQueryAsync objSink, _
    "Select * from RegistryValueChangeEvent Where Hive = 'HKEY_LOCAL_MACHINE' and KeyPath = 'SYSTEM\\ControlSet001\\Control' and ValueName = 'CurrentUser'"

WScript.Echo "Waiting for events..."

While (True) 
     WScript.Sleep (1000)
Wend

 
WScript.Echo "Listening for Registry Change Events..." & vbCrLf 

While(True) 
    WScript.Sleep 1000 
Wend 

Sub SINK_OnObjectReady(wmiObject, wmiAsyncContext) 
    WScript.Echo "Received Registry Value Change Event" & vbCrLf & wmiObject.GetObjectText_() 
End Sub
```



## <a name="event-consumers"></a>потребители событий

Вы можете отслеживать или использовать события с помощью следующих потребителей во время выполнения скрипта или приложения:

-   Получатели временных событий

    [*Временный потребитель*](gloss-t.md) — это клиентское приложение WMI, которое получает WMI-событие. WMI включает уникальный интерфейс, который используется для указания событий WMI для отправки в клиентское приложение. Временный потребитель событий считается временным, так как он работает только в том случае, если он специально загружен пользователем. Дополнительные сведения см. [в статье получение событий в](receiving-events-for-the-duration-of-your-application.md)течение всего приложения.

-   Потребители постоянных событий

    [*Постоянный потребитель*](gloss-p.md) — это COM-объект, который может все время получить событие WMI. Постоянный потребитель событий использует набор постоянных объектов и фильтров для записи событий WMI. Как и временный потребитель событий, вы настраиваете ряд объектов WMI и фильтров, которые захватывают событие WMI. Когда происходит событие, соответствующее фильтру, Инструментарий WMI загружает постоянный потребитель событий и уведомляет его о событии. Поскольку Постоянный потребитель реализуется в репозитории WMI и является исполняемым файлом, зарегистрированным в WMI, постоянный потребитель событий работает и получает события после его создания и даже после перезагрузки операционной системы при условии, что инструментарий WMI запущен. Дополнительные сведения см. [в разделе Получение событий в любое время](receiving-events-at-all-times.md).

Сценарии или приложения, получающие события, имеют особые соображения безопасности. Дополнительные сведения см. в разделе [Защита событий WMI](securing-wmi-events.md).

Приложение или сценарий может использовать встроенный поставщик событий WMI, предоставляющий [стандартные классы потребителей](standard-consumer-classes.md). Каждый стандартный класс-потребитель реагирует на событие с другим действием, отправляя сообщение электронной почты или выполняя сценарий. Нет необходимости писать код поставщика, чтобы использовать стандартный класс потребителя для создания постоянного потребителя событий. Дополнительные сведения см. [в разделе Мониторинг и реагирование на события с помощью стандартных потребителей](monitoring-and-responding-to-events-with-standard-consumers.md).

## <a name="providing-events"></a>Предоставление событий

Поставщик событий — это COM-компонент, который отправляет событие в WMI. Можно создать поставщик событий для отправки события в приложении C++ или C#. Большинство поставщиков событий управляют объектом для WMI, например, приложением или элементом оборудования. Дополнительные сведения см. в разделе [запись поставщика событий](writing-an-event-provider.md).

Событие времени или повторение — это событие, возникающее в предопределенном времени.

Инструментарий WMI предоставляет следующие возможности для создания событий с временными или повторяющимися событиями для приложений.

-   Стандартная инфраструктура событий Майкрософт.
-   Специализированный класс Timer.

Дополнительные сведения см. [в разделе Получение события с превышением времени или повтора](receiving-a-timed-or-repeating-event.md). При написании поставщика событий учитывайте сведения о безопасности, [указанные в этой](providing-events-securely.md)области.

Рекомендуется компилировать постоянные подписки на события в \\ \\ пространство имен корневой подписки. Дополнительные сведения см. в разделе [Реализация постоянных подписок на события между пространствами имен](implementing-cross-namespace-permanent-event-subscriptions.md).

## <a name="subscription-quotas"></a>Квоты подписки

Опрос событий может снизить производительность для поставщиков, которые поддерживают запросы к огромным наборам данных. Кроме того, любой пользователь, имеющий доступ на чтение к пространству имен с динамическими поставщиками, может выполнять атаку типа "отказ в обслуживании" (DoS). WMI поддерживает квоты для всех пользователей в сочетании и для каждого потребителя событий в одном экземпляре [**\_ \_ арбитраторконфигуратион**](--arbitratorconfiguration.md) , расположенном в \\ корневом пространстве имен. Эти квоты являются глобальными, а не для каждого пространства имен. Квоты изменить нельзя.

В настоящее время Инструментарий WMI применяет квоты с помощью свойств [**\_ \_ арбитраторконфигуратион**](--arbitratorconfiguration.md). Каждая квота имеет каждого пользователя и общую версию, включающую всех пользователей в сочетании, а не на пространство имен. В следующей таблице перечислены квоты, которые применяются к свойствам **\_ \_ арбитраторконфигуратион** .



| Общее/изучение                                                                   | Quota                                                                       |
|---------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| темпорарисубскриптионстотал<br/> темпорарисубскриптионсперусер<br/> | 10 000<br/> 1000<br/>                                          |
| перманентсубскриптионстотал<br/> перманентсубскриптионсперусер<br/> | 10 000<br/> 1000<br/>                                          |
| поллингинструктионстотал<br/> поллингинструктионсперусер<br/>       | 10 000<br/> 1000<br/>                                          |
| поллингмеморитотал<br/> поллингмемориперусер<br/>                   | 10 000 000 (0x989680) байт<br/> 5 000 000 (0x4CB40) байт<br/> |



 

Администратор или пользователь с разрешением " **полный доступ на \_ запись** " в пространстве имен может изменить одноэлементный экземпляр [**\_ \_ арбитраторконфигуратион**](--arbitratorconfiguration.md). WMI отслеживает квоту для каждого пользователя.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Использование инструментария WMI](using-wmi.md)
</dt> </dl>

 

