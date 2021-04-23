---
description: Для получения уведомлений от поставщика системного реестра приложение управления должно быть зарегистрировано как временный потребитель событий.
ms.assetid: 4cac5fdd-c842-4d7e-a56e-2e1312df68b4
ms.tgt_platform: multiple
title: Регистрация для событий системного реестра
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 886046f5ffef366cdba2efb86629019f2ee0b5e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105703182"
---
# <a name="registering-for-system-registry-events"></a><span data-ttu-id="f4c28-103">Регистрация для событий системного реестра</span><span class="sxs-lookup"><span data-stu-id="f4c28-103">Registering for System Registry Events</span></span>

<span data-ttu-id="f4c28-104">Для получения уведомлений от поставщика [системного реестра](/previous-versions/windows/desktop/regprov/system-registry-provider) приложение управления должно быть зарегистрировано как временный потребитель событий.</span><span class="sxs-lookup"><span data-stu-id="f4c28-104">To receive notifications from the [System Registry](/previous-versions/windows/desktop/regprov/system-registry-provider) provider, a management application must register as a temporary event consumer.</span></span> <span data-ttu-id="f4c28-105">Большинство требований, регистрируемых для поставщика системного реестра, те же, что и при любой регистрации событий, но также необходимо выполнить следующую процедуру.</span><span class="sxs-lookup"><span data-stu-id="f4c28-105">Most of the requirements to register for the System Registry provider are the same as any other event registration, except you must also perform the following procedure.</span></span>

<span data-ttu-id="f4c28-106">Поставщик реестра предоставляет классы событий для событий в системном реестре.</span><span class="sxs-lookup"><span data-stu-id="f4c28-106">The registry provider supplies event classes for events in the system registry.</span></span> <span data-ttu-id="f4c28-107">Дополнительные сведения о регистрации общих событий см. [в разделе Получение WMI-события](receiving-a-wmi-event.md).</span><span class="sxs-lookup"><span data-stu-id="f4c28-107">For more information about general event registration, see [Receiving a WMI Event](receiving-a-wmi-event.md).</span></span>

<span data-ttu-id="f4c28-108">В следующей процедуре описывается регистрация для событий системного реестра.</span><span class="sxs-lookup"><span data-stu-id="f4c28-108">The following procedure describes how to register for system registry events.</span></span>

<span data-ttu-id="f4c28-109">**Регистрация для событий системного реестра**</span><span class="sxs-lookup"><span data-stu-id="f4c28-109">**To register for system registry events**</span></span>

1.  <span data-ttu-id="f4c28-110">Вызов метода запроса уведомления.</span><span class="sxs-lookup"><span data-stu-id="f4c28-110">Call a notification query method.</span></span>

    <span data-ttu-id="f4c28-111">В любом скрипте или C++ используйте запрос уведомления, например [**SWbemServices.Exeкнотификатионкуерясинк**](swbemservices-execnotificationqueryasync.md) или [**IWbemServices:: ExecNotificationQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationqueryasync).</span><span class="sxs-lookup"><span data-stu-id="f4c28-111">In either script or C++, use a notification query such as [**SWbemServices.ExecNotificationQueryAsync**](swbemservices-execnotificationqueryasync.md) or [**IWbemServices::ExecNotificationQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationqueryasync).</span></span> <span data-ttu-id="f4c28-112">Создайте строку запроса для параметра *Бстркуери* **IWbemServices:: ExecNotificationQueryAsync** или *стркуери* в скрипте.</span><span class="sxs-lookup"><span data-stu-id="f4c28-112">Create a query string for the *bstrQuery* parameter of **IWbemServices::ExecNotificationQueryAsync** or the *strQuery* in script.</span></span>

2.  <span data-ttu-id="f4c28-113">Определите тип события, которое требуется получить, и создайте запрос.</span><span class="sxs-lookup"><span data-stu-id="f4c28-113">Determine which type of event you want to receive and create the query.</span></span>

    <span data-ttu-id="f4c28-114">В следующей таблице перечислены классы событий реестра, которые можно использовать.</span><span class="sxs-lookup"><span data-stu-id="f4c28-114">The following table lists the registry event classes that you can use.</span></span>

    

    | <span data-ttu-id="f4c28-115">Класс событий</span><span class="sxs-lookup"><span data-stu-id="f4c28-115">Event class</span></span>                                                      | <span data-ttu-id="f4c28-116">Расположение Hive</span><span class="sxs-lookup"><span data-stu-id="f4c28-116">Hive location</span></span>        | <span data-ttu-id="f4c28-117">Описание</span><span class="sxs-lookup"><span data-stu-id="f4c28-117">Description</span></span>                                                 |
    |------------------------------------------------------------------|----------------------|-------------------------------------------------------------|
    | [<span data-ttu-id="f4c28-118">**регистревент**</span><span class="sxs-lookup"><span data-stu-id="f4c28-118">**RegistryEvent**</span></span>](/previous-versions/windows/desktop/regprov/registryevent)                       | <span data-ttu-id="f4c28-119">Н/Д</span><span class="sxs-lookup"><span data-stu-id="f4c28-119">N/A</span></span><br/>       | <span data-ttu-id="f4c28-120">Абстрактный базовый класс для изменений в реестре.</span><span class="sxs-lookup"><span data-stu-id="f4c28-120">Abstract base class for changes in the registry.</span></span><br/> |
    | [<span data-ttu-id="f4c28-121">**регистритричанжеевент**</span><span class="sxs-lookup"><span data-stu-id="f4c28-121">**RegistryTreeChangeEvent**</span></span>](/previous-versions/windows/desktop/regprov/registrytreechangeevent)   | <span data-ttu-id="f4c28-122">RootPath</span><span class="sxs-lookup"><span data-stu-id="f4c28-122">RootPath</span></span><br/>  | <span data-ttu-id="f4c28-123">Отслеживает изменения в иерархии ключей.</span><span class="sxs-lookup"><span data-stu-id="f4c28-123">Monitors changes to a hierarchy of keys.</span></span><br/>         |
    | [<span data-ttu-id="f4c28-124">**регистрикэйчанжеевент**</span><span class="sxs-lookup"><span data-stu-id="f4c28-124">**RegistryKeyChangeEvent**</span></span>](/previous-versions/windows/desktop/regprov/registrykeychangeevent)     | <span data-ttu-id="f4c28-125">Путь</span><span class="sxs-lookup"><span data-stu-id="f4c28-125">KeyPath</span></span><br/>   | <span data-ttu-id="f4c28-126">Отслеживает изменения в одном ключе.</span><span class="sxs-lookup"><span data-stu-id="f4c28-126">Monitors changes to a single key.</span></span><br/>                |
    | [<span data-ttu-id="f4c28-127">**События registryvaluechangeevent**</span><span class="sxs-lookup"><span data-stu-id="f4c28-127">**RegistryValueChangeEvent**</span></span>](/previous-versions/windows/desktop/regprov/registryvaluechangeevent) | <span data-ttu-id="f4c28-128">ValueName</span><span class="sxs-lookup"><span data-stu-id="f4c28-128">ValueName</span></span><br/> | <span data-ttu-id="f4c28-129">Отслеживает изменения в одном значении.</span><span class="sxs-lookup"><span data-stu-id="f4c28-129">Monitors changes to a single value.</span></span><br/>              |

    

     

    <span data-ttu-id="f4c28-130">Эти классы имеют свойство **Hive** , которое определяет иерархию ключей для отслеживания изменений, таких как **hKey \_ локальный \_ компьютер**.</span><span class="sxs-lookup"><span data-stu-id="f4c28-130">These classes have a property called **Hive** that identifies the hierarchy of keys to be monitored for change, such as **HKEY\_LOCAL\_MACHINE**.</span></span>

    <span data-ttu-id="f4c28-131">Изменения в **\_ классах hKey \_ root** и **hKey \_ текущего \_ пользователя** Hive не поддерживаются [**регистревент**](/previous-versions/windows/desktop/regprov/registryevent) или производными от него классами, например [**регистритричанжеевент**](/previous-versions/windows/desktop/regprov/registrytreechangeevent).</span><span class="sxs-lookup"><span data-stu-id="f4c28-131">Changes to the **HKEY\_CLASSES\_ROOT** and **HKEY\_CURRENT\_USER** hives are not supported by [**RegistryEvent**](/previous-versions/windows/desktop/regprov/registryevent) or classes derived from it, such as [**RegistryTreeChangeEvent**](/previous-versions/windows/desktop/regprov/registrytreechangeevent).</span></span>

3.  <span data-ttu-id="f4c28-132">Создайте предложение WHERE для регистрации событий.</span><span class="sxs-lookup"><span data-stu-id="f4c28-132">Create the WHERE clause for your event registration.</span></span>

    <span data-ttu-id="f4c28-133">Поставщик системного реестра имеет определенные правила для предложений WHERE.</span><span class="sxs-lookup"><span data-stu-id="f4c28-133">The System Registry provider has specific rules for WHERE clauses.</span></span> <span data-ttu-id="f4c28-134">Дополнительные сведения см. в разделе [Создание правильного предложения WHERE для поставщика реестра](creating-a-proper-where-clause-for-the-registry-provider.md).</span><span class="sxs-lookup"><span data-stu-id="f4c28-134">For more information, see [Creating a Proper WHERE Clause for the Registry Provider](creating-a-proper-where-clause-for-the-registry-provider.md).</span></span> <span data-ttu-id="f4c28-135">Дополнительные общие сведения о создании предложения WHERE см. в разделе [запросы с помощью WQL](querying-with-wql.md).</span><span class="sxs-lookup"><span data-stu-id="f4c28-135">For more general information about creating a WHERE clause, see [Querying with WQL](querying-with-wql.md).</span></span>

4.  <span data-ttu-id="f4c28-136">Определите, получает ли потребитель события.</span><span class="sxs-lookup"><span data-stu-id="f4c28-136">Determine whether your consumer is receiving events.</span></span>

    <span data-ttu-id="f4c28-137">Поставщик системного реестра не гарантирует, что все отправленные события будут доставлены.</span><span class="sxs-lookup"><span data-stu-id="f4c28-137">The System Registry provider does not guarantee that all sent events are delivered.</span></span> <span data-ttu-id="f4c28-138">Дополнительные сведения см. в разделе [получение событий реестра](receiving-registry-events.md).</span><span class="sxs-lookup"><span data-stu-id="f4c28-138">For more information, see [Receiving Registry Events](receiving-registry-events.md).</span></span>

<span data-ttu-id="f4c28-139">В следующем примере кода VBScript показано, как определить изменение реестра в **\_ \_** \\  \\ кусте **Microsoft** Hive или поддереве в разделе "программное обеспечение на локальном компьютере".</span><span class="sxs-lookup"><span data-stu-id="f4c28-139">The following VBScript code example shows how to detect a registry change in the **HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft** hive or subtree.</span></span> <span data-ttu-id="f4c28-140">Это скрипт мониторинга, который в демонстрационных целях выполняется в процессе с именем Wscript.exe до тех пор, пока он не будет завершен в **диспетчере задач**, Инструментарий WMI остановлен или операционная система перезагружается.</span><span class="sxs-lookup"><span data-stu-id="f4c28-140">This is a monitoring script that, for demonstration purposes, runs in a process named Wscript.exe until it is terminated in **Task Manager**, WMI is stopped, or the operating system is rebooted.</span></span> <span data-ttu-id="f4c28-141">Скрипт использует вызов [*семисинчронаус*](gloss-s.md) для [**SWbemServices.Exeкнотификатионкуери**](swbemservices-execnotificationquery.md).</span><span class="sxs-lookup"><span data-stu-id="f4c28-141">The script uses a [*semisynchronous*](gloss-s.md) call to [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md).</span></span> <span data-ttu-id="f4c28-142">Дополнительные сведения о вызовах семисинчронаус см. в разделе [выполнение вызова семисинчронаус с помощью VBScript](making-a-semisynchronous-call-with-vbscript.md).</span><span class="sxs-lookup"><span data-stu-id="f4c28-142">For more information about semisynchronous calls, see [Making a Semisynchronous Call with VBScript](making-a-semisynchronous-call-with-vbscript.md).</span></span>


```VB
Set wmiServices = GetObject("winmgmts:root/default") 
Set colTreeChanges = wmiServices.ExecNotificationQuery _
    ("SELECT * FROM RegistryTreeChangeEvent " _
    & "WHERE Hive='HKEY_LOCAL_MACHINE' " _
    & "AND RootPath='SOFTWARE\\Microsoft'")

While (True)
   Set TreeChange = colTreeChanges.NextEvent
   TreeChange.GetObjectText_()
   Wscript.Echo  "Hive = " & TreeChange.Hive & VBNewLine _
      & "RootPath = "& TreeChange.RootPath _
      & TreeChange.GetObjectText_()      
Wend
```



В следующем примере кода VBScript показано, как отслеживать изменение значений ключа путем регистрации для события поставщика реестра типа [**регистрикэйчанжеевент**](/previous-versions/windows/desktop/regprov/registrykeychangeevent). Скрипт вызывает асинхронный метод [**SWbemServices.Exeкнотификатионкуерясинк**](swbemservices-execnotificationqueryasync.md). <span data-ttu-id="f4c28-145">Дополнительные сведения об асинхронных вызовах и безопасности см. [в разделе выполнение асинхронного вызова с помощью VBScript](making-an-asynchronous-call-with-vbscript.md).</span><span class="sxs-lookup"><span data-stu-id="f4c28-145">For more information about asynchronous calls and security, see [Making an Asynchronous Call with VBScript](making-an-asynchronous-call-with-vbscript.md).</span></span>

<span data-ttu-id="f4c28-146">Следующий скрипт выполняется неограниченно до перезагрузки компьютера, Инструментарий WMI остановлен или сценарий остановлен.</span><span class="sxs-lookup"><span data-stu-id="f4c28-146">The following script runs indefinitely until the computer is rebooted, WMI is stopped, or the script is stopped.</span></span> <span data-ttu-id="f4c28-147">Чтобы прерывать выполнение скрипта вручную, используйте диспетчер задач, чтобы прерывать процесс.</span><span class="sxs-lookup"><span data-stu-id="f4c28-147">To stop the script manually, use Task Manager to stop the process.</span></span> <span data-ttu-id="f4c28-148">Чтобы остановить его программно, используйте метод [**Terminate**](/windows/desktop/CIMWin32Prov/terminate-method-in-class-win32-process) в \_ классе процесса Win32.</span><span class="sxs-lookup"><span data-stu-id="f4c28-148">To stop it programmatically, use the [**Terminate**](/windows/desktop/CIMWin32Prov/terminate-method-in-class-win32-process) method in the Win32\_Process class.</span></span>


```VB
strComputer = "."
Set objWMIServices = GetObject("winmgmts:root/default") 
Set wmiSink = WScript.CreateObject( _
    "WbemScripting.SWbemSink", "SINK_") 
Set ObjRegistry = GetObject("winmgmts:_
    {impersonationLevel = impersonate}!\\" _
    & strComputer & "\root\default:StdRegProv")

' Create a new key
strPath = "SOFTWARE\MyKey\MySubKey\"
Return = objRegistry.CreateKey(HKEY_LOCAL_MACHINE, strPath)

' Start listening for change in key
objWMIServices.ExecNotificationQueryAsync wmiSink, _ 
    "SELECT * FROM RegistryKeyChangeEvent " _ 
    & "WHERE Hive='HKEY_LOCAL_MACHINE' AND " _ 
    & "KeyPath='SOFTWARE\\MyKey\\MySubKey\\'" 
WScript.Echo "Listening for Registry Change Events..." 

While(True) 
    WScript.Sleep 1000
' You can use Regedit to make a change in the key 
' HKEY_LOCAL_MACHINE\SOFTWARE\MyKey\MySubKey\ 
'    to see an event generated.
Wend 

Sub SINK_OnObjectReady(EventObject, wmiAsyncContext) 
    WScript.Echo "Received Registry Change Event" & vbCrLf & _
      EventObject.GetObjectText_() 
End Sub
```



 

