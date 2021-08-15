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
ms.openlocfilehash: 91302b0d6c6e13f86f275d755c5f4b6150de6a59dd400e47ed877d01f3fe876e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118312060"
---
# <a name="wmi-tasks-performance-monitoring"></a>Задачи WMI: Мониторинг производительности

Используйте классы WMI, которые получают данные из счетчиков производительности для доступа и обновления данных о производительности компьютера. Другие примеры см. в разделе TechNet Скриптцентер по адресу [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx) . Дополнительные сведения см. в разделе [библиотеки производительности и инструментарий WMI](performance-libraries-and-wmi.md) и [наблюдение за данными производительности](monitoring-performance-data.md).

Примеры сценариев, приведенные в этом разделе, получают данные только с локального компьютера. Дополнительные сведения об использовании сценария для получения данных с удаленных компьютеров см. в разделе [Подключение к WMI на удаленном компьютере](connecting-to-wmi-on-a-remote-computer.md).


В следующей процедуре описывается выполнение скрипта.

**Запуск сценария**

1.  Скопируйте код и сохраните его в файле с расширением vbs, например *filename.vbs*. Убедитесь, что текстовый редактор не добавляет к файлу расширение .txt.
2.  Откройте окно командной строки и перейдите в каталог, в котором был сохранен файл.
3.  Введите **cscript filename.vbs** в командной строке.
4.  Если доступ к журналу событий невозможен, проверьте, выполняется ли в командной строке с повышенными привилегиями. Некоторые журналы событий, например журнал событий безопасности, могут быть защищены с помощью элементов управления доступом пользователей (UAC).

> [!Note]  
> По умолчанию Cscript отображает выходные данные скрипта в окне командной строки. Поскольку сценарии WMI могут создавать большие объемы выходных данных, может потребоваться перенаправить выходные данные в файл. Введите **cscript filename.vbs > outfile.txt** в командной строке, чтобы перенаправить выходные данные скрипта *filename.vbs* в *outfile.txt*.

 

В следующей таблице перечислены примеры сценариев, которые можно использовать для получения различных типов данных с локального компьютера.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Часто выполняемые действия в новом интерфейсе</th>
<th>Классы или методы WMI</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>... получить данные счетчиков производительности, которые можно увидеть в программе Perfmon в сценарии?</td>
<td>Используйте классы, имена которых начинаются с &quot; <a href="/windows/desktop/CIMWin32Prov/performance-counter-classes">Win32_PerfFormattedData</a> &quot; , например <a href="/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data"><strong>Win32_PerfFormattedData_PerfProc_Process</strong></a>. Свойства с именами, например <strong>пажефилебитес</strong> , соответствуют счетчикам производительности, отображаемым в PerfMon. &quot;Win32_PerfFormattedData &quot; классы вычисляют конечные значения счетчиков автоматически.<br/></td>
</tr>
<tr class="even">
<td>... Получайте актуальные данные о производительности для одного процесса, диска и других данных?</td>
<td>Используйте <a href="/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data"><strong>Win32_PerfFormattedData_PerfProc_Process</strong></a> или соответствующий <a href="/windows/desktop/CIMWin32Prov/performance-counter-classes">класс счетчика производительности</a> и метод <a href="swbemobjectex-refresh-.md"><strong>SWbemObjectEx.Refresh_</strong></a> . Дополнительные сведения см. в разделе <a href="scripting-with-swbemobject.md">Создание скриптов с помощью SWbemObject</a>.<br/> В C++ используйте <a href="/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemconfigurerefresher-addobjectbypath"><strong>ивбемконфигуререфрешер:: аддобжектбипас</strong></a> и <a href="/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh"><strong>Ивбемрефрешер:: Refresh</strong></a>. Дополнительные сведения см. в разделе <a href="monitoring-performance-data.md">наблюдение за данными производительности</a>.<br/> Следующий сценарий выполняется до перезагрузки компьютера, Инструментарий WMI остановлен или сценарий остановлен. Чтобы прерывать выполнение скрипта вручную, используйте диспетчер задач, чтобы прерывать процесс. Чтобы остановить его программно, используйте метод <a href="/windows/desktop/CIMWin32Prov/terminate-method-in-class-win32-process"><strong>Terminate</strong></a> в классе <a href="/windows/desktop/CIMWin32Prov/win32-process"><strong>Win32_Process</strong></a> .<br/> <span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>VB</th>
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
<td>... получать актуальные данные о производительности для всех процессов без повторяющегося опроса?</td>
<td><p>Используйте классы, имена которых начинаются с &quot; Win32_PerfFormattedData &quot; и объекта <a href="swbemrefresher.md"><strong>свбемрефрешер</strong></a> . Обновитель содержит объекты, поэтому вам не нужно многократно получать коллекцию. Для вычисления данных о производительности требуется как минимум два значения, так как большинство счетчиков являются счетчиками скорости. При первом отображении данные для обновления будут пустыми.</p>
<p>Следующий скрипт выполняется неограниченно до перезагрузки компьютера, Инструментарий WMI остановлен или сценарий остановлен. Чтобы прерывать выполнение скрипта вручную, используйте диспетчер задач, чтобы прерывать процесс. Чтобы остановить его программно, используйте метод <a href="/windows/desktop/CIMWin32Prov/terminate-method-in-class-win32-process"><strong>Terminate</strong></a> в классе <a href="/windows/desktop/CIMWin32Prov/win32-process"><strong>Win32_Process</strong></a> .</p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>VB</th>
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
<td>... получите и вычислите данные о производительности для процессов на Windows 2000?</td>
<td><p>Используйте &quot; Win32_PerfRawData &quot; классы, такие как <a href="/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data"><strong>Win32_PerfRawData_PerfProc_Process</strong></a>. Дважды получите данные свойства, например <strong>перцентпроцессортиме</strong>, для определенного процесса. Найдите формулу, указанную в квалификаторе <a href="countertype-qualifier.md"><strong>CounterType</strong></a> для свойства, и вычислите ее. CounterType в примере — <a href="/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10)">PERF_100NSEC_TIMER_INV</a>. Дополнительные сведения см. в разделе <a href="monitoring-performance-data.md">наблюдение за данными производительности</a>.</p>
<p>Следующий скрипт выполняется неограниченно до перезагрузки компьютера, Инструментарий WMI остановлен или сценарий остановлен. Чтобы прерывать выполнение скрипта вручную, используйте диспетчер задач, чтобы прерывать процесс. Чтобы остановить его программно, используйте метод <a href="/windows/desktop/CIMWin32Prov/terminate-method-in-class-win32-process"><strong>Terminate</strong></a> в классе <a href="/windows/desktop/CIMWin32Prov/win32-process"><strong>Win32_Process</strong></a> .</p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>VB</th>
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



 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Задачи WMI для скриптов и приложений](wmi-tasks-for-scripts-and-applications.md)
</dt> <dt>

[Примеры приложений WMI на C++](wmi-c---application-examples.md)
</dt> <dt>

[Скриптцентер TechNet](https://www.microsoft.com/technet/scriptcenter)
</dt> </dl>
