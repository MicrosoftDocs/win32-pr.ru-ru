---
description: С помощью инструментария WMI можно программно получать доступ к данным системных счетчиков из объектов в библиотеках производительности.
ms.assetid: a0ed14e9-d2ec-43eb-8c8e-eac3c134ea1d
ms.tgt_platform: multiple
title: Мониторинг данных производительности
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95cee18ba88a8aff920c2d14b5709a0fd913e2ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105647681"
---
# <a name="monitoring-performance-data"></a><span data-ttu-id="7ca1f-103">Мониторинг данных производительности</span><span class="sxs-lookup"><span data-stu-id="7ca1f-103">Monitoring Performance Data</span></span>

<span data-ttu-id="7ca1f-104">С помощью инструментария WMI можно программно получать доступ к данным системных счетчиков из объектов в библиотеках производительности.</span><span class="sxs-lookup"><span data-stu-id="7ca1f-104">Using WMI, you can access system counter data programmatically from objects in the performance libraries.</span></span> <span data-ttu-id="7ca1f-105">Это те же данные производительности, которые отображаются в системном мониторе в программе Perfmon.</span><span class="sxs-lookup"><span data-stu-id="7ca1f-105">This is the same performance data that appears in the System Monitor in the Perfmon utility.</span></span> <span data-ttu-id="7ca1f-106">Используйте предустановленные [Классы счетчиков производительности](/windows/desktop/CIMWin32Prov/performance-counter-classes) для получения данных о производительности в скриптах или приложениях C++.</span><span class="sxs-lookup"><span data-stu-id="7ca1f-106">Use the preinstalled [performance counter classes](/windows/desktop/CIMWin32Prov/performance-counter-classes) to obtain performance data in scripts or C++ applications.</span></span>

<span data-ttu-id="7ca1f-107">В этом разделе обсуждаются следующие разделы:</span><span class="sxs-lookup"><span data-stu-id="7ca1f-107">The following sections are discussed in this topic:</span></span>

-   [<span data-ttu-id="7ca1f-108">Классы производительности WMI</span><span class="sxs-lookup"><span data-stu-id="7ca1f-108">WMI Performance Classes</span></span>](#wmi-performance-classes)
-   [<span data-ttu-id="7ca1f-109">Поставщики данных производительности</span><span class="sxs-lookup"><span data-stu-id="7ca1f-109">Performance Data Providers</span></span>](#performance-data-providers)
-   [<span data-ttu-id="7ca1f-110">Использование форматированных классов данных о производительности</span><span class="sxs-lookup"><span data-stu-id="7ca1f-110">Using Formatted Performance Data Classes</span></span>](#using-formatted-performance-data-classes)
-   [<span data-ttu-id="7ca1f-111">Использование необработанных классов данных о производительности</span><span class="sxs-lookup"><span data-stu-id="7ca1f-111">Using Raw Performance Data Classes</span></span>](#using-raw-performance-data-classes)
-   [<span data-ttu-id="7ca1f-112">См. также</span><span class="sxs-lookup"><span data-stu-id="7ca1f-112">Related topics</span></span>](#related-topics)

## <a name="wmi-performance-classes"></a><span data-ttu-id="7ca1f-113">Классы производительности WMI</span><span class="sxs-lookup"><span data-stu-id="7ca1f-113">WMI Performance Classes</span></span>

<span data-ttu-id="7ca1f-114">Например, объект "NetworkInterface" в системном мониторе представлен в инструментарии WMI классом [**Win32 \_ перфравдата \_ tcpip \_ NetworkInterface**](./retrieving-raw-and-formatted-performance-data.md) для необработанных данных и класс [**Win32 \_ перфформаттеддата \_ tcpip \_ NetworkInterface**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) для предварительно вычисленных или форматированных данных.</span><span class="sxs-lookup"><span data-stu-id="7ca1f-114">As an example, the "NetworkInterface" object, in System Monitor, is represented in WMI by the [**Win32\_PerfRawData\_Tcpip\_NetworkInterface**](./retrieving-raw-and-formatted-performance-data.md) class for raw data and the [**Win32\_PerfFormattedData\_Tcpip\_NetworkInterface**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) class for precalculated, or formatted data.</span></span> <span data-ttu-id="7ca1f-115">Классы, производные от [**Win32 \_ перфравдата**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) и из [**Win32 \_ перфформаттеддата**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) , должны использоваться с объектом [*обновления*](gloss-r.md) .</span><span class="sxs-lookup"><span data-stu-id="7ca1f-115">Classes derived from [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) and from [**Win32\_PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) must be used with a [*refresher*](gloss-r.md) object.</span></span> <span data-ttu-id="7ca1f-116">В классах необработанных данных приложение C++ или сценарий должны выполнять вычисления, чтобы получить те же выходные данные, что и Perfmon.exe.</span><span class="sxs-lookup"><span data-stu-id="7ca1f-116">On raw data classes, your C++ application or script must perform calculations to obtain the same output as Perfmon.exe.</span></span> <span data-ttu-id="7ca1f-117">В форматированных классах данных предоставлены предварительно вычисленные данные.</span><span class="sxs-lookup"><span data-stu-id="7ca1f-117">Formatted data classes supply precalculated data.</span></span> <span data-ttu-id="7ca1f-118">Дополнительные сведения о получении данных в приложениях C++ см. [в разделе доступ к данным производительности в c++](accessing-performance-data-in-c--.md).</span><span class="sxs-lookup"><span data-stu-id="7ca1f-118">For more information about obtaining data in C++ applications, see [Accessing Performance Data in C++](accessing-performance-data-in-c--.md).</span></span> <span data-ttu-id="7ca1f-119">Сведения о сценариях см. в разделе [доступ к данным о производительности в скрипте](accessing-performance-data-in-script.md) и [Обновление данных WMI в скриптах](refreshing-wmi-data-in-scripts.md).</span><span class="sxs-lookup"><span data-stu-id="7ca1f-119">For scripting, see [Accessing Performance Data in Script](accessing-performance-data-in-script.md) and [Refreshing WMI Data in Scripts](refreshing-wmi-data-in-scripts.md).</span></span>

<span data-ttu-id="7ca1f-120">В следующем примере кода VBScript используется [**\_ \_ \_ процесс Win32 перфформаттеддата PerfProc**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) для получения данных о производительности процесса простоя.</span><span class="sxs-lookup"><span data-stu-id="7ca1f-120">The following VBScript code example uses [**Win32\_PerfFormattedData\_PerfProc\_Process**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) to obtain performance data for the Idle process.</span></span> <span data-ttu-id="7ca1f-121">Скрипт отображает те же данные, которые отображаются в PerfMon для счетчика "% загруженности процессора" объекта "процесс".</span><span class="sxs-lookup"><span data-stu-id="7ca1f-121">The script displays the same data that appears in Perfmon for the % Processor Time counter of the Process object.</span></span> <span data-ttu-id="7ca1f-122">Вызов [**свбемобжектекс. Refresh \_**](swbemobjectex-refresh-.md) выполняет операцию обновления.</span><span class="sxs-lookup"><span data-stu-id="7ca1f-122">The call to [**SWbemObjectEx.Refresh\_**](swbemobjectex-refresh-.md) performs the refresh operation.</span></span> <span data-ttu-id="7ca1f-123">Имейте в виду, что для получения базовых показателей данные должны обновляться в случае аренды.</span><span class="sxs-lookup"><span data-stu-id="7ca1f-123">Be aware that the data must be refreshed, at lease once, to obtain a baseline.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
    & "{impersonationLevel=impersonate}!\\" _
    & strComputer & "\root\cimv2")
set PerfProcess = objWMIService.Get(_
    "Win32_PerfFormattedData_PerfProc_Process.Name='Idle'")

While (True)
    PerfProcess.Refresh_     
    Wscript.Echo PerfProcess.PercentProcessorTime
    Wscript.Sleep 1000
Wend
```



<span data-ttu-id="7ca1f-124">Классы счетчиков производительности также могут предоставлять статистические данные.</span><span class="sxs-lookup"><span data-stu-id="7ca1f-124">Performance counter classes can also provide statistical data.</span></span> <span data-ttu-id="7ca1f-125">Дополнительные сведения см. в разделе [получение статистических данных о производительности](obtaining-statistical-performance-data.md).</span><span class="sxs-lookup"><span data-stu-id="7ca1f-125">For more information, see [Obtaining Statistical Performance Data](obtaining-statistical-performance-data.md).</span></span>

## <a name="performance-data-providers"></a><span data-ttu-id="7ca1f-126">Поставщики данных производительности</span><span class="sxs-lookup"><span data-stu-id="7ca1f-126">Performance Data Providers</span></span>

<span data-ttu-id="7ca1f-127">Инструментарий WMI имеет предварительно установленные поставщики, которые отслеживают производительность системы как в локальной системе, так и удаленно.</span><span class="sxs-lookup"><span data-stu-id="7ca1f-127">WMI has preinstalled providers that monitor system performance on both the local system and remotely.</span></span> <span data-ttu-id="7ca1f-128">Поставщик [вмиперфкласс](wmiperfclass-provider.md) создает классы, производные от [**Win32 \_ перфравдата**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) и из [**Win32 \_ перфформаттеддата**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata).</span><span class="sxs-lookup"><span data-stu-id="7ca1f-128">The [WmiPerfClass](wmiperfclass-provider.md) provider creates the classes derived from [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) and from [**Win32\_PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata).</span></span> <span data-ttu-id="7ca1f-129">Поставщик [вмиперфинст](wmiperfinst-provider.md) динамически предоставляет данные для необработанных и неформатированных классов.</span><span class="sxs-lookup"><span data-stu-id="7ca1f-129">The [WmiPerfInst](wmiperfinst-provider.md) provider supplies data dynamically to both raw and formatted classes.</span></span>

## <a name="using-formatted-performance-data-classes"></a><span data-ttu-id="7ca1f-130">Использование форматированных классов данных о производительности</span><span class="sxs-lookup"><span data-stu-id="7ca1f-130">Using Formatted Performance Data Classes</span></span>

<span data-ttu-id="7ca1f-131">Следующий пример кода VBScript получает данные производительности о памяти, разделах диска и рабочих очередях сервера.</span><span class="sxs-lookup"><span data-stu-id="7ca1f-131">The following VBScript code example obtains performance data about memory, disk partitions, and server work queues.</span></span> <span data-ttu-id="7ca1f-132">Затем Скрипт определяет, находятся ли значения в допустимом диапазоне.</span><span class="sxs-lookup"><span data-stu-id="7ca1f-132">The script then determines if the values are within an acceptable range.</span></span>

<span data-ttu-id="7ca1f-133">Скрипт использует следующие объекты поставщика WMI и объекты сценариев:</span><span class="sxs-lookup"><span data-stu-id="7ca1f-133">The script uses the following WMI provider objects and scripting objects:</span></span>

-   <span data-ttu-id="7ca1f-134">Предустановленные классы счетчиков производительности WMI.</span><span class="sxs-lookup"><span data-stu-id="7ca1f-134">Preinstalled WMI performance counter classes.</span></span>
-   <span data-ttu-id="7ca1f-135">Объект Обновитель, [**свбемрефрешер**](swbemrefresher.md).</span><span class="sxs-lookup"><span data-stu-id="7ca1f-135">The refresher object, [**SWbemRefresher**](swbemrefresher.md).</span></span>
-   <span data-ttu-id="7ca1f-136">Элементы, добавляемые в контейнер Обновитель, [ **свбемрефрешаблеитем**](swbemrefreshableitem.md)</span><span class="sxs-lookup"><span data-stu-id="7ca1f-136">Items to add to the refresher container, [**SWbemRefreshableItem**](swbemrefreshableitem.md)</span></span>


```VB
Set objCimv2 = GetObject("winmgmts:root\cimv2")
Set objRefresher = CreateObject("WbemScripting.SWbemRefresher")

' Add items to the SWbemRefresher
' Without the SWbemRefreshableItem.ObjectSet call,
' the script will fail
Set objMemory = objRefresher.AddEnum _
    (objCimv2, _ 
    "Win32_PerfFormattedData_PerfOS_Memory").ObjectSet
Set objDiskQueue = objRefresher.AddEnum _
    (objCimv2, _
    "Win32_PerfFormattedData_PerfDisk_LogicalDisk").ObjectSet
Set objQueueLength = objRefresher.AddEnum _
    (objCimv2, _
    "Win32_PerfFormattedData_PerfNet_ServerWorkQueues").ObjectSet

' Initial refresh needed to get baseline values
objRefresher.Refresh
intTotalHealth = 0
' Do three refreshes to get data
For i = 1 to 3
    WScript.Echo "Refresh " & i
    For each intAvailableBytes in objMemory
        WScript.Echo "Available megabytes of memory: " _
            & intAvailableBytes.AvailableMBytes
        If intAvailableBytes.AvailableMBytes < 4 Then
            intTotalHealth = intTotalHealth + 1
        End If
    Next
    For each intDiskQueue in objDiskQueue
        WScript.Echo "Current disk queue length " & "Name: " _
            & intDiskQueue.Name & ":" _
            & intDiskQueue.CurrentDiskQueueLength
        If intDiskQueue.CurrentDiskQueueLength > 2 Then
            intTotalHealth = intTotalHealth + 1
        End If
    Next
    For each intServerQueueLength in objQueueLength
        WScript.Echo "Server work queue length: " _
            & intServerQueueLength.QueueLength
        If intServerQueueLength.QueueLength > 4 Then
            intTotalHealth = intTotalHealth + 1                       
        End If
    Wscript.Echo "  "
    Next
    If intTotalHealth > 0 Then
        Wscript.Echo "Unhealthy."
    Else
        Wscript.Echo "Healthy."
    End If
    intTotalHealth = 0
    Wscript.Sleep 5000
' Refresh data for all objects in the collection
    objRefresher.Refresh
Next
```



## <a name="using-raw-performance-data-classes"></a><span data-ttu-id="7ca1f-137">Использование необработанных классов данных о производительности</span><span class="sxs-lookup"><span data-stu-id="7ca1f-137">Using Raw Performance Data Classes</span></span>

<span data-ttu-id="7ca1f-138">Следующий пример кода VBScript получает необработанный процент времени процессора на локальном компьютере и преобразует его в проценты.</span><span class="sxs-lookup"><span data-stu-id="7ca1f-138">The following VBScript code example obtains raw, current percent processor time on the local computer and converts it to a percentage.</span></span> <span data-ttu-id="7ca1f-139">В примере показано, как получить необработанные данные о производительности из свойства **перцентпроцессортиме** класса [**\_ процессора Win32 \_ перфравдата \_ перфос**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) .</span><span class="sxs-lookup"><span data-stu-id="7ca1f-139">The example shows you how to obtain raw performance data from the **PercentProcessorTime** property of the [**Win32\_PerfRawData\_PerfOS\_Processor**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) class.</span></span>

<span data-ttu-id="7ca1f-140">Чтобы вычислить значение процентного времени процессора, необходимо указать формулу.</span><span class="sxs-lookup"><span data-stu-id="7ca1f-140">To calculate the percent processor time value, you must locate the formula.</span></span> <span data-ttu-id="7ca1f-141">Найдите значение в квалификаторе **CounterType** для свойства **Перцентпроцессортиме** в таблице [**квалификатора CounterType**](countertype-qualifier.md) , чтобы получить имя константы.</span><span class="sxs-lookup"><span data-stu-id="7ca1f-141">Look up the value in the **CounterType** qualifier for the **PercentProcessorTime** property in the [**CounterType Qualifier**](countertype-qualifier.md) table to get the constant name.</span></span> <span data-ttu-id="7ca1f-142">Чтобы получить формулу, найдите имя константы в [типах счетчиков](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10)) .</span><span class="sxs-lookup"><span data-stu-id="7ca1f-142">Locate the constant name in [Counter Types](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10)) to obtain the formula.</span></span>


```VB
Set objService = GetObject( _
    "Winmgmts:{impersonationlevel=impersonate}!\Root\Cimv2")

For i = 1 to 8
    Set objInstance1 = objService.Get( _
        "Win32_PerfRawData_PerfOS_Processor.Name='_Total'")
    N1 = objInstance1.PercentProcessorTime
    D1 = objInstance1.TimeStamp_Sys100NS

'Sleep for two seconds = 2000 ms
    WScript.Sleep(2000)

    Set perf_instance2 = objService.Get( _
        "Win32_PerfRawData_PerfOS_Processor.Name='_Total'")
    N2 = perf_instance2.PercentProcessorTime
    D2 = perf_instance2.TimeStamp_Sys100NS
' Look up the CounterType qualifier for the PercentProcessorTime 
' and obtain the formula to calculate the meaningful data. 
' CounterType - PERF_100NSEC_TIMER_INV
' Formula - (1- ((N2 - N1) / (D2 - D1))) x 100

    PercentProcessorTime = (1 - ((N2 - N1)/(D2-D1)))*100
    WScript.Echo "% Processor Time=" , Round(PercentProcessorTime,2)
Next
```



## <a name="related-topics"></a><span data-ttu-id="7ca1f-143">См. также</span><span class="sxs-lookup"><span data-stu-id="7ca1f-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7ca1f-144">Использование инструментария WMI</span><span class="sxs-lookup"><span data-stu-id="7ca1f-144">Using WMI</span></span>](using-wmi.md)
</dt> </dl>

 

 
