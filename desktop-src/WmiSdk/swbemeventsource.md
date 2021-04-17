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
# <a name="swbemeventsource-object"></a><span data-ttu-id="5ef0d-103">Объект Свбемевентсаурце</span><span class="sxs-lookup"><span data-stu-id="5ef0d-103">SWbemEventSource object</span></span>

<span data-ttu-id="5ef0d-104">Объект **свбемевентсаурце** извлекает события из запроса события в сочетании с [**SWbemServices.Exeкнотификатионкуери**](swbemservices-execnotificationquery.md).</span><span class="sxs-lookup"><span data-stu-id="5ef0d-104">The **SWbemEventSource** object retrieves events from an event query in conjunction with [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md).</span></span> <span data-ttu-id="5ef0d-105">При вызове **SWbemServices.Exeкнотификатионкуери** для создания запроса события вы получаете объект **свбемевентсаурце** .</span><span class="sxs-lookup"><span data-stu-id="5ef0d-105">You get an **SWbemEventSource** object if you make a call to **SWbemServices.ExecNotificationQuery** to make an event query.</span></span> <span data-ttu-id="5ef0d-106">Затем можно использовать метод [**некстевент**](swbemeventsource-nextevent.md) для получения событий по мере их поступления.</span><span class="sxs-lookup"><span data-stu-id="5ef0d-106">You can then use the [**NextEvent**](swbemeventsource-nextevent.md) method to retrieve events as they arrive.</span></span> <span data-ttu-id="5ef0d-107">Не удается создать этот объект с [помощью вызова функции](/previous-versions//xzysf6hc(v=vs.85)) VBScript.</span><span class="sxs-lookup"><span data-stu-id="5ef0d-107">This object cannot be created by the VBScript [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) call.</span></span>

## <a name="members"></a><span data-ttu-id="5ef0d-108">Элементы</span><span class="sxs-lookup"><span data-stu-id="5ef0d-108">Members</span></span>

<span data-ttu-id="5ef0d-109">Объект **свбемевентсаурце** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="5ef0d-109">The **SWbemEventSource** object has these types of members:</span></span>

-   [<span data-ttu-id="5ef0d-110">Методы</span><span class="sxs-lookup"><span data-stu-id="5ef0d-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="5ef0d-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="5ef0d-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="5ef0d-112">Методы</span><span class="sxs-lookup"><span data-stu-id="5ef0d-112">Methods</span></span>

<span data-ttu-id="5ef0d-113">Объект **свбемевентсаурце** содержит эти методы.</span><span class="sxs-lookup"><span data-stu-id="5ef0d-113">The **SWbemEventSource** object has these methods.</span></span>



| <span data-ttu-id="5ef0d-114">Метод</span><span class="sxs-lookup"><span data-stu-id="5ef0d-114">Method</span></span>                                          | <span data-ttu-id="5ef0d-115">Описание</span><span class="sxs-lookup"><span data-stu-id="5ef0d-115">Description</span></span>                                                                                                                                  |
|:------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5ef0d-116">**некстевент**</span><span class="sxs-lookup"><span data-stu-id="5ef0d-116">**NextEvent**</span></span>](swbemeventsource-nextevent.md) | <span data-ttu-id="5ef0d-117">Используется для получения события в сочетании с [**SWbemServices.Exeкнотификатионкуери**](swbemservices-execnotificationquery.md).</span><span class="sxs-lookup"><span data-stu-id="5ef0d-117">Used to retrieve an event in conjunction with [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md).</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="5ef0d-118">Свойства</span><span class="sxs-lookup"><span data-stu-id="5ef0d-118">Properties</span></span>

<span data-ttu-id="5ef0d-119">Объект **свбемевентсаурце** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="5ef0d-119">The **SWbemEventSource** object has these properties.</span></span>



| <span data-ttu-id="5ef0d-120">Свойство</span><span class="sxs-lookup"><span data-stu-id="5ef0d-120">Property</span></span>                                                    | <span data-ttu-id="5ef0d-121">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="5ef0d-121">Access type</span></span>          | <span data-ttu-id="5ef0d-122">Описание</span><span class="sxs-lookup"><span data-stu-id="5ef0d-122">Description</span></span>                                              |
|:------------------------------------------------------------|:---------------------|:---------------------------------------------------------|
| [<span data-ttu-id="5ef0d-123">**Безопасность\_**</span><span class="sxs-lookup"><span data-stu-id="5ef0d-123">**Security\_**</span></span>](swbemeventsource-security-.md)<br/> | <span data-ttu-id="5ef0d-124">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="5ef0d-124">Read-only</span></span><br/> | <span data-ttu-id="5ef0d-125">Используется для чтения или изменения параметров безопасности.</span><span class="sxs-lookup"><span data-stu-id="5ef0d-125">Used to read or change the security settings.</span></span><br/> |



 

## <a name="examples"></a><span data-ttu-id="5ef0d-126">Примеры</span><span class="sxs-lookup"><span data-stu-id="5ef0d-126">Examples</span></span>

<span data-ttu-id="5ef0d-127">Этот скрипт использует методы класса **свбемевентсаурце** и класс [**SwbemServices**](swbemservices.md) в сочетании с WQL-запросом для событий приложения.</span><span class="sxs-lookup"><span data-stu-id="5ef0d-127">This script uses the methods of the **SWbemEventSource** class and the [**SWbemServices**](swbemservices.md) class in conjunction with a WQL query for application events.</span></span> <span data-ttu-id="5ef0d-128">Дополнительные сведения об уведомлениях о событиях WMI и запросах см. в разделе [мониторинг событий](monitoring-events.md), [выполнение сценария на основе события](running-a-script-based-on-an-event.md)и [Получение асинхронных уведомлений о событиях](receiving-asynchronous-event-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="5ef0d-128">For more information about WMI event notification and queries see [Monitoring Events](monitoring-events.md), [Running a Script Based on an Event](running-a-script-based-on-an-event.md), and [Receiving Asynchronous Event Notifications](receiving-asynchronous-event-notifications.md).</span></span>


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



## <a name="requirements"></a><span data-ttu-id="5ef0d-129">Требования</span><span class="sxs-lookup"><span data-stu-id="5ef0d-129">Requirements</span></span>



| <span data-ttu-id="5ef0d-130">Требование</span><span class="sxs-lookup"><span data-stu-id="5ef0d-130">Requirement</span></span> | <span data-ttu-id="5ef0d-131">Значение</span><span class="sxs-lookup"><span data-stu-id="5ef0d-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5ef0d-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5ef0d-132">Minimum supported client</span></span><br/> | <span data-ttu-id="5ef0d-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5ef0d-133">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5ef0d-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5ef0d-134">Minimum supported server</span></span><br/> | <span data-ttu-id="5ef0d-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5ef0d-135">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5ef0d-136">Header</span><span class="sxs-lookup"><span data-stu-id="5ef0d-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="5ef0d-137"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="5ef0d-137"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="5ef0d-138">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="5ef0d-138">Type library</span></span><br/>             | <dl> <span data-ttu-id="5ef0d-139"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="5ef0d-139"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="5ef0d-140">DLL</span><span class="sxs-lookup"><span data-stu-id="5ef0d-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5ef0d-141"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5ef0d-141"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="5ef0d-142">CLSID</span><span class="sxs-lookup"><span data-stu-id="5ef0d-142">CLSID</span></span><br/>                    | <span data-ttu-id="5ef0d-143">\_СВБЕМЕВЕНТСАУРЦЕ CLSID</span><span class="sxs-lookup"><span data-stu-id="5ef0d-143">CLSID\_SWbemEventSource</span></span><br/>                                                      |
| <span data-ttu-id="5ef0d-144">IID</span><span class="sxs-lookup"><span data-stu-id="5ef0d-144">IID</span></span><br/>                      | <span data-ttu-id="5ef0d-145">IID \_ исвбемевентсаурце</span><span class="sxs-lookup"><span data-stu-id="5ef0d-145">IID\_ISWbemEventSource</span></span><br/>                                                       |



## <a name="see-also"></a><span data-ttu-id="5ef0d-146">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5ef0d-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ef0d-147">Создание скриптов для объектов API</span><span class="sxs-lookup"><span data-stu-id="5ef0d-147">Scripting API Objects</span></span>](scripting-api-objects.md)
</dt> </dl>

 

