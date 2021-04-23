---
description: Системные администраторы могут использовать инструментарий WMI для наблюдения за событиями в сети.
ms.assetid: 871d4add-a7b1-4ec9-a202-3821fdf09e9f
ms.tgt_platform: multiple
title: Отслеживание событий
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ea5d9fc6f9a12f4aa1fb7bc0ff6f66fc4dd4a7e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155239"
---
# <a name="monitoring-events"></a><span data-ttu-id="f8cb6-103">Отслеживание событий</span><span class="sxs-lookup"><span data-stu-id="f8cb6-103">Monitoring Events</span></span>

<span data-ttu-id="f8cb6-104">Системные администраторы могут использовать инструментарий WMI для наблюдения за событиями в сети.</span><span class="sxs-lookup"><span data-stu-id="f8cb6-104">System administrators can use WMI to monitor events on a network.</span></span> <span data-ttu-id="f8cb6-105">Пример:</span><span class="sxs-lookup"><span data-stu-id="f8cb6-105">For example:</span></span>

-   <span data-ttu-id="f8cb6-106">Служба неожиданно останавливается.</span><span class="sxs-lookup"><span data-stu-id="f8cb6-106">A service stops unexpectedly.</span></span>
-   <span data-ttu-id="f8cb6-107">Сервер становится недоступным.</span><span class="sxs-lookup"><span data-stu-id="f8cb6-107">A server becomes unavailable.</span></span>
-   <span data-ttu-id="f8cb6-108">Емкость диска будет заполнять до 80%.</span><span class="sxs-lookup"><span data-stu-id="f8cb6-108">A disk drive fills to 80% capacity.</span></span>
-   <span data-ttu-id="f8cb6-109">События безопасности выводятся в журнал событий NT.</span><span class="sxs-lookup"><span data-stu-id="f8cb6-109">Security events are reported to an NT Event Log.</span></span>

<span data-ttu-id="f8cb6-110">WMI поддерживает обнаружение событий и доставку потребителям событий, так как некоторые поставщики WMI являются поставщиками событий.</span><span class="sxs-lookup"><span data-stu-id="f8cb6-110">WMI supports event detection and delivery to event consumers because some WMI providers are event providers.</span></span> <span data-ttu-id="f8cb6-111">Дополнительные сведения см. [в разделе Получение WMI-события](receiving-a-wmi-event.md).</span><span class="sxs-lookup"><span data-stu-id="f8cb6-111">For more information, see [Receiving a WMI Event](receiving-a-wmi-event.md).</span></span>

<span data-ttu-id="f8cb6-112">[*Потребители событий*](gloss-e.md) — это приложения или скрипты, запрашивающие уведомления о событиях, а затем выполняющие задачи при возникновении конкретных событий.</span><span class="sxs-lookup"><span data-stu-id="f8cb6-112">[*Event consumers*](gloss-e.md) are applications or scripts that request notification of events, and then perform tasks when specific events occur.</span></span> <span data-ttu-id="f8cb6-113">Можно создавать скрипты или приложения для мониторинга событий, которые временно отслеживают время возникновения событий.</span><span class="sxs-lookup"><span data-stu-id="f8cb6-113">You can create event monitoring scripts or applications that temporarily monitor when events occur.</span></span> <span data-ttu-id="f8cb6-114">Инструментарий WMI также предоставляет набор предварительно установленных постоянных поставщиков событий и постоянных классов потребителей, позволяющих постоянно отслеживать события.</span><span class="sxs-lookup"><span data-stu-id="f8cb6-114">WMI also supplies a set of preinstalled permanent event providers and the permanent consumer classes that enable you to permanently monitor events.</span></span> <span data-ttu-id="f8cb6-115">Дополнительные сведения см. [в разделе Мониторинг и реагирование на события с помощью стандартных потребителей](monitoring-and-responding-to-events-with-standard-consumers.md).</span><span class="sxs-lookup"><span data-stu-id="f8cb6-115">For more information, see [Monitoring and Responding to Events with Standard Consumers](monitoring-and-responding-to-events-with-standard-consumers.md).</span></span>

<span data-ttu-id="f8cb6-116">В этом разделе обсуждаются следующие разделы:</span><span class="sxs-lookup"><span data-stu-id="f8cb6-116">The following sections are discussed in this topic:</span></span>

-   [<span data-ttu-id="f8cb6-117">Использование временных потребителей событий</span><span class="sxs-lookup"><span data-stu-id="f8cb6-117">Using Temporary Event Consumers</span></span>](#using-temporary-event-consumers)
-   [<span data-ttu-id="f8cb6-118">Использование постоянных потребителей событий</span><span class="sxs-lookup"><span data-stu-id="f8cb6-118">Using Permanent Event Consumers</span></span>](#using-permanent-event-consumers)

## <a name="using-temporary-event-consumers"></a><span data-ttu-id="f8cb6-119">Использование временных потребителей событий</span><span class="sxs-lookup"><span data-stu-id="f8cb6-119">Using Temporary Event Consumers</span></span>

<span data-ttu-id="f8cb6-120">Временные потребители событий — это скрипты или приложения, которые возвращают события, соответствующие запросу или фильтру событий.</span><span class="sxs-lookup"><span data-stu-id="f8cb6-120">Temporary event consumers are scripts or applications that return the events that match an event query or filter.</span></span> <span data-ttu-id="f8cb6-121">Временные запросы событий обычно используют [**IWbemServices:: ексекнотификатионкуери**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery) в приложениях C++ или [**SWbemServices.Exeкнотификатионкуери**](swbemservices-execnotificationquery.md) в скриптах и Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="f8cb6-121">Temporary event queries usually use either [**IWbemServices::ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery) in C++ applications or [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md) in scripts and Visual Basic.</span></span>

<span data-ttu-id="f8cb6-122">Запрос события запрашивает экземпляры класса событий, указывающего определенный тип события, например [**Win32 \_ Процесстраце**](/previous-versions/windows/desktop/krnlprov/win32-processtrace) или [**регистрикэйчанжеевент**](/previous-versions/windows/desktop/regprov/registrykeychangeevent).</span><span class="sxs-lookup"><span data-stu-id="f8cb6-122">An event query requests instances of an event class that specifies a certain type of event, such as [**Win32\_ProcessTrace**](/previous-versions/windows/desktop/krnlprov/win32-processtrace) or [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent).</span></span>

<span data-ttu-id="f8cb6-123">Следующий пример кода VBScript запрашивает уведомление при создании экземпляра [**Win32 \_ процесстраце**](/previous-versions/windows/desktop/krnlprov/win32-processtrace) .</span><span class="sxs-lookup"><span data-stu-id="f8cb6-123">The following VBScript code example requests notification when an instance of [**Win32\_ProcessTrace**](/previous-versions/windows/desktop/krnlprov/win32-processtrace) is created.</span></span> <span data-ttu-id="f8cb6-124">Экземпляр этого класса создается при запуске или остановке процесса.</span><span class="sxs-lookup"><span data-stu-id="f8cb6-124">An instance of this class is generated when a process is started or stopped.</span></span>

<span data-ttu-id="f8cb6-125">Чтобы выполнить сценарий, скопируйте его в файл с именем event.vbs и используйте следующую командную строку: **cscript event.vbs**.</span><span class="sxs-lookup"><span data-stu-id="f8cb6-125">To execute the script, copy it to a file named event.vbs and use the following command line: **cscript event.vbs**.</span></span> <span data-ttu-id="f8cb6-126">Выходные данные скрипта можно просмотреть, запустив Notepad.exe или любой другой процесс.</span><span class="sxs-lookup"><span data-stu-id="f8cb6-126">You can see output from the script by starting Notepad.exe or any other process.</span></span> <span data-ttu-id="f8cb6-127">Сценарий останавливается после запуска или остановки пяти процессов.</span><span class="sxs-lookup"><span data-stu-id="f8cb6-127">The script stops after five processes have started or stopped.</span></span>

<span data-ttu-id="f8cb6-128">Этот скрипт вызывает [**SWbemServices.Exeкнотификатионкуери**](swbemservices-execnotificationquery.md), который является [*семисинчронаус*](gloss-s.md) версией метода.</span><span class="sxs-lookup"><span data-stu-id="f8cb6-128">This script calls [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md), which is the [*semisynchronous*](gloss-s.md) version of the method.</span></span> <span data-ttu-id="f8cb6-129">См. следующий скрипт для примера настройки асинхронной подписки на события, вызвав [**SWbemServices.Exeкнотификатионкуерясинк**](swbemservices-execnotificationqueryasync.md).</span><span class="sxs-lookup"><span data-stu-id="f8cb6-129">See the next script for an example of setting up an asynchronous temporary event subscription by calling [**SWbemServices.ExecNotificationQueryAsync**](swbemservices-execnotificationqueryasync.md).</span></span> <span data-ttu-id="f8cb6-130">Дополнительные сведения см. [в разделе вызов метода](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="f8cb6-130">For more information, see [Calling a Method](calling-a-method.md).</span></span> <span data-ttu-id="f8cb6-131">Скрипт вызывает [**свбемевентсаурце. некстевент**](swbemeventsource-nextevent.md) для получения и обработки каждого события по мере его поступления.</span><span class="sxs-lookup"><span data-stu-id="f8cb6-131">The script calls [**SWbemEventSource.NextEvent**](swbemeventsource-nextevent.md) to obtain and process each event as it arrives.</span></span> <span data-ttu-id="f8cb6-132">Сохраните скрипт в файле с расширением vbs и выполните сценарий в командной строке с помощью CScript: **cscript file.vbs**.</span><span class="sxs-lookup"><span data-stu-id="f8cb6-132">Save the script in a file with a .vbs extension and run the script on a command line using CScript: **cscript file.vbs**.</span></span>


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:\\" _
    & strComputer & "\root\CIMV2") 
Set objEvents = objWMIService.ExecNotificationQuery _
    ("SELECT * FROM Win32_ProcessTrace")

Wscript.Echo "Waiting for events ..."
i = 0
Do Until i=5
    Set objReceivedEvent = objEvents.NextEvent
    'report an event
    Wscript.Echo "Win32_ProcessTrace event occurred" & VBNewLine _
        & "Process Name = " _
            & objReceivedEvent.ProcessName & VBNewLine _
        & "Process ID = " _
            & objReceivedEvent.Processid & VBNewLine _
        & "Session ID = " & objReceivedEvent.SessionID 
i = i+ 1
Loop
```



Временные потребители событий должны запускаться вручную и не должны сохраняться при перезапуске WMI или перезапуске операционной системы. <span data-ttu-id="f8cb6-134">Временный потребитель событий может обрабатывать события только во время его выполнения.</span><span class="sxs-lookup"><span data-stu-id="f8cb6-134">A temporary event consumer can process events only while it is running.</span></span>

<span data-ttu-id="f8cb6-135">В следующей процедуре описывается создание временного потребителя событий.</span><span class="sxs-lookup"><span data-stu-id="f8cb6-135">The following procedure describes how to create a temporary event consumer.</span></span>

<span data-ttu-id="f8cb6-136">**Создание временного потребителя событий**</span><span class="sxs-lookup"><span data-stu-id="f8cb6-136">**To create a temporary event consumer**</span></span>

1.  <span data-ttu-id="f8cb6-137">Определите, какой язык программирования следует использовать.</span><span class="sxs-lookup"><span data-stu-id="f8cb6-137">Decide which programming language to use.</span></span>

    <span data-ttu-id="f8cb6-138">Язык программирования определяет используемый API.</span><span class="sxs-lookup"><span data-stu-id="f8cb6-138">The programming language determines the API to use.</span></span>

    -   <span data-ttu-id="f8cb6-139">Для языка программирования C++ используйте [COM API для WMI](com-api-for-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="f8cb6-139">For the C++ programming language, use the [COM API for WMI](com-api-for-wmi.md).</span></span>
    -   <span data-ttu-id="f8cb6-140">Для Visual Basic или языков сценариев используйте [API скриптов для инструментария WMI](scripting-api-for-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="f8cb6-140">For Visual Basic or scripting languages, use the [Scripting API for WMI](scripting-api-for-wmi.md).</span></span>

2.  <span data-ttu-id="f8cb6-141">Начните программировать временное приложение-потребитель событий так же, как вы запускаете приложение WMI.</span><span class="sxs-lookup"><span data-stu-id="f8cb6-141">Start coding a temporary event consumer application the same way that you start a WMI application.</span></span>

    <span data-ttu-id="f8cb6-142">Первые шаги написания кода зависят от языка программирования.</span><span class="sxs-lookup"><span data-stu-id="f8cb6-142">The first steps of coding depend on the programming language.</span></span> <span data-ttu-id="f8cb6-143">Как правило, вы входите на WMI и устанавливаете параметры безопасности.</span><span class="sxs-lookup"><span data-stu-id="f8cb6-143">Typically, you log onto WMI and set up the security settings.</span></span> <span data-ttu-id="f8cb6-144">Дополнительные сведения см. [в разделе Создание приложения WMI или скрипта](creating-a-wmi-application-or-script.md).</span><span class="sxs-lookup"><span data-stu-id="f8cb6-144">For more information, see [Creating a WMI Application or Script](creating-a-wmi-application-or-script.md).</span></span>

3.  <span data-ttu-id="f8cb6-145">Определите запрос события, который вы хотите использовать.</span><span class="sxs-lookup"><span data-stu-id="f8cb6-145">Define the event query that you want to use.</span></span>

    <span data-ttu-id="f8cb6-146">Для получения некоторых типов данных о производительности может потребоваться использовать классы, предоставляемые высокопроизводительными поставщиками.</span><span class="sxs-lookup"><span data-stu-id="f8cb6-146">To obtain some types of performance data, you may need to use classes provided by high-performance providers.</span></span> <span data-ttu-id="f8cb6-147">Дополнительные сведения см. в статьях [мониторинг данных производительности](monitoring-performance-data.md), [Определение типа получаемого события](determining-the-type-of-event-to-receive.md)и [выполнение запросов с помощью WQL](querying-with-wql.md).</span><span class="sxs-lookup"><span data-stu-id="f8cb6-147">For more information, see [Monitoring Performance Data](monitoring-performance-data.md), [Determining the Type of Event To Receive](determining-the-type-of-event-to-receive.md), and [Querying with WQL](querying-with-wql.md).</span></span>

4.  <span data-ttu-id="f8cb6-148">Решите сделать либо асинхронный вызов, либо вызов семисинчронаус, а затем выберите метод API.</span><span class="sxs-lookup"><span data-stu-id="f8cb6-148">Decide to make either an asynchronous call or an semisynchronous call, and choose the API method.</span></span>

    <span data-ttu-id="f8cb6-149">Асинхронные вызовы позволяют избежать издержек при опросе данных.</span><span class="sxs-lookup"><span data-stu-id="f8cb6-149">Asynchronous calls allow you to avoid the overhead of polling for data.</span></span> <span data-ttu-id="f8cb6-150">Однако вызовы семисинчронаус обеспечивают аналогичные производительность с большей безопасностью.</span><span class="sxs-lookup"><span data-stu-id="f8cb6-150">However, semisynchronous calls provide similar performance with greater security.</span></span> <span data-ttu-id="f8cb6-151">Дополнительные сведения см. [в разделе вызов метода](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="f8cb6-151">For more information, see [Calling a Method](calling-a-method.md).</span></span>

5.  <span data-ttu-id="f8cb6-152">Сделайте вызов асинхронного или семисинчронаусного метода и включите в него запрос события в качестве параметра *стркуери* .</span><span class="sxs-lookup"><span data-stu-id="f8cb6-152">Make the asynchronous or semisynchronous method call and include an event query as the *strQuery* parameter.</span></span>

    <span data-ttu-id="f8cb6-153">Для приложений C++ вызовите следующие методы:</span><span class="sxs-lookup"><span data-stu-id="f8cb6-153">For C++ applications, call the following methods:</span></span>

    -   [<span data-ttu-id="f8cb6-154">**IWbemServices:: Ексекнотификатионкуери**</span><span class="sxs-lookup"><span data-stu-id="f8cb6-154">**IWbemServices::ExecNotificationQuery**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery)
    -   [<span data-ttu-id="f8cb6-155">**IWbemServices:: ExecNotificationQueryAsync**</span><span class="sxs-lookup"><span data-stu-id="f8cb6-155">**IWbemServices::ExecNotificationQueryAsync**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationqueryasync)

    <span data-ttu-id="f8cb6-156">Для скриптов вызовите следующие методы:</span><span class="sxs-lookup"><span data-stu-id="f8cb6-156">For scripts, call the following methods:</span></span>

    -   [<span data-ttu-id="f8cb6-157">**SWbemServices.ExeКнотификатионкуери**</span><span class="sxs-lookup"><span data-stu-id="f8cb6-157">**SWbemServices.ExecNotificationQuery**</span></span>](swbemservices-execnotificationquery.md)
    -   [<span data-ttu-id="f8cb6-158">**SWbemServices.ExeКнотификатионкуерясинк**</span><span class="sxs-lookup"><span data-stu-id="f8cb6-158">**SWbemServices.ExecNotificationQueryAsync**</span></span>](swbemservices-execnotificationqueryasync.md)

6.  <span data-ttu-id="f8cb6-159">Напишите код для обработки возвращенного объекта события.</span><span class="sxs-lookup"><span data-stu-id="f8cb6-159">Write the code to process the returned event object.</span></span>

    <span data-ttu-id="f8cb6-160">Для асинхронных запросов событий разместите код в различных методах или событиях приемника объекта.</span><span class="sxs-lookup"><span data-stu-id="f8cb6-160">For asynchronous event queries, put the code in the various methods or events of the object sink.</span></span> <span data-ttu-id="f8cb6-161">Для запросов событий семисинчронаус каждый объект возвращается, так как WMI получает его, поэтому код должен находиться в цикле, обрабатывающем каждый объект.</span><span class="sxs-lookup"><span data-stu-id="f8cb6-161">For semisynchronous event queries, each object is returned as WMI obtains it, so the code should be in the loop that handles each object.</span></span>

<span data-ttu-id="f8cb6-162">Следующий пример кода скрипта представляет собой асинхронную версию скрипта [**Win32 \_ процесстраце**](/previous-versions/windows/desktop/krnlprov/win32-processtrace) .</span><span class="sxs-lookup"><span data-stu-id="f8cb6-162">The following script code example is an asynchronous version of the [**Win32\_ProcessTrace**](/previous-versions/windows/desktop/krnlprov/win32-processtrace) script.</span></span> <span data-ttu-id="f8cb6-163">Так как асинхронные операции возвращаются немедленно, диалоговое окно сохраняет активный скрипт, пока он ожидает событий.</span><span class="sxs-lookup"><span data-stu-id="f8cb6-163">Because asynchronous operations return immediately, a dialog box keeps the script active while it is waiting for events.</span></span>

<span data-ttu-id="f8cb6-164">Вместо вызова [**свбемевентсаурце. некстевент**](swbemeventsource-nextevent.md) для получения каждого события сценарий имеет обработчик события [**свбемсинк онобжектреади**](swbemsink-onobjectready.md) .</span><span class="sxs-lookup"><span data-stu-id="f8cb6-164">Rather than call [**SWbemEventSource.NextEvent**](swbemeventsource-nextevent.md) to receive each event, the script has an event handler for the [**SWbemSink OnObjectReady**](swbemsink-onobjectready.md) event.</span></span>


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:\\" & _
    strComputer & "\root\CIMV2") 
Set EventSink = WScript.CreateObject( _
    "WbemScripting.SWbemSink","SINK_")

objWMIservice.ExecNotificationQueryAsync EventSink, _
    "SELECT * FROM Win32_ProcessTrace WITHIN 10"
WScript.Echo "Waiting for events..."

i = 0
While (True)
    Wscript.Sleep(1000)
Wend

Sub SINK_OnObjectReady(objObject, objAsyncContext)
    Wscript.Echo "Win32_ProcessTrace event has occurred."
    i = i+1
    If i = 3 Then WScript.Quit 0 
End Sub

```



> [!Note]
>
> <span data-ttu-id="f8cb6-165">Асинхронный обратный вызов, такой как обратный вызов, обрабатываемый `SINK_OnObjectReady` подподпрограммой, позволяет пользователю, не прошедшему проверку подлинности, предоставлять данные в приемник.</span><span class="sxs-lookup"><span data-stu-id="f8cb6-165">An asynchronous callback such as a callback handled by the `SINK_OnObjectReady` subroutine, allows a nonauthenticated user to provide data to the sink.</span></span> <span data-ttu-id="f8cb6-166">Для повышения безопасности используйте либо семисинчронаус связь, либо синхронное взаимодействие.</span><span class="sxs-lookup"><span data-stu-id="f8cb6-166">For better security, use either semisynchronous communication or synchronous communication.</span></span> <span data-ttu-id="f8cb6-167">Дополнительные сведения см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="f8cb6-167">For more information, see the following topics:</span></span>
>
> -   [<span data-ttu-id="f8cb6-168">Вызов Семисинчронаус с помощью C++</span><span class="sxs-lookup"><span data-stu-id="f8cb6-168">Making a Semisynchronous Call with C++</span></span>](making-a-semisynchronous-call-with-c--.md)
> -   [<span data-ttu-id="f8cb6-169">Вызов Семисинчронаус с помощью VBScript</span><span class="sxs-lookup"><span data-stu-id="f8cb6-169">Making a Semisynchronous Call with VBScript</span></span>](making-a-semisynchronous-call-with-vbscript.md)
> -   [<span data-ttu-id="f8cb6-170">Создание асинхронного вызова с помощью C++</span><span class="sxs-lookup"><span data-stu-id="f8cb6-170">Making an Asynchronous Call with C++</span></span>](making-an-asynchronous-call-with-c--.md)
> -   [<span data-ttu-id="f8cb6-171">Выполнение асинхронного вызова с помощью VBScript</span><span class="sxs-lookup"><span data-stu-id="f8cb6-171">Making an Asynchronous Call with VBScript</span></span>](making-an-asynchronous-call-with-vbscript.md)
> -   [<span data-ttu-id="f8cb6-172">Настройка безопасности при асинхронном вызове</span><span class="sxs-lookup"><span data-stu-id="f8cb6-172">Setting Security on an Asynchronous Call</span></span>](setting-security-on-an-asynchronous-call.md)
> -   [<span data-ttu-id="f8cb6-173">Защита клиентов скриптов</span><span class="sxs-lookup"><span data-stu-id="f8cb6-173">Securing Scripting Clients</span></span>](securing-scripting-clients.md)

 

## <a name="using-permanent-event-consumers"></a><span data-ttu-id="f8cb6-174">Использование постоянных потребителей событий</span><span class="sxs-lookup"><span data-stu-id="f8cb6-174">Using Permanent Event Consumers</span></span>

<span data-ttu-id="f8cb6-175">Постоянный потребитель событий выполняется до тех пор, пока регистрация не будет явно отменена, а затем запускается при перезапуске WMI или системы.</span><span class="sxs-lookup"><span data-stu-id="f8cb6-175">A permanent event consumer runs until its registration is explicitly canceled, and then starts up when WMI or the system restarts.</span></span>

<span data-ttu-id="f8cb6-176">Постоянный потребитель событий — это сочетание классов WMI, фильтров и COM-объектов в системе.</span><span class="sxs-lookup"><span data-stu-id="f8cb6-176">A permanent event consumer is a combination of WMI classes, filters, and COM objects on a system.</span></span>

<span data-ttu-id="f8cb6-177">В следующем списке указаны части, необходимые для создания постоянного потребителя событий.</span><span class="sxs-lookup"><span data-stu-id="f8cb6-177">The following list identifies the parts required to create a permanent event consumer:</span></span>

-   <span data-ttu-id="f8cb6-178">COM-объект, содержащий код, реализующий постоянный потребитель.</span><span class="sxs-lookup"><span data-stu-id="f8cb6-178">A COM object containing the code that implements the permanent consumer.</span></span>
-   <span data-ttu-id="f8cb6-179">Новый постоянный класс потребителя.</span><span class="sxs-lookup"><span data-stu-id="f8cb6-179">A new permanent consumer class.</span></span>
-   <span data-ttu-id="f8cb6-180">Экземпляр класса постоянного потребителя.</span><span class="sxs-lookup"><span data-stu-id="f8cb6-180">An instance of the permanent consumer class.</span></span>
-   <span data-ttu-id="f8cb6-181">Фильтр, содержащий запрос для событий.</span><span class="sxs-lookup"><span data-stu-id="f8cb6-181">A filter that contains the query for events.</span></span>
-   <span data-ttu-id="f8cb6-182">Связь между потребителем и фильтром.</span><span class="sxs-lookup"><span data-stu-id="f8cb6-182">A link between the consumer and the filter.</span></span>

<span data-ttu-id="f8cb6-183">Дополнительные сведения см. [в разделе Получение событий в любое время](--filtertoconsumerbinding.md).</span><span class="sxs-lookup"><span data-stu-id="f8cb6-183">For more information, see [Receiving Events At All Times](--filtertoconsumerbinding.md).</span></span>

<span data-ttu-id="f8cb6-184">Инструментарий WMI предоставляет несколько постоянных потребителей.</span><span class="sxs-lookup"><span data-stu-id="f8cb6-184">WMI supplies several permanent consumers.</span></span> <span data-ttu-id="f8cb6-185">Классы потребителей и COM-объекты, содержащие код, предварительно установлены.</span><span class="sxs-lookup"><span data-stu-id="f8cb6-185">The consumer classes and COM object containing the code are preinstalled.</span></span> <span data-ttu-id="f8cb6-186">Например, можно создать и настроить экземпляр класса [**активескриптевентконсумер**](activescripteventconsumer.md) для выполнения скрипта при возникновении события.</span><span class="sxs-lookup"><span data-stu-id="f8cb6-186">For example, you can create and configure an instance of the [**ActiveScriptEventConsumer**](activescripteventconsumer.md) class to run a script when an event occurs.</span></span> <span data-ttu-id="f8cb6-187">Дополнительные сведения см. [в разделе Мониторинг и реагирование на события с помощью стандартных потребителей](monitoring-and-responding-to-events-with-standard-consumers.md).</span><span class="sxs-lookup"><span data-stu-id="f8cb6-187">For more information, see [Monitoring and Responding to Events with Standard Consumers](monitoring-and-responding-to-events-with-standard-consumers.md).</span></span> <span data-ttu-id="f8cb6-188">Пример использования **активескриптевентконсумер** см. в разделе [выполнение сценария на основе события](running-a-script-based-on-an-event.md).</span><span class="sxs-lookup"><span data-stu-id="f8cb6-188">For an example of using **ActiveScriptEventConsumer**, see [Running a Script Based on an Event](running-a-script-based-on-an-event.md).</span></span>

<span data-ttu-id="f8cb6-189">В следующей процедуре описывается создание постоянного потребителя событий.</span><span class="sxs-lookup"><span data-stu-id="f8cb6-189">The following procedure describes how to create a permanent event consumer.</span></span>

<span data-ttu-id="f8cb6-190">**Создание постоянного потребителя событий**</span><span class="sxs-lookup"><span data-stu-id="f8cb6-190">**To create a permanent event consumer**</span></span>

1.  <span data-ttu-id="f8cb6-191">[Зарегистрируйте поставщика событий](registering-a-provider.md) в используемом пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="f8cb6-191">[Register the event provider](registering-a-provider.md) with the namespace that you are using.</span></span>

    <span data-ttu-id="f8cb6-192">Некоторые поставщики событий могут использовать только определенное пространство имен.</span><span class="sxs-lookup"><span data-stu-id="f8cb6-192">Some event providers can only use a specific namespace.</span></span> <span data-ttu-id="f8cb6-193">Например, [**\_ \_ инстанцекреатионевент**](--instancecreationevent.md) является внутренним событием, которое поддерживается [поставщиком Win32](/windows/desktop/CIMWin32Prov/win32-provider) и зарегистрировано по умолчанию с \\ корневым \\ пространством имен CIMV2.</span><span class="sxs-lookup"><span data-stu-id="f8cb6-193">For example, [**\_\_InstanceCreationEvent**](--instancecreationevent.md) is an intrinsic event that is supported by the [Win32 provider](/windows/desktop/CIMWin32Prov/win32-provider) and is registered by default with the \\root\\cimv2 namespace.</span></span>

    > [!Note]  
    > <span data-ttu-id="f8cb6-194">Для создания подписки между пространствами имен можно использовать свойство **евентнамеспаце** объекта [**\_ \_ EventFilter**](--eventfilter.md) , используемого в регистрации.</span><span class="sxs-lookup"><span data-stu-id="f8cb6-194">You can use the **EventNamespace** property of the [**\_\_EventFilter**](--eventfilter.md) used in the registration to create a cross-namespace subscription.</span></span> <span data-ttu-id="f8cb6-195">Дополнительные сведения см. в разделе [Реализация постоянных подписок на события между пространствами имен](implementing-cross-namespace-permanent-event-subscriptions.md).</span><span class="sxs-lookup"><span data-stu-id="f8cb6-195">For more information, see [Implementing Cross-Namespace Permanent Event Subscriptions](implementing-cross-namespace-permanent-event-subscriptions.md).</span></span>

     

2.  <span data-ttu-id="f8cb6-196">[Зарегистрируйте поставщик потребителей событий](registering-an-event-consumer-provider.md) с пространством имен, в котором находятся классы событий.</span><span class="sxs-lookup"><span data-stu-id="f8cb6-196">[Register the event consumer provider](registering-an-event-consumer-provider.md) with the namespace where event classes are located.</span></span>

    <span data-ttu-id="f8cb6-197">WMI использует поставщик объекта-получателя событий для поиска постоянного объекта-получателя события.</span><span class="sxs-lookup"><span data-stu-id="f8cb6-197">WMI uses an event consumer provider to find an event consumer that is permanent.</span></span> <span data-ttu-id="f8cb6-198">Постоянный потребитель событий — это приложение, которое Инструментарий WMI запускает при получении события.</span><span class="sxs-lookup"><span data-stu-id="f8cb6-198">The permanent event consumer is the application that WMI starts when an event is received.</span></span> <span data-ttu-id="f8cb6-199">Для регистрации объекта-получателя событий поставщики создают экземпляры [**\_ \_ евентконсумерпровидеррегистратион**](--eventconsumerproviderregistration.md).</span><span class="sxs-lookup"><span data-stu-id="f8cb6-199">To register event consumer, providers create instances of [**\_\_EventConsumerProviderRegistration**](--eventconsumerproviderregistration.md).</span></span>

3.  <span data-ttu-id="f8cb6-200">Создайте экземпляр класса, который представляет постоянный потребитель событий, который вы хотите использовать.</span><span class="sxs-lookup"><span data-stu-id="f8cb6-200">Create an instance of the class that represents the permanent event consumer you want to use.</span></span>

    <span data-ttu-id="f8cb6-201">Классы потребителей событий являются производными от класса [**\_ \_ евентконсумер**](--eventconsumer.md).</span><span class="sxs-lookup"><span data-stu-id="f8cb6-201">Event consumer classes are derived from the class [**\_\_EventConsumer**](--eventconsumer.md).</span></span> <span data-ttu-id="f8cb6-202">Задайте свойства, необходимые для экземпляра потребителя событий.</span><span class="sxs-lookup"><span data-stu-id="f8cb6-202">Set the properties that the event consumer instance requires.</span></span>

4.  <span data-ttu-id="f8cb6-203">Зарегистрируйте потребитель в COM с помощью программы **regsvr32** .</span><span class="sxs-lookup"><span data-stu-id="f8cb6-203">Register the consumer with COM by using the **regsvr32** utility.</span></span>
5.  <span data-ttu-id="f8cb6-204">Создайте экземпляр класса фильтра событий [**\_ \_ EventFilter**](--eventfilter.md).</span><span class="sxs-lookup"><span data-stu-id="f8cb6-204">Create an instance of the event filter class [**\_\_EventFilter**](--eventfilter.md).</span></span>

    <span data-ttu-id="f8cb6-205">Задайте обязательные поля для экземпляра фильтра событий.</span><span class="sxs-lookup"><span data-stu-id="f8cb6-205">Set the required fields for the event filter instance.</span></span> <span data-ttu-id="f8cb6-206">Обязательные поля для [**\_ \_ EventFilter**](--eventfilter.md) : **Name**, **куерилангуаже** и **Query**.</span><span class="sxs-lookup"><span data-stu-id="f8cb6-206">The required fields for [**\_\_EventFilter**](--eventfilter.md) are **Name**, **QueryLanguage**, and **Query**.</span></span> <span data-ttu-id="f8cb6-207">Свойство **Name** может быть любым уникальным именем для экземпляра этого класса.</span><span class="sxs-lookup"><span data-stu-id="f8cb6-207">The **Name** property can be any unique name for an instance of this class.</span></span> <span data-ttu-id="f8cb6-208">Свойству **куерилангуаже** всегда присвоено значение WQL.</span><span class="sxs-lookup"><span data-stu-id="f8cb6-208">The **QueryLanguage** property is always set to "WQL".</span></span> <span data-ttu-id="f8cb6-209">Свойство **Query** представляет собой строку, содержащую запрос события.</span><span class="sxs-lookup"><span data-stu-id="f8cb6-209">The **Query** property is a string that contains an event query.</span></span> <span data-ttu-id="f8cb6-210">Событие создается при сбое запроса непостоянного потребителя событий.</span><span class="sxs-lookup"><span data-stu-id="f8cb6-210">An event is generated when a permanent event consumer's query fails.</span></span> <span data-ttu-id="f8cb6-211">Источник события — WinMgmt, идентификатор события — 10, а тип события — ошибка.</span><span class="sxs-lookup"><span data-stu-id="f8cb6-211">The event's source is WinMgmt, the event ID is 10, and the event type is Error.</span></span>

6.  <span data-ttu-id="f8cb6-212">Создайте экземпляр класса [**\_ \_ филтертоконсумербиндинг**](--filtertoconsumerbinding.md) , чтобы связать логический объект-получатель события с фильтром событий.</span><span class="sxs-lookup"><span data-stu-id="f8cb6-212">Create an instance of the [**\_\_FilterToConsumerBinding**](--filtertoconsumerbinding.md) class to associate a logical event consumer with an event filter.</span></span>

    <span data-ttu-id="f8cb6-213">Инструментарий WMI использует ассоциацию для поиска объекта-получателя события, связанного с событием, которое соответствует критериям, заданным в фильтре событий.</span><span class="sxs-lookup"><span data-stu-id="f8cb6-213">WMI uses an association to find the event consumer associated with the event that matches the criteria specified in the event filter.</span></span> <span data-ttu-id="f8cb6-214">WMI использует поставщик потребителей событий, чтобы найти постоянное приложение-потребитель событий для запуска.</span><span class="sxs-lookup"><span data-stu-id="f8cb6-214">WMI uses the event consumer provider to find the permanent event consumer application to start.</span></span>

 

 
