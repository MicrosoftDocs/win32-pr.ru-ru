---
description: Объект Свбемсинк реализуется клиентскими приложениями для получения результатов асинхронных операций и уведомлений о событиях.
ms.assetid: a90777ef-fa26-4bfb-b196-c083a0c92a29
ms.tgt_platform: multiple
title: Объект Свбемсинк (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemSink
- ISWbemSinkEvents
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: b8007b7387a09e31f49dbc833f657bc959ee11e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711615"
---
# <a name="swbemsink-object"></a><span data-ttu-id="b8207-103">Объект Свбемсинк</span><span class="sxs-lookup"><span data-stu-id="b8207-103">SWbemSink object</span></span>

<span data-ttu-id="b8207-104">Объект **свбемсинк** реализуется клиентскими приложениями для получения результатов асинхронных операций и уведомлений о событиях.</span><span class="sxs-lookup"><span data-stu-id="b8207-104">The **SWbemSink** object is implemented by client applications to receive the results of asynchronous operations and event notifications.</span></span> <span data-ttu-id="b8207-105">Чтобы выполнить асинхронный вызов, необходимо создать экземпляр объекта **свбемсинк** и передать его в качестве параметра *обжвбемсинк* .</span><span class="sxs-lookup"><span data-stu-id="b8207-105">To make an asynchronous call, you must create an instance of an **SWbemSink** object and pass it as the *ObjWbemSink* parameter.</span></span> <span data-ttu-id="b8207-106">События в реализации **свбемсинк** запускаются при возвращении состояния или результатов, а также после завершения вызова.</span><span class="sxs-lookup"><span data-stu-id="b8207-106">The events in your implementation of **SWbemSink** are triggered when status or results are returned, or when the call is complete.</span></span> <span data-ttu-id="b8207-107">Вызов функции **CreateObject** VBScript создает этот объект.</span><span class="sxs-lookup"><span data-stu-id="b8207-107">The VBScript **CreateObject** call creates this object.</span></span>

## <a name="members"></a><span data-ttu-id="b8207-108">Элементы</span><span class="sxs-lookup"><span data-stu-id="b8207-108">Members</span></span>

<span data-ttu-id="b8207-109">Объект **свбемсинк** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="b8207-109">The **SWbemSink** object has these types of members:</span></span>

-   [<span data-ttu-id="b8207-110">Методы</span><span class="sxs-lookup"><span data-stu-id="b8207-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="b8207-111">Методы</span><span class="sxs-lookup"><span data-stu-id="b8207-111">Methods</span></span>

<span data-ttu-id="b8207-112">Объект **свбемсинк** содержит эти методы.</span><span class="sxs-lookup"><span data-stu-id="b8207-112">The **SWbemSink** object has these methods.</span></span>



| <span data-ttu-id="b8207-113">Метод</span><span class="sxs-lookup"><span data-stu-id="b8207-113">Method</span></span>                             | <span data-ttu-id="b8207-114">Описание</span><span class="sxs-lookup"><span data-stu-id="b8207-114">Description</span></span>                                                                        |
|:-----------------------------------|:-----------------------------------------------------------------------------------|
| [<span data-ttu-id="b8207-115">**Отменить**</span><span class="sxs-lookup"><span data-stu-id="b8207-115">**Cancel**</span></span>](swbemsink-cancel.md) | <span data-ttu-id="b8207-116">Отменяет все асинхронные операции, связанные с этим приемником.</span><span class="sxs-lookup"><span data-stu-id="b8207-116">Cancels all asynchronous operations that are associated with this sink.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="b8207-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b8207-117">Remarks</span></span>

<span data-ttu-id="b8207-118">Асинхронный обратный вызов позволяет пользователю без проверки подлинности предоставлять данные в приемник.</span><span class="sxs-lookup"><span data-stu-id="b8207-118">An asynchronous callback allows a non-authenticated user to provide data to the sink.</span></span> <span data-ttu-id="b8207-119">Это создает угрозы безопасности для сценариев и приложений.</span><span class="sxs-lookup"><span data-stu-id="b8207-119">This poses security risks to your scripts and applications.</span></span> <span data-ttu-id="b8207-120">Чтобы устранить риски, используйте либо семисинчронаус связь, либо синхронное взаимодействие.</span><span class="sxs-lookup"><span data-stu-id="b8207-120">To eliminate the risks, use either semisynchronous communication or synchronous communication.</span></span> <span data-ttu-id="b8207-121">Дополнительные сведения см. [в разделе вызов метода](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="b8207-121">For more information, see [Calling a Method](calling-a-method.md).</span></span>

### <a name="events"></a><span data-ttu-id="b8207-122">События</span><span class="sxs-lookup"><span data-stu-id="b8207-122">Events</span></span>

<span data-ttu-id="b8207-123">Можно реализовать подпрограммы, которые будут вызываться при запуске событий.</span><span class="sxs-lookup"><span data-stu-id="b8207-123">You can implement subroutines to be called when events are triggered.</span></span> <span data-ttu-id="b8207-124">Например, если требуется обработать каждый объект, возвращаемый асинхронным вызовом запроса, например [**SWbemServices.Exeккуерясинк**](swbemservices-execqueryasync.md), создайте подпрограммы с помощью приемника, указанного в асинхронном вызове, как показано в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="b8207-124">For example, if you want to process each object that is returned by an asynchronous query call such as [**SWbemServices.ExecQueryAsync**](swbemservices-execqueryasync.md), create a subroutine using the sink that is specified in the asynchronous call, as shown in the following example.</span></span>


```VB
Sub SinkName_OnObjectReady(objObject, objAsyncContext)
```



<span data-ttu-id="b8207-125">Используйте следующую таблицу в качестве ссылки для задания событий и описаний триггеров.</span><span class="sxs-lookup"><span data-stu-id="b8207-125">Use the following table as a reference to identify events and trigger descriptions.</span></span>



| <span data-ttu-id="b8207-126">Событие</span><span class="sxs-lookup"><span data-stu-id="b8207-126">Event</span></span>                                            | <span data-ttu-id="b8207-127">Описание</span><span class="sxs-lookup"><span data-stu-id="b8207-127">Description</span></span>                                                             |
|--------------------------------------------------|-------------------------------------------------------------------------|
| [<span data-ttu-id="b8207-128">**OnCompleted**</span><span class="sxs-lookup"><span data-stu-id="b8207-128">**OnCompleted**</span></span>](swbemsink-oncompleted.md)     | <span data-ttu-id="b8207-129">Активируется после завершения асинхронной операции.</span><span class="sxs-lookup"><span data-stu-id="b8207-129">Triggered when an asynchronous operation is complete.</span></span>                   |
| [<span data-ttu-id="b8207-130">**онобжектпут**</span><span class="sxs-lookup"><span data-stu-id="b8207-130">**OnObjectPut**</span></span>](swbemsink-onobjectput.md)     | <span data-ttu-id="b8207-131">Активируется при завершении асинхронной операции размещения.</span><span class="sxs-lookup"><span data-stu-id="b8207-131">Triggered when an asynchronous Put operation is complete.</span></span>               |
| [<span data-ttu-id="b8207-132">**онобжектреади**</span><span class="sxs-lookup"><span data-stu-id="b8207-132">**OnObjectReady**</span></span>](swbemsink-onobjectready.md) | <span data-ttu-id="b8207-133">Активируется, когда доступен объект, предоставленный асинхронным вызовом.</span><span class="sxs-lookup"><span data-stu-id="b8207-133">Triggered when an object provided by an asynchronous call is available.</span></span> |
| [<span data-ttu-id="b8207-134">**OnProgress**</span><span class="sxs-lookup"><span data-stu-id="b8207-134">**OnProgress**</span></span>](swbemsink-onprogress.md)       | <span data-ttu-id="b8207-135">Активируется для предоставления состояния асинхронной операции.</span><span class="sxs-lookup"><span data-stu-id="b8207-135">Triggered to provide the status of a asynchronous operation.</span></span>            |



 

<span data-ttu-id="b8207-136">**Асинхронное получение статистики журнала событий**</span><span class="sxs-lookup"><span data-stu-id="b8207-136">**Asynchronously Retrieving Event Log Statistics**</span></span>

<span data-ttu-id="b8207-137">Инструментарий WMI поддерживает как асинхронные, так и частично Синхронные сценарии.</span><span class="sxs-lookup"><span data-stu-id="b8207-137">WMI supports both asynchronous and semi-synchronous scripts.</span></span> <span data-ttu-id="b8207-138">При получении событий из журналов событий асинхронные скрипты часто извлекают эти данные гораздо быстрее.</span><span class="sxs-lookup"><span data-stu-id="b8207-138">When retrieving events from the event logs, asynchronous scripts often retrieve this data much faster.</span></span>

<span data-ttu-id="b8207-139">В асинхронном скрипте выдается запрос, и управление немедленно возвращается в скрипт.</span><span class="sxs-lookup"><span data-stu-id="b8207-139">In an asynchronous script, a query is issued and control is immediately returned to the script.</span></span> <span data-ttu-id="b8207-140">Запрос по-своему обрабатывается в отдельном потоке, а скрипт начинает немедленно реагировать на возвращаемые сведения.</span><span class="sxs-lookup"><span data-stu-id="b8207-140">The query continues to process on a separate thread while the script begins to immediately act on the information that is returned.</span></span> <span data-ttu-id="b8207-141">Асинхронные скрипты управляются событиями: при каждом извлечении записи события срабатывает событие Онобжектреади.</span><span class="sxs-lookup"><span data-stu-id="b8207-141">Asynchronous scripts are event driven: each time an event record is retrieved, the OnObjectReady event is fired.</span></span> <span data-ttu-id="b8207-142">По завершении запроса будет срабатывать событие OnComplete, и скрипт может продолжаться в зависимости от того факта, что были возвращены все доступные записи.</span><span class="sxs-lookup"><span data-stu-id="b8207-142">When the query has completed, the OnCompleted event will fire, and the script can continue based on the fact that all the available records have been returned.</span></span>

<span data-ttu-id="b8207-143">В частично синхронном сценарии, напротив, выдается запрос, а затем сценарий помещает в очередь большой объем извлеченных сведений, прежде чем реагировать на нее.</span><span class="sxs-lookup"><span data-stu-id="b8207-143">In a semi-synchronous script, by contrast, a query is issued and the script then queues a large amount of retrieved information before acting upon it.</span></span> <span data-ttu-id="b8207-144">Для многих объектов достаточно частично синхронной обработки. Например, при запросах к диску для его свойств может существовать только промежуток времени между моментом выдачи запроса и временем возврата и обработки информации.</span><span class="sxs-lookup"><span data-stu-id="b8207-144">For many objects, semi-synchronous processing is adequate; for example, when querying a disk drive for its properties, there might be only a split second between the time the query is issued and the time the information is returned and acted upon.</span></span> <span data-ttu-id="b8207-145">Это связано с тем, что объем возвращаемой информации относительно невелик.</span><span class="sxs-lookup"><span data-stu-id="b8207-145">This is due in large part to the fact that the amount of information returned is relatively small.</span></span>

<span data-ttu-id="b8207-146">Однако при запросе к журналу событий интервал между моментом выдачи запроса и временем, когда односинхронный сценарий может завершиться возвратом и обработкой данных, может занять несколько часов.</span><span class="sxs-lookup"><span data-stu-id="b8207-146">When querying an event log, however, the interval between the time the query is issued and the time that a semi-synchronous script can finish returning and acting on the information can take hours.</span></span> <span data-ttu-id="b8207-147">С поверх этого сценарий может завершиться нехваткой памяти и создать ошибку самостоятельно, прежде чем завершить работу.</span><span class="sxs-lookup"><span data-stu-id="b8207-147">On top of that, the script might run out of memory and fail on its own before completing.</span></span>

<span data-ttu-id="b8207-148">Для журналов событий с большим количеством записей разница во времени обработки может быть значительной.</span><span class="sxs-lookup"><span data-stu-id="b8207-148">For event logs with a large number of records, the difference in processing time can be considerable.</span></span> <span data-ttu-id="b8207-149">На тестовом компьютере под управлением Windows 2000 с 2 000 записями в журнале событий синхронный запрос, который извлекает все события и отображает их в окне командной строки, занял 10 минут 45 секунд.</span><span class="sxs-lookup"><span data-stu-id="b8207-149">On a Windows 2000-based test computer with 2,000 records in the event log, a semi-synchronous query that retrieved all the events and displayed them in a command window took 10 minutes 45 seconds.</span></span> <span data-ttu-id="b8207-150">Асинхронный запрос, выполняющий одну и ту же операцию, занял одну минуту 54 секунд.</span><span class="sxs-lookup"><span data-stu-id="b8207-150">An asynchronous query that performed the same operation took one minute 54 seconds.</span></span>

## <a name="examples"></a><span data-ttu-id="b8207-151">Примеры</span><span class="sxs-lookup"><span data-stu-id="b8207-151">Examples</span></span>

<span data-ttu-id="b8207-152">Следующий сценарий VBScript асинхронно запрашивает журналы событий для всех записей.</span><span class="sxs-lookup"><span data-stu-id="b8207-152">The following VBScript asynchronously queries the event logs for all records.</span></span>


```VB
Const POPUP_DURATION = 10
Const OK_BUTTON = 0
Set objWSHShell = Wscript.CreateObject("Wscript.Shell")
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
 & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set objSink = WScript.CreateObject("WbemScripting.SWbemSink","SINK_")
objWMIService.InstancesOfAsync objSink, "Win32_NTLogEvent"
errReturn = objWshShell.Popup("Retrieving events", POPUP_DURATION, _
"Event Retrieval", OK_BUTTON)
Sub SINK_OnCompleted(iHResult, objErrorObject, objAsyncContext)
 WScript.Echo "Asynchronous operation is done."
End Sub
Sub SINK_OnObjectReady(objEvent, objAsyncContext)
 Wscript.Echo "Category: " & objEvent.Category
 Wscript.Echo "Computer Name: " & objEvent.ComputerName
 Wscript.Echo "Event Code: " & objEvent.EventCode
 Wscript.Echo "Message: " & objEvent.Message
 Wscript.Echo "Record Number: " & objEvent.RecordNumber
 Wscript.Echo "Source Name: " & objEvent.SourceName
 Wscript.Echo "Time Written: " & objEvent.TimeWritten
 Wscript.Echo "Event Type: " & objEvent.Type
 Wscript.Echo "User: " & objEvent.User
End Sub
```



## <a name="requirements"></a><span data-ttu-id="b8207-153">Требования</span><span class="sxs-lookup"><span data-stu-id="b8207-153">Requirements</span></span>



| <span data-ttu-id="b8207-154">Требование</span><span class="sxs-lookup"><span data-stu-id="b8207-154">Requirement</span></span> | <span data-ttu-id="b8207-155">Значение</span><span class="sxs-lookup"><span data-stu-id="b8207-155">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b8207-156">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b8207-156">Minimum supported client</span></span><br/> | <span data-ttu-id="b8207-157">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b8207-157">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b8207-158">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b8207-158">Minimum supported server</span></span><br/> | <span data-ttu-id="b8207-159">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b8207-159">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b8207-160">Header</span><span class="sxs-lookup"><span data-stu-id="b8207-160">Header</span></span><br/>                   | <dl> <span data-ttu-id="b8207-161"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="b8207-161"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="b8207-162">IDL</span><span class="sxs-lookup"><span data-stu-id="b8207-162">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b8207-163"><dt>Wbemdisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b8207-163"><dt>Wbemdisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="b8207-164">DLL</span><span class="sxs-lookup"><span data-stu-id="b8207-164">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b8207-165"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b8207-165"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="b8207-166">CLSID</span><span class="sxs-lookup"><span data-stu-id="b8207-166">CLSID</span></span><br/>                    | <span data-ttu-id="b8207-167">\_СВБЕМСИНК CLSID</span><span class="sxs-lookup"><span data-stu-id="b8207-167">CLSID\_SWbemSink</span></span><br/> <span data-ttu-id="b8207-168">\_СВБЕМСИНКЕВЕНТС CLSID</span><span class="sxs-lookup"><span data-stu-id="b8207-168">CLSID\_SWbemSinkEvents</span></span><br/>                           |
| <span data-ttu-id="b8207-169">IID</span><span class="sxs-lookup"><span data-stu-id="b8207-169">IID</span></span><br/>                      | <span data-ttu-id="b8207-170">IID \_ исвбемсинк</span><span class="sxs-lookup"><span data-stu-id="b8207-170">IID\_ISWbemSink</span></span><br/> <span data-ttu-id="b8207-171">IID \_ исвбемсинкевентс</span><span class="sxs-lookup"><span data-stu-id="b8207-171">IID\_ISWbemSinkEvents</span></span><br/>                             |



## <a name="see-also"></a><span data-ttu-id="b8207-172">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b8207-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8207-173">Создание скриптов для объектов API</span><span class="sxs-lookup"><span data-stu-id="b8207-173">Scripting API Objects</span></span>](scripting-api-objects.md)
</dt> </dl>

 

 




