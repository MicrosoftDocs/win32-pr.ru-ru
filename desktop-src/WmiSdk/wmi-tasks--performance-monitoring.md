---
description: Используйте классы WMI, которые получают данные из счетчиков производительности для доступа и обновления данных о производительности компьютера.
ms.assetid: 4c88de96-992e-4d34-ba93-35d2b6e73c1d
ms.tgt_platform: multiple
title: 'Задачи WMI: Мониторинг производительности'
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: bbb254e14280bec5a928bdc32aaa9a3e03c7a4f4
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/16/2021
ms.locfileid: "105656825"
---
# <a name="wmi-tasks-performance-monitoring"></a><span data-ttu-id="e947e-103">Задачи WMI: Мониторинг производительности</span><span class="sxs-lookup"><span data-stu-id="e947e-103">WMI Tasks: Performance Monitoring</span></span>

<span data-ttu-id="e947e-104">Используйте классы WMI, которые получают данные из счетчиков производительности для доступа и обновления данных о производительности компьютера.</span><span class="sxs-lookup"><span data-stu-id="e947e-104">Use the WMI classes that obtain data from performance counters to access and refresh data about computer performance.</span></span> <span data-ttu-id="e947e-105">Другие примеры см. в разделе TechNet Скриптцентер по адресу [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx) .</span><span class="sxs-lookup"><span data-stu-id="e947e-105">For other examples, see the TechNet ScriptCenter at [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx).</span></span> <span data-ttu-id="e947e-106">Дополнительные сведения см. в разделе [библиотеки производительности и инструментарий WMI](performance-libraries-and-wmi.md) и [наблюдение за данными производительности](monitoring-performance-data.md).</span><span class="sxs-lookup"><span data-stu-id="e947e-106">For more information, see [Performance Libraries and WMI](performance-libraries-and-wmi.md) and [Monitoring Performance Data](monitoring-performance-data.md).</span></span>

<span data-ttu-id="e947e-107">Примеры сценариев, приведенные в этом разделе, получают данные только с локального компьютера.</span><span class="sxs-lookup"><span data-stu-id="e947e-107">The script examples shown in this topic obtain data only from the local computer.</span></span> <span data-ttu-id="e947e-108">Дополнительные сведения об использовании сценария для получения данных с удаленных компьютеров см. в разделе [Подключение к WMI на удаленном компьютере](connecting-to-wmi-on-a-remote-computer.md).</span><span class="sxs-lookup"><span data-stu-id="e947e-108">For more information about how to use the script to obtain data from remote computers, see [Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span></span>


<span data-ttu-id="e947e-109">В следующей процедуре описывается выполнение скрипта.</span><span class="sxs-lookup"><span data-stu-id="e947e-109">The following procedure describes how to run a script.</span></span>

<span data-ttu-id="e947e-110">**Запуск сценария**</span><span class="sxs-lookup"><span data-stu-id="e947e-110">**To run a script**</span></span>

1.  <span data-ttu-id="e947e-111">Скопируйте код и сохраните его в файле с расширением vbs, например *filename.vbs*.</span><span class="sxs-lookup"><span data-stu-id="e947e-111">Copy the code and save it in a file with a .vbs extension, such as *filename.vbs*.</span></span> <span data-ttu-id="e947e-112">Убедитесь, что текстовый редактор не добавляет расширение txt в файл.</span><span class="sxs-lookup"><span data-stu-id="e947e-112">Ensure that your text editor does not add a .txt extension to the file.</span></span>
2.  <span data-ttu-id="e947e-113">Откройте окно командной строки и перейдите в каталог, в котором был сохранен файл.</span><span class="sxs-lookup"><span data-stu-id="e947e-113">Open a command prompt window and navigate to the directory where you saved the file.</span></span>
3.  <span data-ttu-id="e947e-114">Введите **cscript filename.vbs** в командной строке.</span><span class="sxs-lookup"><span data-stu-id="e947e-114">Type **cscript filename.vbs** at the command prompt.</span></span>
4.  <span data-ttu-id="e947e-115">Если доступ к журналу событий невозможен, проверьте, выполняется ли в командной строке с повышенными привилегиями.</span><span class="sxs-lookup"><span data-stu-id="e947e-115">If you cannot access an event log, check to see if you are running from an Elevated command prompt.</span></span> <span data-ttu-id="e947e-116">Некоторые журналы событий, например журнал событий безопасности, могут быть защищены с помощью элементов управления доступом пользователей (UAC).</span><span class="sxs-lookup"><span data-stu-id="e947e-116">Some Event Log, such as the Security Event Log, may be protected by User Access Controls (UAC).</span></span>

> [!Note]  
> <span data-ttu-id="e947e-117">По умолчанию Cscript отображает выходные данные скрипта в окне командной строки.</span><span class="sxs-lookup"><span data-stu-id="e947e-117">By default, cscript displays the output of a script in the command prompt window.</span></span> <span data-ttu-id="e947e-118">Поскольку сценарии WMI могут создавать большие объемы выходных данных, может потребоваться перенаправить выходные данные в файл.</span><span class="sxs-lookup"><span data-stu-id="e947e-118">Because WMI scripts can produce large amounts of output, you might want to redirect the output to a file.</span></span> <span data-ttu-id="e947e-119">Введите **cscript filename.vbs > outfile.txt** в командной строке, чтобы перенаправить выходные данные скрипта *filename.vbs* в *outfile.txt*.</span><span class="sxs-lookup"><span data-stu-id="e947e-119">Type **cscript filename.vbs > outfile.txt** at the command prompt to redirect the output of the *filename.vbs* script to *outfile.txt*.</span></span>

 

<span data-ttu-id="e947e-120">В следующей таблице перечислены примеры сценариев, которые можно использовать для получения различных типов данных с локального компьютера.</span><span class="sxs-lookup"><span data-stu-id="e947e-120">The following table lists script examples that can be used to obtain various types of data from the local computer.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e947e-121">Часто выполняемые действия в новом интерфейсе</span><span class="sxs-lookup"><span data-stu-id="e947e-121">How do I...</span></span></th>
<th><span data-ttu-id="e947e-122">Классы или методы WMI</span><span class="sxs-lookup"><span data-stu-id="e947e-122">WMI classes or methods</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e947e-123">... получить данные счетчиков производительности, которые можно увидеть в программе Perfmon в сценарии?</span><span class="sxs-lookup"><span data-stu-id="e947e-123">...obtain the performance counter data that I can see in the Perfmon utility in a script?</span></span></td>
<td><span data-ttu-id="e947e-124">Используйте классы, имена которых начинаются с &quot; <a href="/windows/desktop/CIMWin32Prov/performance-counter-classes">Win32_PerfFormattedData</a> &quot; , например <a href="/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data"><strong>Win32_PerfFormattedData_PerfProc_Process</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="e947e-124">Use classes that have names that begin with &quot;<a href="/windows/desktop/CIMWin32Prov/performance-counter-classes">Win32_PerfFormattedData</a>&quot;, for example <a href="/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data"><strong>Win32_PerfFormattedData_PerfProc_Process</strong></a>.</span></span> <span data-ttu-id="e947e-125">Свойства с именами, например <strong>пажефилебитес</strong> , соответствуют счетчикам производительности, отображаемым в PerfMon.</span><span class="sxs-lookup"><span data-stu-id="e947e-125">Properties with names like <strong>PageFileBytes</strong> correspond to performance counters you see in Perfmon.</span></span> <span data-ttu-id="e947e-126">&quot;Win32_PerfFormattedData &quot; классы вычисляют конечные значения счетчиков автоматически.</span><span class="sxs-lookup"><span data-stu-id="e947e-126">The &quot;Win32_PerfFormattedData&quot; classes calculate the final values of counters for you.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e947e-127">... Получайте актуальные данные о производительности для одного процесса, диска и других данных?</span><span class="sxs-lookup"><span data-stu-id="e947e-127">...get on-going performance data for a single process, disk drive, and other data?</span></span></td>
<td><span data-ttu-id="e947e-128">Используйте <a href="/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data"><strong>Win32_PerfFormattedData_PerfProc_Process</strong></a> или соответствующий <a href="/windows/desktop/CIMWin32Prov/performance-counter-classes">класс счетчика производительности</a> и метод <a href="swbemobjectex-refresh-.md"><strong>SWbemObjectEx.Refresh_</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="e947e-128">Use the <a href="/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data"><strong>Win32_PerfFormattedData_PerfProc_Process</strong></a> or the appropriate formatted <a href="/windows/desktop/CIMWin32Prov/performance-counter-classes">Performance Counter Class</a> and the <a href="swbemobjectex-refresh-.md"><strong>SWbemObjectEx.Refresh_</strong></a> method.</span></span> <span data-ttu-id="e947e-129">Дополнительные сведения см. в разделе <a href="scripting-with-swbemobject.md">Создание скриптов с помощью SWbemObject</a>.</span><span class="sxs-lookup"><span data-stu-id="e947e-129">For more information, see <a href="scripting-with-swbemobject.md">Scripting with SWbemObject</a>.</span></span><br/> <span data-ttu-id="e947e-130">В C++ используйте <a href="/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemconfigurerefresher-addobjectbypath"><strong>ивбемконфигуререфрешер:: аддобжектбипас</strong></a> и <a href="/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh"><strong>Ивбемрефрешер:: Refresh</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="e947e-130">In C++, use <a href="/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemconfigurerefresher-addobjectbypath"><strong>IWbemConfigureRefresher::AddObjectByPath</strong></a> and <a href="/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh"><strong>IWbemRefresher::Refresh</strong></a>.</span></span> <span data-ttu-id="e947e-131">Дополнительные сведения см. в разделе <a href="monitoring-performance-data.md">наблюдение за данными производительности</a>.</span><span class="sxs-lookup"><span data-stu-id="e947e-131">For more information, see <a href="monitoring-performance-data.md">Monitoring Performance Data</a>.</span></span><br/> <span data-ttu-id="e947e-132">Следующий сценарий выполняется до перезагрузки компьютера, Инструментарий WMI остановлен или сценарий остановлен.</span><span class="sxs-lookup"><span data-stu-id="e947e-132">The following script runs until the computer is restarted, WMI is stopped, or the script is stopped.</span></span> <span data-ttu-id="e947e-133">Чтобы прерывать выполнение скрипта вручную, используйте диспетчер задач, чтобы прерывать процесс.</span><span class="sxs-lookup"><span data-stu-id="e947e-133">To stop the script manually, use Task Manager to stop the process.</span></span> <span data-ttu-id="e947e-134">Чтобы остановить его программно, используйте метод <a href="/windows/desktop/CIMWin32Prov/terminate-method-in-class-win32-process"><strong>Terminate</strong></a> в классе <a href="/windows/desktop/CIMWin32Prov/win32-process"><strong>Win32_Process</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="e947e-134">To stop it programmatically, use the <a href="/windows/desktop/CIMWin32Prov/terminate-method-in-class-win32-process"><strong>Terminate</strong></a> method in the <a href="/windows/desktop/CIMWin32Prov/win32-process"><strong>Win32_Process</strong></a> class.</span></span><br/> <span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e947e-135">VB</span><span class="sxs-lookup"><span data-stu-id="e947e-135">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; _
    & &quot;{impersonationLevel=impersonate}!\\&quot; _
    & strComputer & &quot;\root\cimv2&quot;)
set PerfProcess = objWMIService.Get(_
    &quot;Win32_PerfFormattedData_PerfProc_Process.Name=&#39;Idle&#39;&quot;)

While (True)
    PerfProcess.Refresh_     
    Wscript.Echo PerfProcess.PercentProcessorTime
    Wscript.Sleep 1000
Wend</code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e947e-136">... получать актуальные данные о производительности для всех процессов без повторяющегося опроса?</span><span class="sxs-lookup"><span data-stu-id="e947e-136">...get on-going performance data for all processes without repeated polling?</span></span></td>
<td><p><span data-ttu-id="e947e-137">Используйте классы, имена которых начинаются с &quot; Win32_PerfFormattedData &quot; и объекта <a href="swbemrefresher.md"><strong>свбемрефрешер</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="e947e-137">Use classes that have names that begin with &quot;Win32_PerfFormattedData&quot; and an <a href="swbemrefresher.md"><strong>SWbemRefresher</strong></a> object.</span></span> <span data-ttu-id="e947e-138">Обновитель содержит объекты, поэтому вам не нужно многократно получать коллекцию.</span><span class="sxs-lookup"><span data-stu-id="e947e-138">The refresher holds the objects so you do not need to get the collection repeatedly.</span></span> <span data-ttu-id="e947e-139">Для вычисления данных о производительности требуется как минимум два значения, так как большинство счетчиков являются счетчиками скорости.</span><span class="sxs-lookup"><span data-stu-id="e947e-139">A minimum of two values are needed to calculate performance data because most counters are rate counters.</span></span> <span data-ttu-id="e947e-140">При первом отображении данные для обновления будут пустыми.</span><span class="sxs-lookup"><span data-stu-id="e947e-140">The first time you display the refresher data it is empty.</span></span></p>
<p><span data-ttu-id="e947e-141">Следующий скрипт выполняется неограниченно до перезагрузки компьютера, Инструментарий WMI остановлен или сценарий остановлен.</span><span class="sxs-lookup"><span data-stu-id="e947e-141">The following script runs indefinitely until the computer is rebooted, WMI is stopped, or the script is stopped.</span></span> <span data-ttu-id="e947e-142">Чтобы прерывать выполнение скрипта вручную, используйте диспетчер задач, чтобы прерывать процесс.</span><span class="sxs-lookup"><span data-stu-id="e947e-142">To stop the script manually, use Task Manager to stop the process.</span></span> <span data-ttu-id="e947e-143">Чтобы остановить его программно, используйте метод <a href="/windows/desktop/CIMWin32Prov/terminate-method-in-class-win32-process"><strong>Terminate</strong></a> в классе <a href="/windows/desktop/CIMWin32Prov/win32-process"><strong>Win32_Process</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="e947e-143">To stop it programmatically, use the <a href="/windows/desktop/CIMWin32Prov/terminate-method-in-class-win32-process"><strong>Terminate</strong></a> method in the <a href="/windows/desktop/CIMWin32Prov/win32-process"><strong>Win32_Process</strong></a> class.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e947e-144">VB</span><span class="sxs-lookup"><span data-stu-id="e947e-144">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; _
    & &quot;{impersonationLevel=impersonate}!\\&quot; _
    & strComputer & &quot;\root\cimv2&quot;)
set objRefresher = CreateObject(&quot;WbemScripting.Swbemrefresher&quot;)
Set objProcessor = objRefresher.AddEnum _
    (objWMIService, _
    &quot;Win32_PerfFormattedData_PerfOS_Processor&quot;).ObjectSet

While (True)
    objRefresher.Refresh
        For each RefreshItem in objRefresher
            For each objProcess in RefreshItem.ObjectSet
                Wscript.Echo objProcess.GetObjectText_
            Next
        Next
     Wscript.Sleep 5000
Wend</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e947e-145">... Получите и вычислите данные о производительности для процессов в Windows 2000?</span><span class="sxs-lookup"><span data-stu-id="e947e-145">...get and calculate performance data for processes on Windows 2000?</span></span></td>
<td><p><span data-ttu-id="e947e-146">Используйте &quot; Win32_PerfRawData &quot; классы, такие как <a href="/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data"><strong>Win32_PerfRawData_PerfProc_Process</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="e947e-146">Use the &quot;Win32_PerfRawData&quot; classes, such as <a href="/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data"><strong>Win32_PerfRawData_PerfProc_Process</strong></a>.</span></span> <span data-ttu-id="e947e-147">Дважды получите данные свойства, например <strong>перцентпроцессортиме</strong>, для определенного процесса.</span><span class="sxs-lookup"><span data-stu-id="e947e-147">Get the property data, such as <strong>PercentProcessorTime</strong>, twice for a specific process.</span></span> <span data-ttu-id="e947e-148">Найдите формулу, указанную в квалификаторе <a href="countertype-qualifier.md"><strong>CounterType</strong></a> для свойства, и вычислите ее.</span><span class="sxs-lookup"><span data-stu-id="e947e-148">Look up the formula specified in the <a href="countertype-qualifier.md"><strong>CounterType</strong></a> qualifier for the property and calculate.</span></span> <span data-ttu-id="e947e-149">CounterType в примере — <a href="/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10)">PERF_100NSEC_TIMER_INV</a>.</span><span class="sxs-lookup"><span data-stu-id="e947e-149">The CounterType in the example is <a href="/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10)">PERF_100NSEC_TIMER_INV</a>.</span></span> <span data-ttu-id="e947e-150">Дополнительные сведения см. в разделе <a href="monitoring-performance-data.md">наблюдение за данными производительности</a>.</span><span class="sxs-lookup"><span data-stu-id="e947e-150">For more information, see <a href="monitoring-performance-data.md">Monitoring Performance Data</a>.</span></span></p>
<p><span data-ttu-id="e947e-151">Следующий скрипт выполняется неограниченно до перезагрузки компьютера, Инструментарий WMI остановлен или сценарий остановлен.</span><span class="sxs-lookup"><span data-stu-id="e947e-151">The following script runs indefinitely until the computer is rebooted, WMI is stopped, or the script is stopped.</span></span> <span data-ttu-id="e947e-152">Чтобы прерывать выполнение скрипта вручную, используйте диспетчер задач, чтобы прерывать процесс.</span><span class="sxs-lookup"><span data-stu-id="e947e-152">To stop the script manually, use Task Manager to stop the process.</span></span> <span data-ttu-id="e947e-153">Чтобы остановить его программно, используйте метод <a href="/windows/desktop/CIMWin32Prov/terminate-method-in-class-win32-process"><strong>Terminate</strong></a> в классе <a href="/windows/desktop/CIMWin32Prov/win32-process"><strong>Win32_Process</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="e947e-153">To stop it programmatically, use the <a href="/windows/desktop/CIMWin32Prov/terminate-method-in-class-win32-process"><strong>Terminate</strong></a> method in the <a href="/windows/desktop/CIMWin32Prov/win32-process"><strong>Win32_Process</strong></a> class.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e947e-154">VB</span><span class="sxs-lookup"><span data-stu-id="e947e-154">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; _
    & &quot;{impersonationLevel=impersonate}!\\&quot; _
    & strComputer & &quot;\root\cimv2&quot;)

While (True)
    Set object1 = objWMIService.Get( _
    &quot;Win32_PerfRawData_PerfOS_Processor.Name=&#39;_Total&#39;&quot;)
    N1 = object1.PercentProcessorTime
    D1 = object1.TimeStamp_Sys100NS
    Wscript.Sleep(1000)
    set object2 = objWMIService.Get( _
    &quot;Win32_PerfRawData_PerfOS_Processor.Name=&#39;_Total&#39;&quot;)
    N2 = object2.PercentProcessorTime
    D2 = object2.TimeStamp_Sys100NS
    &#39; CounterType - PERF_100NSEC_TIMER_INV
    &#39; Formula - (1- ((N2 - N1) / (D2 - D1))) x 100
    PercentProcessorTime = (1 - ((N2 - N1)/(D2-D1)))*100
    Wscript.Echo &quot;% Processor Time=&quot; , PercentProcessorTime
Wend</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="e947e-155">См. также</span><span class="sxs-lookup"><span data-stu-id="e947e-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e947e-156">Задачи WMI для скриптов и приложений</span><span class="sxs-lookup"><span data-stu-id="e947e-156">WMI Tasks for Scripts and Applications</span></span>](wmi-tasks-for-scripts-and-applications.md)
</dt> <dt>

[<span data-ttu-id="e947e-157">Примеры приложений WMI на C++</span><span class="sxs-lookup"><span data-stu-id="e947e-157">WMI C++ Application Examples</span></span>](wmi-c---application-examples.md)
</dt> <dt>

[<span data-ttu-id="e947e-158">Скриптцентер TechNet</span><span class="sxs-lookup"><span data-stu-id="e947e-158">TechNet ScriptCenter</span></span>](https://www.microsoft.com/technet/scriptcenter)
</dt> </dl>
