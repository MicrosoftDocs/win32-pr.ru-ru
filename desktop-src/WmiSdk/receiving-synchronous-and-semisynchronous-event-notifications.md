---
description: Используйте SWbemServices.ExeКкуери, чтобы запросить все существующие события.
ms.assetid: bc99719a-7e33-4e2d-8355-f8fc97c66f71
ms.tgt_platform: multiple
title: Получение синхронных и Семисинчронаус уведомлений о событиях
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15327c66f7ba3e59824c94d54a206ec348c85952
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693270"
---
# <a name="receiving-synchronous-and-semisynchronous-event-notifications"></a><span data-ttu-id="818b3-103">Получение синхронных и Семисинчронаус уведомлений о событиях</span><span class="sxs-lookup"><span data-stu-id="818b3-103">Receiving Synchronous and Semisynchronous Event Notifications</span></span>

<span data-ttu-id="818b3-104">Используйте [**SWbemServices.Exeккуери**](swbemservices-execquery.md) , чтобы запросить все существующие события.</span><span class="sxs-lookup"><span data-stu-id="818b3-104">Use [**SWbemServices.ExecQuery**](swbemservices-execquery.md) to request all existing events.</span></span>

<span data-ttu-id="818b3-105">В следующем примере кода показано, как запросить события в журнале.</span><span class="sxs-lookup"><span data-stu-id="818b3-105">The following code example shows how to query for the events in a log.</span></span>

`Select * from Win32_NTLogEvent`

<span data-ttu-id="818b3-106">Дополнительные сведения см. в статьях [Определение типа получаемого события](determining-the-type-of-event-to-receive.md), [Получение уведомлений о событиях](receiving-event-notifications.md)и [WQL (SQL для WMI)](wql-sql-for-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="818b3-106">For more information, see [Determining the Type of Event to Receive](determining-the-type-of-event-to-receive.md), [Receiving Event Notifications](receiving-event-notifications.md), and [WQL (SQL for WMI)](wql-sql-for-wmi.md).</span></span>

<span data-ttu-id="818b3-107">При вызове [**SWbemServices.Exeкнотификатионкуери**](swbemservices-execnotificationquery.md) по умолчанию используется обмен данными семисинчронаус.</span><span class="sxs-lookup"><span data-stu-id="818b3-107">The default call to [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md) uses semisynchronous communication.</span></span> <span data-ttu-id="818b3-108">По умолчанию для параметра *ифлагс* заданы флаги **вбемфлагфорвардонли** и **вбемфлагретурниммедиатели** .</span><span class="sxs-lookup"><span data-stu-id="818b3-108">The *iflags* parameter has the **wbemFlagForwardOnly** and **wbemFlagReturnImmediately** flags set by default.</span></span> <span data-ttu-id="818b3-109">Дополнительные сведения см. [в разделе вызов метода](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="818b3-109">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="818b3-110">В следующей процедуре описывается получение уведомления о событии семисинчронаус с помощью VBScript.</span><span class="sxs-lookup"><span data-stu-id="818b3-110">The following procedure describes how to receive semisynchronous event notification using VBScript.</span></span>

<span data-ttu-id="818b3-111">**Получение уведомления о событии семисинчронаус в VBScript**</span><span class="sxs-lookup"><span data-stu-id="818b3-111">**To receive semisynchronous event notification in VBScript**</span></span>

1.  <span data-ttu-id="818b3-112">Создайте запрос для типа события, которое требуется получить.</span><span class="sxs-lookup"><span data-stu-id="818b3-112">Create a query for the type of event that you want to receive.</span></span> <span data-ttu-id="818b3-113">Дополнительные сведения см. [в разделе Определение типа получаемого события](determining-the-type-of-event-to-receive.md).</span><span class="sxs-lookup"><span data-stu-id="818b3-113">For more information, see [Determining the Type of Event to Receive](determining-the-type-of-event-to-receive.md).</span></span>

2.  <span data-ttu-id="818b3-114">Если вы запрашиваете тип экземпляра события, например [**\_ \_ инстанцекреатионевент**](--instancecreationevent.md), укажите в запросе тип целевого экземпляра, например [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk).</span><span class="sxs-lookup"><span data-stu-id="818b3-114">If you request an instance type of event such as [**\_\_InstanceCreationEvent**](--instancecreationevent.md), indicate in the query a type of target instance, for example, [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk).</span></span>

3.  <span data-ttu-id="818b3-115">При необходимости укажите экземпляр, например имя пространства имен при запросе будущих экземпляров [**\_ \_ намеспацемодификатионевент**](--namespacemodificationevent.md) для определенного пространства имен.</span><span class="sxs-lookup"><span data-stu-id="818b3-115">If necessary, specify an instance, for example, the name of a namespace when requesting future [**\_\_NamespaceModificationEvent**](--namespacemodificationevent.md) instances for a specific namespace.</span></span>

4.  <span data-ttu-id="818b3-116">Укажите интервал опроса для инструментарий управления Windows (WMI) (WMI) в запросе, например "в течение 10", для опроса каждые 10 секунд.</span><span class="sxs-lookup"><span data-stu-id="818b3-116">Specify a polling interval for Windows Management Instrumentation (WMI) in a query, such as "WITHIN 10"—to poll every 10 seconds.</span></span> <span data-ttu-id="818b3-117">Дополнительные сведения см. [в разделе предложение внутри](within-clause.md).</span><span class="sxs-lookup"><span data-stu-id="818b3-117">For more information, see [WITHIN Clause](within-clause.md).</span></span>

5.  <span data-ttu-id="818b3-118">Вызовите [**SWbemServices.Exeкнотификатионкуери**](swbemservices-execnotificationquery.md) с помощью запроса.</span><span class="sxs-lookup"><span data-stu-id="818b3-118">Call [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md) using the query.</span></span>

6.  <span data-ttu-id="818b3-119">Перебрать полученную коллекцию.</span><span class="sxs-lookup"><span data-stu-id="818b3-119">Loop through the collection you receive.</span></span>

<span data-ttu-id="818b3-120">В следующем примере показано, как отслеживать вставку и удаление дисков с дисковода гибких дисков на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="818b3-120">The following example shows how to monitor insertion and removal of disks from a floppy disk drive on a local machine.</span></span> <span data-ttu-id="818b3-121">Сценарий запрашивает \_ экземпляры [**\_ \_ инстанцемодификатионевент**](--instancemodificationevent.md) для экземпляра [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) на гибком диске и опрашивает их каждые 10 секунд для новых экземпляров.</span><span class="sxs-lookup"><span data-stu-id="818b3-121">The script requests \_[**\_\_InstanceModificationEvent**](--instancemodificationevent.md) instances for the floppy drive [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) instance and polls every 10 seconds for new instances.</span></span> <span data-ttu-id="818b3-122">Этот сценарий является примером временного потребителя событий и продолжит выполнение до тех пор, пока оно не будет остановлено в диспетчере задач, или система не будет перезагружена.</span><span class="sxs-lookup"><span data-stu-id="818b3-122">This script is an example of a temporary event consumer, and continues running until it is stopped in Task Manager or the system is rebooted.</span></span> <span data-ttu-id="818b3-123">Дополнительные сведения см. [в статье получение событий в](receiving-events-for-the-duration-of-your-application.md)течение всего приложения.</span><span class="sxs-lookup"><span data-stu-id="818b3-123">For more information, see [Receiving Events for the Duration of your Application](receiving-events-for-the-duration-of-your-application.md).</span></span>


```VB
Const FLOPPY_DISK = 2
Set colMonitoredDisks = GetObject("Winmgmts:").ExecNotificationQuery _
    ("Select * from __InstanceModificationEvent within 10 WHERE " _
        & "TargetInstance ISA 'Win32_LogicalDisk'")
i = 0
Do While i = 0
    Set strDiskChange = colMonitoredDisks.NextEvent
    If strDiskChange.TargetInstance.DriveType = FLOPPY_DISK Then
        If strDiskChange.TargetInstance.Size > 0 Then
            Wscript.Echo "A disk has been inserted" & _
                " into the floppy drive."
    Else
            Wscript.Echo "A disk has been removed" & _
                " from the floppy drive."
        End If
    End If
Loop
```



<span data-ttu-id="818b3-124">В следующей процедуре описывается получение уведомления о событии семисинчронаус с помощью C++.</span><span class="sxs-lookup"><span data-stu-id="818b3-124">The following procedure describes how to receive semisynchronous event notification using C++.</span></span>

<span data-ttu-id="818b3-125">**Получение уведомления о событии семисинчронаус в C++**</span><span class="sxs-lookup"><span data-stu-id="818b3-125">**To receive semisynchronous event notification in C++**</span></span>

1.  <span data-ttu-id="818b3-126">Настройте приложение с помощью вызовов функций [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) и [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) .</span><span class="sxs-lookup"><span data-stu-id="818b3-126">Set up the application with calls to the [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) and [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) functions.</span></span>

    <span data-ttu-id="818b3-127">Поскольку WMI основан на COM, вызов [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) и [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) является обязательным шагом для приложения WMI.</span><span class="sxs-lookup"><span data-stu-id="818b3-127">Because WMI is COM based, calling [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) and [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) is a required step for a WMI application.</span></span> <span data-ttu-id="818b3-128">Дополнительные сведения см. [в разделе Создание приложения WMI или скрипта](creating-a-wmi-application-or-script.md).</span><span class="sxs-lookup"><span data-stu-id="818b3-128">For more information, see [Creating a WMI Application or Script](creating-a-wmi-application-or-script.md).</span></span>

2.  <span data-ttu-id="818b3-129">Определите тип событий, которые требуется получить.</span><span class="sxs-lookup"><span data-stu-id="818b3-129">Determine the kind of events that you want to receive.</span></span>

    <span data-ttu-id="818b3-130">Инструментарий WMI поддерживает внутренние и внешние события.</span><span class="sxs-lookup"><span data-stu-id="818b3-130">WMI supports intrinsic and extrinsic events.</span></span> <span data-ttu-id="818b3-131">Внутреннее событие — это событие, предопределенное WMI.</span><span class="sxs-lookup"><span data-stu-id="818b3-131">An intrinsic event is an event predefined by WMI.</span></span> <span data-ttu-id="818b3-132">Внешнее событие является событием, определенным сторонним поставщиком.</span><span class="sxs-lookup"><span data-stu-id="818b3-132">An extrinsic event is an event defined by a third party provider.</span></span> <span data-ttu-id="818b3-133">Дополнительные сведения см. [в разделе Определение типа получаемого события](determining-the-type-of-event-to-receive.md).</span><span class="sxs-lookup"><span data-stu-id="818b3-133">For more information, see [Determining the Type of Event to Receive](determining-the-type-of-event-to-receive.md).</span></span>

3.  <span data-ttu-id="818b3-134">Зарегистрируйтесь, чтобы получить конкретный класс событий с помощью вызова метода [**IWbemServices:: ексекнотификатионкуери**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery) .</span><span class="sxs-lookup"><span data-stu-id="818b3-134">Register to receive a specific class of events with a call to the [**IWbemServices::ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery) method.</span></span>

    <span data-ttu-id="818b3-135">Сделайте каждый запрос особым.</span><span class="sxs-lookup"><span data-stu-id="818b3-135">Make each query very specific.</span></span> <span data-ttu-id="818b3-136">Целью регистрации является регистрация для получения только необходимых уведомлений.</span><span class="sxs-lookup"><span data-stu-id="818b3-136">The goal of registration is to register to receive only the required notifications.</span></span> <span data-ttu-id="818b3-137">Уведомления, не требующие траты времени на обработку и доставку.</span><span class="sxs-lookup"><span data-stu-id="818b3-137">Notifications that are not required waste processing and delivery time.</span></span>

    <span data-ttu-id="818b3-138">Потребитель событий можно спроектировать для получения нескольких событий.</span><span class="sxs-lookup"><span data-stu-id="818b3-138">You can design an event consumer to receive multiple events.</span></span> <span data-ttu-id="818b3-139">Например, потребителю может потребоваться уведомление о событиях изменения экземпляра для определенного класса событий нарушения безопасности.</span><span class="sxs-lookup"><span data-stu-id="818b3-139">For example, a consumer might require notification of instance modification events for a specific class of device and security violation events.</span></span> <span data-ttu-id="818b3-140">В этом случае задачи, выполняемые потребителем при получении события изменения экземпляра, отличаются для двух событий.</span><span class="sxs-lookup"><span data-stu-id="818b3-140">In this case, the tasks a consumer performs when receiving an instance modification event are different for the two events.</span></span> <span data-ttu-id="818b3-141">Таким образом, потребитель должен выполнить один вызов [**IWbemServices:: ексекнотификатионкуери**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery) , чтобы зарегистрировать события изменения экземпляра, и еще один вызов **ексекнотификатионкуери** для регистрации событий нарушения безопасности.</span><span class="sxs-lookup"><span data-stu-id="818b3-141">Thus, the consumer should make one call to [**IWbemServices::ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery) to register for instance modification events, and another call to **ExecNotificationQuery** to register for security violation events.</span></span>

    <span data-ttu-id="818b3-142">В вызове [**ексекнотификатионкуери**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery)задайте для параметра *лфлагс* значение, чтобы **\_ флаг WBEM \_ возвращался \_ немедленно** , а **флаг WBEM — \_ \_ \_ только вперед**.</span><span class="sxs-lookup"><span data-stu-id="818b3-142">In the call to [**ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery), set the *lFlags* parameter to **WBEM\_FLAG\_RETURN\_IMMEDIATELY** and **WBEM\_FLAG\_FORWARD\_ONLY**.</span></span> <span data-ttu-id="818b3-143">**Флаг WBEM \_ \_ возвращает \_** запросы, Семисинчронаус обработку, и флаг WBEM, показывающий **\_ \_ \_ только** однонаправленный перечислитель.</span><span class="sxs-lookup"><span data-stu-id="818b3-143">The **WBEM\_FLAG\_RETURN\_IMMEDIATELY** flag requests semisynchronous processing, and the **WBEM\_FLAG\_FORWARD\_ONLY** flag requests a forward-only enumerator.</span></span> <span data-ttu-id="818b3-144">Дополнительные сведения см. [в разделе вызов метода](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="818b3-144">For more information, see [Calling a Method](calling-a-method.md).</span></span> <span data-ttu-id="818b3-145">Функция **ексекнотификатионкуери** возвращает указатель на интерфейс [**иенумвбемклассобжект**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) .</span><span class="sxs-lookup"><span data-stu-id="818b3-145">The **ExecNotificationQuery** function returns a pointer to an [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) interface.</span></span>

4.  <span data-ttu-id="818b3-146">Опрос для зарегистрированных уведомлений о событиях путем многократного вызова метода [**иенумвбемклассобжект:: Next**](/windows/desktop/api/Wbemcli/nf-wbemcli-ienumwbemclassobject-next) .</span><span class="sxs-lookup"><span data-stu-id="818b3-146">Poll for registered event notifications by making repeated calls to the [**IEnumWbemClassObject::Next**](/windows/desktop/api/Wbemcli/nf-wbemcli-ienumwbemclassobject-next) method.</span></span>
5.  <span data-ttu-id="818b3-147">По завершении выпустите перечислитель, указывающий на объект [**иенумвбемклассобжект**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) .</span><span class="sxs-lookup"><span data-stu-id="818b3-147">When finished, release the enumerator that points to the [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) object.</span></span>

    <span data-ttu-id="818b3-148">Вы можете освободить указатель [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) , связанный с регистрацией.</span><span class="sxs-lookup"><span data-stu-id="818b3-148">You can release the [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) pointer associated with the registration.</span></span> <span data-ttu-id="818b3-149">Освобождение указателя **IWbemServices** приводит к тому, что инструментарий WMI прекращает доставку событий всем связанным временным потребителям.</span><span class="sxs-lookup"><span data-stu-id="818b3-149">Releasing the **IWbemServices** pointer causes WMI to stop delivering events to all associated temporary consumers.</span></span>

 

 
