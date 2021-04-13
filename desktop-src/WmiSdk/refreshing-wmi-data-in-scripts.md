---
description: В скриптах мониторинга можно избежать последовательных вызовов GetObject с помощью объекта Свбемрефрешер. Объект Свбемрефрешер — это контейнер, который может содержать несколько объектов WMI, данные которых могут быть обновлены в одном вызове.
ms.assetid: b34567f5-9349-4580-97d5-723759805d88
ms.tgt_platform: multiple
title: Обновление данных WMI в скриптах
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae0f17ce718fcf5b57e4f3204337634af4129d24
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265373"
---
# <a name="refreshing-wmi-data-in-scripts"></a><span data-ttu-id="61f14-104">Обновление данных WMI в скриптах</span><span class="sxs-lookup"><span data-stu-id="61f14-104">Refreshing WMI Data in Scripts</span></span>

<span data-ttu-id="61f14-105">В скриптах мониторинга можно избежать последовательных **вызовов GetObject с** помощью объекта [**свбемрефрешер**](swbemrefresher.md) .</span><span class="sxs-lookup"><span data-stu-id="61f14-105">In monitoring scripts, you can avoid successive calls to **GetObject** by using an [**SWbemRefresher**](swbemrefresher.md) object.</span></span> <span data-ttu-id="61f14-106">Объект **свбемрефрешер** — это контейнер, который может содержать несколько объектов WMI, данные которых могут быть обновлены в одном вызове.</span><span class="sxs-lookup"><span data-stu-id="61f14-106">The **SWbemRefresher** object is a container that can hold several WMI objects whose data can be refreshed in one call.</span></span>

<span data-ttu-id="61f14-107">Использование объекта [**свбемрефрешер**](swbemrefresher.md) требуется для получения точных данных из классов производительности WMI, таких как [**Win32 \_ перфформаттеддата \_ перфдиск \_ LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md) или другие предустановленные классы, производные от [**\_ производительности Win32**](/windows/desktop/CIMWin32Prov/win32-perf).</span><span class="sxs-lookup"><span data-stu-id="61f14-107">Using an [**SWbemRefresher**](swbemrefresher.md) object is required to get accurate data from WMI performance classes, such as [**Win32\_PerfFormattedData\_PerfDisk\_LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md) or other preinstalled classes derived from [**Win32\_Perf**](/windows/desktop/CIMWin32Prov/win32-perf).</span></span>

<span data-ttu-id="61f14-108">В следующей процедуре описывается обновление данных в скриптах.</span><span class="sxs-lookup"><span data-stu-id="61f14-108">The following procedure describes how to refresh data in scripts.</span></span>

<span data-ttu-id="61f14-109">**Обновление данных в скриптах**</span><span class="sxs-lookup"><span data-stu-id="61f14-109">**To refresh data in scripts**</span></span>

1.  <span data-ttu-id="61f14-110">Вызовите функцию **CreateObject** , чтобы создать объект обновления [**свбемрефрешер**](swbemrefresher.md) .</span><span class="sxs-lookup"><span data-stu-id="61f14-110">Call **CreateObject** to create an [**SWbemRefresher**](swbemrefresher.md) refresher object.</span></span>

    ```VB
    Set objRefresher = CreateObject("WbemScripting.SWbemRefresher")
    ```

    

2.  <span data-ttu-id="61f14-111">Подключитесь к пространству имен WMI.</span><span class="sxs-lookup"><span data-stu-id="61f14-111">Connect to the WMI namespace.</span></span> <span data-ttu-id="61f14-112">Чтобы использовать предварительно установленные классы производительность [**\_ производительности Win32**](/windows/desktop/CIMWin32Prov/win32-perf) , подключитесь к **корневому каталогу \\ CIMV2**.</span><span class="sxs-lookup"><span data-stu-id="61f14-112">To use preinstalled [**Win32\_Perf**](/windows/desktop/CIMWin32Prov/win32-perf) performances classes, connect to **root\\cimv2**.</span></span>

    ```VB
    Set objServicesCimv2 = GetObject("winmgmts:\\" _
        & strComputer & "\root\cimv2")
    ```

    

3.  <span data-ttu-id="61f14-113">Добавьте один объект (вызов [**свбемрефрешер. Add**](swbemrefresher-add.md)) или коллекцию (вызов [**свбемрефрешер. адденум**](swbemrefresher-addenum.md)) в обновитель.</span><span class="sxs-lookup"><span data-stu-id="61f14-113">Add a single object (call [**SWbemRefresher.Add**](swbemrefresher-add.md)) or a collection (call [**SWbemRefresher.AddEnum**](swbemrefresher-addenum.md)) to the refresher.</span></span>

    <span data-ttu-id="61f14-114">Используйте предварительно вычисленные классы данных, производные от [**Win32 \_ перфформаттеддата**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata), например [**Win32 \_ перфформаттеддата \_ перфдиск \_ LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md) , а не [**Win32 \_ перфравдата \_ перфдиск \_ LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md).</span><span class="sxs-lookup"><span data-stu-id="61f14-114">Use the precalculated data classes derived from [**Win32\_PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata), for example, [**Win32\_PerfFormattedData\_PerfDisk\_LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md) instead of [**Win32\_PerfRawData\_PerfDisk\_LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md).</span></span> <span data-ttu-id="61f14-115">В противном случае необходимо вычислить значения для всех свойств, Кроме простых счетчиков.</span><span class="sxs-lookup"><span data-stu-id="61f14-115">Otherwise, you must calculate the values for all of the properties other than simple counters.</span></span>

    ```VB
    Set objRefreshableItem = _
        objRefresher.AddEnum(objServicesCimv2 , _
        "Win32_PerfFormattedData_PerfProc_Process")
    ```

    

4.  <span data-ttu-id="61f14-116">Обновите данные один раз, чтобы получить исходные данные о производительности.</span><span class="sxs-lookup"><span data-stu-id="61f14-116">Refresh the data one time to get the initial performance data.</span></span>

    <span data-ttu-id="61f14-117">Вызовите метод [**свбемрефрешер. Refresh**](swbemrefresher-refresh.md) или универсальный метод [**свбемобжектекс. Refresh \_**](swbemobjectex-refresh-.md) .</span><span class="sxs-lookup"><span data-stu-id="61f14-117">Call either the [**SWbemRefresher.Refresh**](swbemrefresher-refresh.md) method or the generic [**SWbemObjectEx.Refresh\_**](swbemobjectex-refresh-.md) method.</span></span>

    ```VB
    objRefresher.Refresh
    ```

    

5.  <span data-ttu-id="61f14-118">При мониторинге производительности и наличии коллекции в объекте обновления пройдите через объекты коллекции.</span><span class="sxs-lookup"><span data-stu-id="61f14-118">If you are monitoring performance and have a collection in the refresher object, loop through the collection objects.</span></span>

    ```VB
    For Each Process in objRefreshableItem.ObjectSet
        If Process.PercentProcessorTime > 1 then
            WScript.Echo Process.Name & vbnewLine _
                & Process.PercentProcessorTime & "%"
        End If
    Next
    ```

    

6.  <span data-ttu-id="61f14-119">Очистите элементы из обновления, вызвав [**свбемрефрешер. DeleteAll**](swbemrefresher-deleteall.md) или удалив определенные элементы, вызвав [**Свбемрефрешер. Refresh**](swbemrefresher-remove.md).</span><span class="sxs-lookup"><span data-stu-id="61f14-119">Clear the items from the refresher by calling [**SWbemRefresher.DeleteAll**](swbemrefresher-deleteall.md) or remove specific items by calling [**SwbemRefresher.Remove**](swbemrefresher-remove.md).</span></span>

<span data-ttu-id="61f14-120">В следующем примере кода VBScript показано, как обновить один объект на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="61f14-120">The following VBScript code example shows how to refresh a single object on the local computer.</span></span> <span data-ttu-id="61f14-121">Скрипт создает контейнер обновления и добавляет экземпляр перечислителя для экземпляров [**\_ \_ \_ процесса PerfProc Win32 перфформаттеддата**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) .</span><span class="sxs-lookup"><span data-stu-id="61f14-121">The script creates a refresher container and adds an instance of an enumerator for [**Win32\_PerfFormattedData\_PerfProc\_Process**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) instances.</span></span> <span data-ttu-id="61f14-122">Вызов [**обновления**](swbemrefresher-refresh.md) выполняется три раза, чтобы продемонстрировать изменения в свойстве **перцентпроцессортиме** для процессов, использующих более одного процента времени процессора.</span><span class="sxs-lookup"><span data-stu-id="61f14-122">The [**Refresh**](swbemrefresher-refresh.md) call is made three times to demonstrate the changes in the **PercentProcessorTime** property for processes using more than one percent of the processor time.</span></span>


```VB
On Error Resume Next
strComputer = "."
Set objRefresher = CreateObject("WbemScripting.SWbemRefresher")
Set objServicesCimv2 = GetObject("winmgmts:\\" & strComputer & "\root\cimv2")
If Err = 0 Then 
Set objRefreshableItem = _
    objRefresher.AddEnum(objServicesCimv2 ,"Win32_PerfFormattedData_PerfProc_Process")
objRefresher.Refresh
' Loop through the processes three times to locate  
'    and display all the process currently using 
'    more than 1 % of the process time. Refresh on each pass.
For i = 1 to 3
    Wscript.Echo "Refresh number " & i 
    objRefresher.Refresh 
    For Each Process in objRefreshableItem.ObjectSet
        If Process.PercentProcessorTime > 1 then
            WScript.Echo Process.Name & vbnewLine & Process.PercentProcessorTime & "%"
        End If
    Next
Next
Else
    WScript.Echo Err.Description
End If
```



<span data-ttu-id="61f14-123">Свойство [**index**](swbemrefreshableitem-index.md) возвращаемого [**свбемрефрешаблеитем**](swbemrefreshableitem.md) представляет индекс объекта в коллекции обновитель.</span><span class="sxs-lookup"><span data-stu-id="61f14-123">The [**Index**](swbemrefreshableitem-index.md) property of the returned [**SWbemRefreshableItem**](swbemrefreshableitem.md) represents the index of the object in the refresher collection.</span></span> <span data-ttu-id="61f14-124">Можно вызвать свойство [**свбемрефрешаблеитем. Иссет**](swbemrefreshableitem-isset.md) , чтобы определить, является ли элемент в обновитель единственным элементом или коллекцией.</span><span class="sxs-lookup"><span data-stu-id="61f14-124">You can call [**SWbemRefreshableItem.IsSet**](swbemrefreshableitem-isset.md) property to determine whether or not an item in a refresher is a single item or a collection.</span></span> <span data-ttu-id="61f14-125">Для доступа к одному элементу используйте свойство [**свбемрефрешаблеитем. Object**](swbemrefreshableitem-object.md) .</span><span class="sxs-lookup"><span data-stu-id="61f14-125">To access a single item, use the [**SWbemRefreshableItem.Object**](swbemrefreshableitem-object.md) property.</span></span> <span data-ttu-id="61f14-126">Если не выполнить вызов **свбемрефрешаблеитем. Object**, скрипт завершится ошибкой при попытке получить доступ к объекту.</span><span class="sxs-lookup"><span data-stu-id="61f14-126">If you do not make the call to **SWbemRefreshableItem.Object**, then the script fails when you try to access the object.</span></span> <span data-ttu-id="61f14-127">Чтобы получить доступ к коллекции, используйте свойство [**свбемрефрешаблеитем. objecting**](swbemrefreshableitem-objectset.md) .</span><span class="sxs-lookup"><span data-stu-id="61f14-127">To access a collection, use the [**SWbemRefreshableItem.ObjectSet**](swbemrefreshableitem-objectset.md) property.</span></span>

## <a name="related-topics"></a><span data-ttu-id="61f14-128">См. также</span><span class="sxs-lookup"><span data-stu-id="61f14-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="61f14-129">Классы счетчиков производительности</span><span class="sxs-lookup"><span data-stu-id="61f14-129">Performance Counter Classes</span></span>](/windows/desktop/CIMWin32Prov/performance-counter-classes)
</dt> <dt>

[<span data-ttu-id="61f14-130">Доступ к данным о производительности в скрипте</span><span class="sxs-lookup"><span data-stu-id="61f14-130">Accessing Performance Data in Script</span></span>](accessing-performance-data-in-script.md)
</dt> <dt>

[<span data-ttu-id="61f14-131">Задачи WMI: Мониторинг производительности</span><span class="sxs-lookup"><span data-stu-id="61f14-131">WMI Tasks: Performance Monitoring</span></span>](wmi-tasks--performance-monitoring.md)
</dt> <dt>

[<span data-ttu-id="61f14-132">Мониторинг данных производительности</span><span class="sxs-lookup"><span data-stu-id="61f14-132">Monitoring Performance Data</span></span>](monitoring-performance-data.md)
</dt> </dl>

 

 
