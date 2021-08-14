---
description: С помощью инструментария WMI можно программно получать доступ к данным системных счетчиков из объектов в библиотеках производительности.
ms.assetid: a0ed14e9-d2ec-43eb-8c8e-eac3c134ea1d
ms.tgt_platform: multiple
title: Мониторинг данных производительности
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba4f3ddd5024fb27d83f08225fa65faaa2e7d02cdd28189c86fc979175861453
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118317108"
---
# <a name="monitoring-performance-data"></a>Мониторинг данных производительности

С помощью инструментария WMI можно программно получать доступ к данным системных счетчиков из объектов в библиотеках производительности. Это те же данные производительности, которые отображаются в системном мониторе в программе Perfmon. Используйте предустановленные [Классы счетчиков производительности](/windows/desktop/CIMWin32Prov/performance-counter-classes) для получения данных о производительности в скриптах или приложениях C++.

В этом разделе обсуждаются следующие разделы:

-   [Классы производительности WMI](#wmi-performance-classes)
-   [Поставщики данных производительности](#performance-data-providers)
-   [Использование форматированных классов данных о производительности](#using-formatted-performance-data-classes)
-   [Использование необработанных классов данных о производительности](#using-raw-performance-data-classes)
-   [Связанные темы](#related-topics)

## <a name="wmi-performance-classes"></a>Классы производительности WMI

Например, объект "NetworkInterface" в системном мониторе представлен в инструментарии WMI классом [**Win32 \_ перфравдата \_ tcpip \_ NetworkInterface**](./retrieving-raw-and-formatted-performance-data.md) для необработанных данных и класс [**Win32 \_ перфформаттеддата \_ tcpip \_ NetworkInterface**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) для предварительно вычисленных или форматированных данных. Классы, производные от [**Win32 \_ перфравдата**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) и из [**Win32 \_ перфформаттеддата**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) , должны использоваться с объектом [*обновления*](gloss-r.md) . В классах необработанных данных приложение C++ или сценарий должны выполнять вычисления, чтобы получить те же выходные данные, что и Perfmon.exe. В форматированных классах данных предоставлены предварительно вычисленные данные. Дополнительные сведения о получении данных в приложениях C++ см. [в разделе доступ к данным производительности в c++](accessing-performance-data-in-c--.md). Сведения о сценариях см. в разделе [доступ к данным о производительности в скрипте](accessing-performance-data-in-script.md) и [Обновление данных WMI в скриптах](refreshing-wmi-data-in-scripts.md).

В следующем примере кода VBScript используется [**\_ \_ \_ процесс Win32 перфформаттеддата PerfProc**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) для получения данных о производительности процесса простоя. Скрипт отображает те же данные, которые отображаются в PerfMon для счетчика "% загруженности процессора" объекта "процесс". Вызов [**свбемобжектекс. Refresh \_**](swbemobjectex-refresh-.md) выполняет операцию обновления. Имейте в виду, что для получения базовых показателей данные должны обновляться в случае аренды.


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



Классы счетчиков производительности также могут предоставлять статистические данные. Дополнительные сведения см. в разделе [получение статистических данных о производительности](obtaining-statistical-performance-data.md).

## <a name="performance-data-providers"></a>Поставщики данных производительности

Инструментарий WMI имеет предварительно установленные поставщики, которые отслеживают производительность системы как в локальной системе, так и удаленно. Поставщик [вмиперфкласс](wmiperfclass-provider.md) создает классы, производные от [**Win32 \_ перфравдата**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) и из [**Win32 \_ перфформаттеддата**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata). Поставщик [вмиперфинст](wmiperfinst-provider.md) динамически предоставляет данные для необработанных и неформатированных классов.

## <a name="using-formatted-performance-data-classes"></a>Использование форматированных классов данных о производительности

Следующий пример кода VBScript получает данные производительности о памяти, разделах диска и рабочих очередях сервера. Затем Скрипт определяет, находятся ли значения в допустимом диапазоне.

Скрипт использует следующие объекты поставщика WMI и объекты сценариев:

-   Предустановленные классы счетчиков производительности WMI.
-   Объект Обновитель, [**свбемрефрешер**](swbemrefresher.md).
-   Элементы, добавляемые в контейнер Обновитель, [ **свбемрефрешаблеитем**](swbemrefreshableitem.md)


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



## <a name="using-raw-performance-data-classes"></a>Использование необработанных классов данных о производительности

Следующий пример кода VBScript получает необработанный процент времени процессора на локальном компьютере и преобразует его в проценты. В примере показано, как получить необработанные данные о производительности из свойства **перцентпроцессортиме** класса [**\_ процессора Win32 \_ перфравдата \_ перфос**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) .

Чтобы вычислить значение процентного времени процессора, необходимо указать формулу. Найдите значение в квалификаторе **CounterType** для свойства **Перцентпроцессортиме** в таблице [**квалификатора CounterType**](countertype-qualifier.md) , чтобы получить имя константы. Чтобы получить формулу, найдите имя константы в [типах счетчиков](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10)) .


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



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Использование инструментария WMI](using-wmi.md)
</dt> </dl>

 

 
