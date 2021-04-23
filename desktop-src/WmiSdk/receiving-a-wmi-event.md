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
# <a name="receiving-a-wmi-event"></a><span data-ttu-id="93fd5-104">Получение события WMI</span><span class="sxs-lookup"><span data-stu-id="93fd5-104">Receiving a WMI Event</span></span>

<span data-ttu-id="93fd5-105">Инструментарий WMI содержит инфраструктуру событий, которая создает уведомления об изменениях в данных и службах WMI.</span><span class="sxs-lookup"><span data-stu-id="93fd5-105">WMI contains an event infrastructure that produces notifications about changes in WMI data and services.</span></span> <span data-ttu-id="93fd5-106">[*Классы событий*](gloss-e.md) WMI предоставляют уведомления при возникновении конкретных событий.</span><span class="sxs-lookup"><span data-stu-id="93fd5-106">WMI [*event classes*](gloss-e.md) provide notification when specific events occur.</span></span>

<span data-ttu-id="93fd5-107">В этом разделе обсуждаются следующие разделы:</span><span class="sxs-lookup"><span data-stu-id="93fd5-107">The following sections are discussed in this topic:</span></span>

-   [<span data-ttu-id="93fd5-108">Запросы событий</span><span class="sxs-lookup"><span data-stu-id="93fd5-108">Event Queries</span></span>](#event-queries)
-   [<span data-ttu-id="93fd5-109">Пример</span><span class="sxs-lookup"><span data-stu-id="93fd5-109">Example</span></span>](#example)
-   [<span data-ttu-id="93fd5-110">Потребители событий</span><span class="sxs-lookup"><span data-stu-id="93fd5-110">Event Consumers</span></span>](#event-consumers)
-   [<span data-ttu-id="93fd5-111">Предоставление событий</span><span class="sxs-lookup"><span data-stu-id="93fd5-111">Providing Events</span></span>](#providing-events)
-   [<span data-ttu-id="93fd5-112">Квоты подписки</span><span class="sxs-lookup"><span data-stu-id="93fd5-112">Subscription Quotas</span></span>](#subscription-quotas)
-   [<span data-ttu-id="93fd5-113">См. также</span><span class="sxs-lookup"><span data-stu-id="93fd5-113">Related topics</span></span>](#related-topics)

## <a name="event-queries"></a><span data-ttu-id="93fd5-114">Запросы событий</span><span class="sxs-lookup"><span data-stu-id="93fd5-114">Event Queries</span></span>

<span data-ttu-id="93fd5-115">Можно создать [семисинчронаус](receiving-synchronous-and-semisynchronous-event-notifications.md) или [**асинхронный**](receiving-asynchronous-event-notifications.md) запрос для отслеживания изменений в журналах событий, создания процессов, состояния службы, доступности компьютера или свободного места на диске, а также других сущностях или событиях.</span><span class="sxs-lookup"><span data-stu-id="93fd5-115">You can create a [semisynchronous](receiving-synchronous-and-semisynchronous-event-notifications.md) or [**asynchronous**](receiving-asynchronous-event-notifications.md) query to monitor changes to event logs, process creation, service status, computer availability or disk drive free space, and other entities or events.</span></span> <span data-ttu-id="93fd5-116">В сценариях для подписки на события используется метод [**SWbemServices.Exeкнотификатионкуери**](swbemservices-execnotificationquery.md) .</span><span class="sxs-lookup"><span data-stu-id="93fd5-116">In scripting, the [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md) method is used to subscribe to events.</span></span> <span data-ttu-id="93fd5-117">В C++ используется [**IWbemServices:: ексекнотификатионкуери**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery) .</span><span class="sxs-lookup"><span data-stu-id="93fd5-117">In C++, [**IWbemServices::ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery) is used.</span></span> <span data-ttu-id="93fd5-118">Дополнительные сведения см. [в разделе вызов метода](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="93fd5-118">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="93fd5-119">Уведомление об изменении в стандартной модели данных WMI называется [*встроенным событием*](gloss-i.md).</span><span class="sxs-lookup"><span data-stu-id="93fd5-119">Notification of a change in the standard WMI data model is called an [*intrinsic event*](gloss-i.md).</span></span> <span data-ttu-id="93fd5-120">[**\_ \_ Инстанцекреатионевент**](--instancecreationevent.md) или [**\_ \_ намеспацеделетионевент**](--namespacedeletionevent.md) являются примерами встроенных событий.</span><span class="sxs-lookup"><span data-stu-id="93fd5-120">[**\_\_InstanceCreationEvent**](--instancecreationevent.md) or [**\_\_NamespaceDeletionEvent**](--namespacedeletionevent.md) are examples of intrinsic events.</span></span> <span data-ttu-id="93fd5-121">Уведомление об изменении, которое поставщик делает для определения события поставщика, называется [*внешние события*](gloss-e.md).</span><span class="sxs-lookup"><span data-stu-id="93fd5-121">Notification of a change that a provider makes to define a provider event is called an [*extrinsic event*](gloss-e.md).</span></span> <span data-ttu-id="93fd5-122">Например, поставщик [системного реестра](/previous-versions/windows/desktop/regprov/system-registry-provider), [поставщик событий управления питанием](/windows/desktop/CIMWin32Prov/power-management-event-provider)и [поставщик Win32](/windows/desktop/CIMWin32Prov/win32-provider) определяют собственные события.</span><span class="sxs-lookup"><span data-stu-id="93fd5-122">For example, the [System Registry Provider](/previous-versions/windows/desktop/regprov/system-registry-provider), [Power Management Event Provider](/windows/desktop/CIMWin32Prov/power-management-event-provider), and [Win32 Provider](/windows/desktop/CIMWin32Prov/win32-provider) define their own events.</span></span> <span data-ttu-id="93fd5-123">Дополнительные сведения см. [в разделе Определение типа получаемого события](determining-the-type-of-event-to-receive.md).</span><span class="sxs-lookup"><span data-stu-id="93fd5-123">For more information, see [Determining the Type of Event to Receive](determining-the-type-of-event-to-receive.md).</span></span>

## <a name="example"></a><span data-ttu-id="93fd5-124">Пример</span><span class="sxs-lookup"><span data-stu-id="93fd5-124">Example</span></span>

<span data-ttu-id="93fd5-125">Следующий пример кода скрипта является запросом для встроенного [**\_ \_ инстанцекреатионевент**](--instancecreationevent.md) класса событий [**Win32 \_ нтложевент**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogevent).</span><span class="sxs-lookup"><span data-stu-id="93fd5-125">The following script code example is a query for the intrinsic [**\_\_InstanceCreationEvent**](--instancecreationevent.md) of the event class [**Win32\_NTLogEvent**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogevent).</span></span> <span data-ttu-id="93fd5-126">Вы можете запустить эту программу в фоновом режиме и при наличии события появится сообщение.</span><span class="sxs-lookup"><span data-stu-id="93fd5-126">You can run this program in the background and when there is an event, a message appears.</span></span> <span data-ttu-id="93fd5-127">Если закрыть диалоговое окно **Ожидание событий** , программа прекратит ожидание событий.</span><span class="sxs-lookup"><span data-stu-id="93fd5-127">If you close the **Waiting for events** dialog box, the program stops waiting for events.</span></span> <span data-ttu-id="93fd5-128">Имейте в виду, что параметр **SeSecurityPrivilege** должен быть включен.</span><span class="sxs-lookup"><span data-stu-id="93fd5-128">Be aware that the **SeSecurityPrivilege** must be enabled.</span></span>


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





<span data-ttu-id="93fd5-129">В следующем примере кода VBScript показано [ \_ \_ события registryvaluechangeevent](registering-for-system-registry-events.md) внешних событий, определяемое поставщиком реестра.</span><span class="sxs-lookup"><span data-stu-id="93fd5-129">The following VBScript code example shows the extrinsic event [\_\_RegistryValueChangeEvent](registering-for-system-registry-events.md) that the registry provider defines.</span></span> <span data-ttu-id="93fd5-130">Скрипт создает временный потребитель с помощью вызова [**SWbemServices.Exeкнотификатионкуерясинк**](swbemservices-execnotificationqueryasync.md)и получает события только при выполнении скрипта.</span><span class="sxs-lookup"><span data-stu-id="93fd5-130">The script creates a temporary consumer by using the call to [**SWbemServices.ExecNotificationQueryAsync**](swbemservices-execnotificationqueryasync.md), and only receives events when the script is running.</span></span> <span data-ttu-id="93fd5-131">Следующий скрипт выполняется неограниченно до перезагрузки компьютера, Инструментарий WMI остановлен или сценарий остановлен.</span><span class="sxs-lookup"><span data-stu-id="93fd5-131">The following script runs indefinitely until the computer is rebooted, WMI is stopped, or the script is stopped.</span></span> <span data-ttu-id="93fd5-132">Чтобы прерывать выполнение скрипта вручную, используйте диспетчер задач, чтобы прерывать процесс.</span><span class="sxs-lookup"><span data-stu-id="93fd5-132">To stop the script manually, use Task Manager to stop the process.</span></span> <span data-ttu-id="93fd5-133">Чтобы остановить его программно, используйте метод [**Terminate**](/windows/desktop/CIMWin32Prov/terminate-method-in-class-win32-process) в \_ классе процесса Win32.</span><span class="sxs-lookup"><span data-stu-id="93fd5-133">To stop it programmatically, use the [**Terminate**](/windows/desktop/CIMWin32Prov/terminate-method-in-class-win32-process) method in the Win32\_Process class.</span></span> <span data-ttu-id="93fd5-134">Дополнительные сведения см. [в разделе Настройка безопасности при асинхронном вызове](setting-security-on-an-asynchronous-call.md).</span><span class="sxs-lookup"><span data-stu-id="93fd5-134">For more information, see [Setting Security on an Asynchronous Call](setting-security-on-an-asynchronous-call.md).</span></span>


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



## <a name="event-consumers"></a><span data-ttu-id="93fd5-135">потребители событий</span><span class="sxs-lookup"><span data-stu-id="93fd5-135">Event Consumers</span></span>

<span data-ttu-id="93fd5-136">Вы можете отслеживать или использовать события с помощью следующих потребителей во время выполнения скрипта или приложения:</span><span class="sxs-lookup"><span data-stu-id="93fd5-136">You can monitor or consume events using the following consumers while a script or application is running:</span></span>

-   <span data-ttu-id="93fd5-137">Получатели временных событий</span><span class="sxs-lookup"><span data-stu-id="93fd5-137">Temporary event consumers</span></span>

    <span data-ttu-id="93fd5-138">[*Временный потребитель*](gloss-t.md) — это клиентское приложение WMI, которое получает WMI-событие.</span><span class="sxs-lookup"><span data-stu-id="93fd5-138">A [*temporary consumer*](gloss-t.md) is a WMI client application that receives a WMI event.</span></span> <span data-ttu-id="93fd5-139">WMI включает уникальный интерфейс, который используется для указания событий WMI для отправки в клиентское приложение.</span><span class="sxs-lookup"><span data-stu-id="93fd5-139">WMI includes a unique interface that use to specify the events for WMI to send to a client application.</span></span> <span data-ttu-id="93fd5-140">Временный потребитель событий считается временным, так как он работает только в том случае, если он специально загружен пользователем.</span><span class="sxs-lookup"><span data-stu-id="93fd5-140">A temporary event consumer is considered temporary because it only works when specifically loaded by a user.</span></span> <span data-ttu-id="93fd5-141">Дополнительные сведения см. [в статье получение событий в](receiving-events-for-the-duration-of-your-application.md)течение всего приложения.</span><span class="sxs-lookup"><span data-stu-id="93fd5-141">For more information, see [Receiving Events for the Duration of Your Application](receiving-events-for-the-duration-of-your-application.md).</span></span>

-   <span data-ttu-id="93fd5-142">Потребители постоянных событий</span><span class="sxs-lookup"><span data-stu-id="93fd5-142">Permanent event consumers</span></span>

    <span data-ttu-id="93fd5-143">[*Постоянный потребитель*](gloss-p.md) — это COM-объект, который может все время получить событие WMI.</span><span class="sxs-lookup"><span data-stu-id="93fd5-143">A [*permanent consumer*](gloss-p.md) is a COM object that can receive a WMI event at all times.</span></span> <span data-ttu-id="93fd5-144">Постоянный потребитель событий использует набор постоянных объектов и фильтров для записи событий WMI.</span><span class="sxs-lookup"><span data-stu-id="93fd5-144">A permanent event consumer uses a set of persistent objects and filters to capture a WMI event.</span></span> <span data-ttu-id="93fd5-145">Как и временный потребитель событий, вы настраиваете ряд объектов WMI и фильтров, которые захватывают событие WMI.</span><span class="sxs-lookup"><span data-stu-id="93fd5-145">Like a temporary event consumer, you set up a series of WMI objects and filters that capture a WMI event.</span></span> <span data-ttu-id="93fd5-146">Когда происходит событие, соответствующее фильтру, Инструментарий WMI загружает постоянный потребитель событий и уведомляет его о событии.</span><span class="sxs-lookup"><span data-stu-id="93fd5-146">When an event occurs that matches a filter, WMI loads the permanent event consumer and notifies it about the event.</span></span> <span data-ttu-id="93fd5-147">Поскольку Постоянный потребитель реализуется в репозитории WMI и является исполняемым файлом, зарегистрированным в WMI, постоянный потребитель событий работает и получает события после его создания и даже после перезагрузки операционной системы при условии, что инструментарий WMI запущен.</span><span class="sxs-lookup"><span data-stu-id="93fd5-147">Because a permanent consumer is implemented in the WMI repository and is an executable file that is registered in WMI, the permanent event consumer operates and receives events after it is created and even after a reboot of the operating system as long as WMI is running.</span></span> <span data-ttu-id="93fd5-148">Дополнительные сведения см. [в разделе Получение событий в любое время](receiving-events-at-all-times.md).</span><span class="sxs-lookup"><span data-stu-id="93fd5-148">For more information, see [Receiving Events at All Times](receiving-events-at-all-times.md).</span></span>

<span data-ttu-id="93fd5-149">Сценарии или приложения, получающие события, имеют особые соображения безопасности.</span><span class="sxs-lookup"><span data-stu-id="93fd5-149">Scripts or applications that receive events have special security considerations.</span></span> <span data-ttu-id="93fd5-150">Дополнительные сведения см. в разделе [Защита событий WMI](securing-wmi-events.md).</span><span class="sxs-lookup"><span data-stu-id="93fd5-150">For more information, see [Securing WMI Events](securing-wmi-events.md).</span></span>

<span data-ttu-id="93fd5-151">Приложение или сценарий может использовать встроенный поставщик событий WMI, предоставляющий [стандартные классы потребителей](standard-consumer-classes.md).</span><span class="sxs-lookup"><span data-stu-id="93fd5-151">An application or script can use a built-in WMI event provider that supplies [standard consumer classes](standard-consumer-classes.md).</span></span> <span data-ttu-id="93fd5-152">Каждый стандартный класс-потребитель реагирует на событие с другим действием, отправляя сообщение электронной почты или выполняя сценарий.</span><span class="sxs-lookup"><span data-stu-id="93fd5-152">Each standard consumer class responds to an event with a different action by sending an email message or executing a script.</span></span> <span data-ttu-id="93fd5-153">Нет необходимости писать код поставщика, чтобы использовать стандартный класс потребителя для создания постоянного потребителя событий.</span><span class="sxs-lookup"><span data-stu-id="93fd5-153">You do not have to write provider code to use a standard consumer class to create a permanent event consumer.</span></span> <span data-ttu-id="93fd5-154">Дополнительные сведения см. [в разделе Мониторинг и реагирование на события с помощью стандартных потребителей](monitoring-and-responding-to-events-with-standard-consumers.md).</span><span class="sxs-lookup"><span data-stu-id="93fd5-154">For more information, see [Monitoring and Responding to Events with Standard Consumers](monitoring-and-responding-to-events-with-standard-consumers.md).</span></span>

## <a name="providing-events"></a><span data-ttu-id="93fd5-155">Предоставление событий</span><span class="sxs-lookup"><span data-stu-id="93fd5-155">Providing Events</span></span>

<span data-ttu-id="93fd5-156">Поставщик событий — это COM-компонент, который отправляет событие в WMI.</span><span class="sxs-lookup"><span data-stu-id="93fd5-156">An event provider is a COM component that sends an event to WMI.</span></span> <span data-ttu-id="93fd5-157">Можно создать поставщик событий для отправки события в приложении C++ или C#.</span><span class="sxs-lookup"><span data-stu-id="93fd5-157">You can create an event provider to send an event in a C++ or C# application.</span></span> <span data-ttu-id="93fd5-158">Большинство поставщиков событий управляют объектом для WMI, например, приложением или элементом оборудования.</span><span class="sxs-lookup"><span data-stu-id="93fd5-158">Most event providers manage an object for WMI, for example, an application or hardware item.</span></span> <span data-ttu-id="93fd5-159">Дополнительные сведения см. в разделе [запись поставщика событий](writing-an-event-provider.md).</span><span class="sxs-lookup"><span data-stu-id="93fd5-159">For more information, see [Writing an Event Provider](writing-an-event-provider.md).</span></span>

<span data-ttu-id="93fd5-160">Событие времени или повторение — это событие, возникающее в предопределенном времени.</span><span class="sxs-lookup"><span data-stu-id="93fd5-160">A timed or repeating event is an event that occurs at a predetermined time.</span></span>

<span data-ttu-id="93fd5-161">Инструментарий WMI предоставляет следующие возможности для создания событий с временными или повторяющимися событиями для приложений.</span><span class="sxs-lookup"><span data-stu-id="93fd5-161">WMI provides the following ways to create timed or repeating events for your applications:</span></span>

-   <span data-ttu-id="93fd5-162">Стандартная инфраструктура событий Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="93fd5-162">The standard Microsoft event infrastructure.</span></span>
-   <span data-ttu-id="93fd5-163">Специализированный класс Timer.</span><span class="sxs-lookup"><span data-stu-id="93fd5-163">A specialized timer class.</span></span>

<span data-ttu-id="93fd5-164">Дополнительные сведения см. [в разделе Получение события с превышением времени или повтора](receiving-a-timed-or-repeating-event.md).</span><span class="sxs-lookup"><span data-stu-id="93fd5-164">For more information, see [Receiving a Timed or Repeating Event](receiving-a-timed-or-repeating-event.md).</span></span> <span data-ttu-id="93fd5-165">При написании поставщика событий учитывайте сведения о безопасности, [указанные в этой](providing-events-securely.md)области.</span><span class="sxs-lookup"><span data-stu-id="93fd5-165">When you write an event provider, consider the security information identified in [Providing Events Securely](providing-events-securely.md).</span></span>

<span data-ttu-id="93fd5-166">Рекомендуется компилировать постоянные подписки на события в \\ \\ пространство имен корневой подписки.</span><span class="sxs-lookup"><span data-stu-id="93fd5-166">It is recommended that permanent event subscriptions be compiled into the \\root\\subscription namespace.</span></span> <span data-ttu-id="93fd5-167">Дополнительные сведения см. в разделе [Реализация постоянных подписок на события между пространствами имен](implementing-cross-namespace-permanent-event-subscriptions.md).</span><span class="sxs-lookup"><span data-stu-id="93fd5-167">For more information, see [Implementing Cross-Namespace Permanent Event Subscriptions](implementing-cross-namespace-permanent-event-subscriptions.md).</span></span>

## <a name="subscription-quotas"></a><span data-ttu-id="93fd5-168">Квоты подписки</span><span class="sxs-lookup"><span data-stu-id="93fd5-168">Subscription Quotas</span></span>

<span data-ttu-id="93fd5-169">Опрос событий может снизить производительность для поставщиков, которые поддерживают запросы к огромным наборам данных.</span><span class="sxs-lookup"><span data-stu-id="93fd5-169">Polling for events can degrade performance for providers that support queries over huge data sets.</span></span> <span data-ttu-id="93fd5-170">Кроме того, любой пользователь, имеющий доступ на чтение к пространству имен с динамическими поставщиками, может выполнять атаку типа "отказ в обслуживании" (DoS).</span><span class="sxs-lookup"><span data-stu-id="93fd5-170">Additionally, any user that has read access to a namespace with dynamic providers can perform a denial of service (DoS) attack.</span></span> <span data-ttu-id="93fd5-171">WMI поддерживает квоты для всех пользователей в сочетании и для каждого потребителя событий в одном экземпляре [**\_ \_ арбитраторконфигуратион**](--arbitratorconfiguration.md) , расположенном в \\ корневом пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="93fd5-171">WMI maintains quotas for all of the users combined and for each event consumer in the single instance of [**\_\_ArbitratorConfiguration**](--arbitratorconfiguration.md) located in the \\root namespace.</span></span> <span data-ttu-id="93fd5-172">Эти квоты являются глобальными, а не для каждого пространства имен.</span><span class="sxs-lookup"><span data-stu-id="93fd5-172">These quotas are global rather than for each namespace.</span></span> <span data-ttu-id="93fd5-173">Квоты изменить нельзя.</span><span class="sxs-lookup"><span data-stu-id="93fd5-173">You cannot change the quotas.</span></span>

<span data-ttu-id="93fd5-174">В настоящее время Инструментарий WMI применяет квоты с помощью свойств [**\_ \_ арбитраторконфигуратион**](--arbitratorconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="93fd5-174">WMI currently enforces quotas using the properties of [**\_\_ArbitratorConfiguration**](--arbitratorconfiguration.md).</span></span> <span data-ttu-id="93fd5-175">Каждая квота имеет каждого пользователя и общую версию, включающую всех пользователей в сочетании, а не на пространство имен.</span><span class="sxs-lookup"><span data-stu-id="93fd5-175">Each quota has a per user and a total version that includes all users combined, not per namespace.</span></span> <span data-ttu-id="93fd5-176">В следующей таблице перечислены квоты, которые применяются к свойствам **\_ \_ арбитраторконфигуратион** .</span><span class="sxs-lookup"><span data-stu-id="93fd5-176">The following table lists the quotas that apply to the **\_\_ArbitratorConfiguration** properties.</span></span>



| <span data-ttu-id="93fd5-177">Общее/изучение</span><span class="sxs-lookup"><span data-stu-id="93fd5-177">Total/PerUser</span></span>                                                                   | <span data-ttu-id="93fd5-178">Quota</span><span class="sxs-lookup"><span data-stu-id="93fd5-178">Quota</span></span>                                                                       |
|---------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="93fd5-179">темпорарисубскриптионстотал</span><span class="sxs-lookup"><span data-stu-id="93fd5-179">TemporarySubscriptionsTotal</span></span><br/> <span data-ttu-id="93fd5-180">темпорарисубскриптионсперусер</span><span class="sxs-lookup"><span data-stu-id="93fd5-180">TemporarySubscriptionsPerUser</span></span><br/> | <span data-ttu-id="93fd5-181">10 000</span><span class="sxs-lookup"><span data-stu-id="93fd5-181">10,000</span></span><br/> <span data-ttu-id="93fd5-182">1000</span><span class="sxs-lookup"><span data-stu-id="93fd5-182">1,000</span></span><br/>                                          |
| <span data-ttu-id="93fd5-183">перманентсубскриптионстотал</span><span class="sxs-lookup"><span data-stu-id="93fd5-183">PermanentSubscriptionsTotal</span></span><br/> <span data-ttu-id="93fd5-184">перманентсубскриптионсперусер</span><span class="sxs-lookup"><span data-stu-id="93fd5-184">PermanentSubscriptionsPerUser</span></span><br/> | <span data-ttu-id="93fd5-185">10 000</span><span class="sxs-lookup"><span data-stu-id="93fd5-185">10,000</span></span><br/> <span data-ttu-id="93fd5-186">1000</span><span class="sxs-lookup"><span data-stu-id="93fd5-186">1,000</span></span><br/>                                          |
| <span data-ttu-id="93fd5-187">поллингинструктионстотал</span><span class="sxs-lookup"><span data-stu-id="93fd5-187">PollingInstructionsTotal</span></span><br/> <span data-ttu-id="93fd5-188">поллингинструктионсперусер</span><span class="sxs-lookup"><span data-stu-id="93fd5-188">PollingInstructionsPerUser</span></span><br/>       | <span data-ttu-id="93fd5-189">10 000</span><span class="sxs-lookup"><span data-stu-id="93fd5-189">10,000</span></span><br/> <span data-ttu-id="93fd5-190">1000</span><span class="sxs-lookup"><span data-stu-id="93fd5-190">1,000</span></span><br/>                                          |
| <span data-ttu-id="93fd5-191">поллингмеморитотал</span><span class="sxs-lookup"><span data-stu-id="93fd5-191">PollingMemoryTotal</span></span><br/> <span data-ttu-id="93fd5-192">поллингмемориперусер</span><span class="sxs-lookup"><span data-stu-id="93fd5-192">PollingMemoryPerUser</span></span><br/>                   | <span data-ttu-id="93fd5-193">10 000 000 (0x989680) байт</span><span class="sxs-lookup"><span data-stu-id="93fd5-193">10,000,000 (0x989680) bytes</span></span><br/> <span data-ttu-id="93fd5-194">5 000 000 (0x4CB40) байт</span><span class="sxs-lookup"><span data-stu-id="93fd5-194">5,000,000 (0x4CB40) bytes</span></span><br/> |



 

<span data-ttu-id="93fd5-195">Администратор или пользователь с разрешением " **полный доступ на \_ запись** " в пространстве имен может изменить одноэлементный экземпляр [**\_ \_ арбитраторконфигуратион**](--arbitratorconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="93fd5-195">An administrator or a user with **FULL\_WRITE** permission in the namespace can modify the singleton instance of [**\_\_ArbitratorConfiguration**](--arbitratorconfiguration.md).</span></span> <span data-ttu-id="93fd5-196">WMI отслеживает квоту для каждого пользователя.</span><span class="sxs-lookup"><span data-stu-id="93fd5-196">WMI tracks the per-user quota.</span></span>

## <a name="related-topics"></a><span data-ttu-id="93fd5-197">См. также</span><span class="sxs-lookup"><span data-stu-id="93fd5-197">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="93fd5-198">Использование инструментария WMI</span><span class="sxs-lookup"><span data-stu-id="93fd5-198">Using WMI</span></span>](using-wmi.md)
</dt> </dl>

 

