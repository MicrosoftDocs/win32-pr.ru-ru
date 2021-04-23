---
description: Задачи WMI для журналов событий получают данные о событиях из файлов журнала событий и выполняют такие операции, как резервное копирование или очистка файлов журнала. Другие примеры см. в разделе TechNet Скриптцентер по адресу https://www.microsoft.com/technet .
ms.assetid: f6d4e68e-d757-44aa-be74-3b26168626b8
ms.tgt_platform: multiple
title: 'Задачи WMI: журналы событий '
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8fdcfe3f547e58fa60e552abad9867f8556fc8b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711728"
---
# <a name="wmi-tasks-event-logs"></a><span data-ttu-id="9b14d-104">Задачи WMI: журналы событий </span><span class="sxs-lookup"><span data-stu-id="9b14d-104">WMI Tasks: Event Logs</span></span>

<span data-ttu-id="9b14d-105">Задачи WMI для журналов событий получают данные о событиях из файлов журнала событий и выполняют такие операции, как резервное копирование или очистка файлов журнала.</span><span class="sxs-lookup"><span data-stu-id="9b14d-105">WMI tasks for event logs obtain event data from event log files and perform operations like backing up or clearing log files.</span></span> <span data-ttu-id="9b14d-106">Другие примеры см. в разделе TechNet Скриптцентер по адресу [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx) .</span><span class="sxs-lookup"><span data-stu-id="9b14d-106">For other examples, see the TechNet ScriptCenter at [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx).</span></span>

<span data-ttu-id="9b14d-107">Примеры сценариев, приведенные в этом разделе, получают данные только с локального компьютера.</span><span class="sxs-lookup"><span data-stu-id="9b14d-107">The script examples shown in this topic obtain data only from the local computer.</span></span> <span data-ttu-id="9b14d-108">Дополнительные сведения об использовании сценария для получения данных с удаленных компьютеров см. в разделе [Подключение к WMI на удаленном компьютере](connecting-to-wmi-on-a-remote-computer.md).</span><span class="sxs-lookup"><span data-stu-id="9b14d-108">For more information about how to use the script to obtain data from remote computers, see [Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span></span>


<span data-ttu-id="9b14d-109">В следующей процедуре описывается выполнение скрипта.</span><span class="sxs-lookup"><span data-stu-id="9b14d-109">The following procedure describes how to run a script.</span></span>

<span data-ttu-id="9b14d-110">**Запуск сценария**</span><span class="sxs-lookup"><span data-stu-id="9b14d-110">**To run a script**</span></span>

1.  <span data-ttu-id="9b14d-111">Скопируйте код и сохраните его в файле с расширением vbs, например *filename.vbs*.</span><span class="sxs-lookup"><span data-stu-id="9b14d-111">Copy the code and save it in a file with a .vbs extension, such as *filename.vbs*.</span></span> <span data-ttu-id="9b14d-112">Убедитесь, что текстовый редактор не добавляет расширение txt в файл.</span><span class="sxs-lookup"><span data-stu-id="9b14d-112">Ensure that your text editor does not add a .txt extension to the file.</span></span>
2.  <span data-ttu-id="9b14d-113">Откройте окно командной строки и перейдите в каталог, в котором был сохранен файл.</span><span class="sxs-lookup"><span data-stu-id="9b14d-113">Open a command prompt window and navigate to the directory where you saved the file.</span></span>
3.  <span data-ttu-id="9b14d-114">Введите **cscript filename.vbs** в командной строке.</span><span class="sxs-lookup"><span data-stu-id="9b14d-114">Type **cscript filename.vbs** at the command prompt.</span></span>
4.  <span data-ttu-id="9b14d-115">Если доступ к журналу событий невозможен, проверьте, выполняется ли в командной строке с повышенными привилегиями.</span><span class="sxs-lookup"><span data-stu-id="9b14d-115">If you cannot access an event log, check to see if you are running from an Elevated command prompt.</span></span> <span data-ttu-id="9b14d-116">Некоторые журналы событий, например журнал событий безопасности, могут быть защищены с помощью элементов управления доступом пользователей (UAC).</span><span class="sxs-lookup"><span data-stu-id="9b14d-116">Some Event Log, such as the Security Event Log, may be protected by User Access Controls (UAC).</span></span>

> [!Note]  
> <span data-ttu-id="9b14d-117">По умолчанию Cscript отображает выходные данные скрипта в окне командной строки.</span><span class="sxs-lookup"><span data-stu-id="9b14d-117">By default, cscript displays the output of a script in the command prompt window.</span></span> <span data-ttu-id="9b14d-118">Поскольку сценарии WMI могут создавать большие объемы выходных данных, может потребоваться перенаправить выходные данные в файл.</span><span class="sxs-lookup"><span data-stu-id="9b14d-118">Because WMI scripts can produce large amounts of output, you might want to redirect the output to a file.</span></span> <span data-ttu-id="9b14d-119">Введите **cscript filename.vbs > outfile.txt** в командной строке, чтобы перенаправить выходные данные скрипта *filename.vbs* в *outfile.txt*.</span><span class="sxs-lookup"><span data-stu-id="9b14d-119">Type **cscript filename.vbs > outfile.txt** at the command prompt to redirect the output of the *filename.vbs* script to *outfile.txt*.</span></span>

 

<span data-ttu-id="9b14d-120">В следующей таблице перечислены примеры сценариев, которые можно использовать для получения различных типов данных с локального компьютера.</span><span class="sxs-lookup"><span data-stu-id="9b14d-120">The following table lists script examples that can be used to obtain various types of data from the local computer.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9b14d-121">Часто выполняемые действия в новом интерфейсе</span><span class="sxs-lookup"><span data-stu-id="9b14d-121">How do I...</span></span></th>
<th><span data-ttu-id="9b14d-122">Классы или методы WMI</span><span class="sxs-lookup"><span data-stu-id="9b14d-122">WMI classes or methods</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9b14d-123">... получить сведения о журнале событий безопасности?</span><span class="sxs-lookup"><span data-stu-id="9b14d-123">...retrieve information about the Security event log?</span></span></td>
<td><span data-ttu-id="9b14d-124">Включите привилегии <a href="privilege-constants.md">безопасности</a> при подключении к классу <a href="/previous-versions/windows/desktop/legacy/aa394225(v=vs.85)"><strong>Win32_NTEventlogFile</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="9b14d-124">Include the <a href="privilege-constants.md">Security</a> privilege when connecting to the <a href="/previous-versions/windows/desktop/legacy/aa394225(v=vs.85)"><strong>Win32_NTEventlogFile</strong></a> class.</span></span> <span data-ttu-id="9b14d-125">Дополнительные сведения см. в статье <a href="executing-privileged-operations-using-vbscript.md">выполнение привилегированных операций с помощью VBScript</a>.</span><span class="sxs-lookup"><span data-stu-id="9b14d-125">For more information, see <a href="executing-privileged-operations-using-vbscript.md">Executing Privileged Operations Using VBScript</a>.</span></span><br/> <span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9b14d-126">VB</span><span class="sxs-lookup"><span data-stu-id="9b14d-126">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; _
    & &quot;{impersonationLevel=impersonate,(Security)}!\\&quot; & _
        strComputer & &quot;\root\cimv2&quot;)
Set colLogFiles = objWMIService.ExecQuery _
    (&quot;Select * from Win32_NTEventLogFile &quot; _
        & &quot;Where LogFileName=&#39;Security&#39;&quot;)
For Each objLogFile in colLogFiles
    Wscript.Echo objLogFile.NumberOfRecords
    Wscript.Echo &quot;Maximum Size: &quot; _
    &  objLogfile.MaxFileSize 
Next</code></pre></td>
</tr>
</tbody>
</table>
<span data-codelanguage="PowerShell"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9b14d-127">PowerShell</span><span class="sxs-lookup"><span data-stu-id="9b14d-127">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$strComputer = &quot;.&quot;
$colLogFiles = Get-WmiObject -Class Win32_NTEventLogFile -ComputerName $strComputer | Where-Object {$_.LogFileName -eq &#39;security&#39;}
foreach ($objLogFile in $colLogFiles) 
{ 
    &quot;Record Number: &quot; + $objLogFile.NumberOfRecords
    &quot;Maximum Size: &quot; + $objLogFile.MaxFileSize
}</code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="9b14d-128">... создать резервную копию журнала событий?</span><span class="sxs-lookup"><span data-stu-id="9b14d-128">...back up an event log?</span></span></td>
<td><p><span data-ttu-id="9b14d-129">Используйте класс <a href="/previous-versions/windows/desktop/legacy/aa394225(v=vs.85)"><strong>Win32_NTEventlogFile</strong></a> и метод <a href="/previous-versions/windows/desktop/eventlogprov/backupeventlog-method-in-class-win32-nteventlogfile"><strong>баккупевентлог</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="9b14d-129">Use the <a href="/previous-versions/windows/desktop/legacy/aa394225(v=vs.85)"><strong>Win32_NTEventlogFile</strong></a> class and the <a href="/previous-versions/windows/desktop/eventlogprov/backupeventlog-method-in-class-win32-nteventlogfile"><strong>BackupEventLog</strong></a> method.</span></span> <span data-ttu-id="9b14d-130">При подключении к WMI может потребоваться включить право на <a href="privilege-constants.md">резервное копирование</a> .</span><span class="sxs-lookup"><span data-stu-id="9b14d-130">You may need to include the <a href="privilege-constants.md">Backup</a> privilege when connecting to WMI.</span></span> <span data-ttu-id="9b14d-131">Дополнительные сведения см. в статье <a href="executing-privileged-operations-using-vbscript.md">выполнение привилегированных операций с помощью VBScript</a>.</span><span class="sxs-lookup"><span data-stu-id="9b14d-131">For more information, see <a href="executing-privileged-operations-using-vbscript.md">Executing Privileged Operations Using VBScript</a>.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9b14d-132">VB</span><span class="sxs-lookup"><span data-stu-id="9b14d-132">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate,(Backup)}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colLogFiles = objWMIService.ExecQuery (&quot;Select * from Win32_NTEventLogFile &quot; & &quot;Where LogFileName=&#39;Application&#39;&quot;)
For Each objLogfile in colLogFiles
    errBackupLog = objLogFile.BackupEventLog(&quot;c:\scripts\application.evt&quot;)
    WScript.Echo &quot;File saved as c:\scripts\applications.evt&quot;
Next</code></pre></td>
</tr>
</tbody>
</table>
<span data-codelanguage="PowerShell"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9b14d-133">PowerShell</span><span class="sxs-lookup"><span data-stu-id="9b14d-133">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$strComputer = &quot;.&quot;
$colLogFiles = Get-WmiObject -Class Win32_NTEventLogFile -ComputerName $strComputer | Where-Object {$_.LogFileName -eq &#39;Application&#39;}

foreach ($objLogFile in $colLogFiles) 
{ 
    [void]$objLogFile.BackupEventlog(&quot;c:\scripts\applications.evt&quot;)
    &quot;File saved as c:\scripts\applications.evt&quot;
}</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9b14d-134">... создать резервную копию журнала событий более одного раза?</span><span class="sxs-lookup"><span data-stu-id="9b14d-134">...back up an event log more than once?</span></span></td>
<td><p><span data-ttu-id="9b14d-135">Перед использованием <a href="/previous-versions/windows/desktop/legacy/aa394225(v=vs.85)"><strong>Win32_NTEventlogFile</strong></a> и метода <a href="/previous-versions/windows/desktop/eventlogprov/backupeventlog-method-in-class-win32-nteventlogfile"><strong>баккупевентлог</strong></a> убедитесь, что файл резервной копии имеет уникальное имя.</span><span class="sxs-lookup"><span data-stu-id="9b14d-135">Ensure that the backup file has a unique name before using the <a href="/previous-versions/windows/desktop/legacy/aa394225(v=vs.85)"><strong>Win32_NTEventlogFile</strong></a> and the <a href="/previous-versions/windows/desktop/eventlogprov/backupeventlog-method-in-class-win32-nteventlogfile"><strong>BackupEventLog</strong></a> method.</span></span> <span data-ttu-id="9b14d-136">Операционная система не позволяет перезаписать существующий файл резервной копии; необходимо либо переместить файл резервной копии, либо переименовать его, прежде чем можно будет запустить сценарий снова.</span><span class="sxs-lookup"><span data-stu-id="9b14d-136">The operating system does not allow you to overwrite an existing backup file; you must either move the backup file or rename it before you can run the script again.</span></span> <span data-ttu-id="9b14d-137">При подключении к WMI может потребоваться включить право на <a href="privilege-constants.md">резервное копирование</a> .</span><span class="sxs-lookup"><span data-stu-id="9b14d-137">You may need to include the <a href="privilege-constants.md">Backup</a> privilege when connecting to WMI.</span></span> <span data-ttu-id="9b14d-138">Дополнительные сведения см. в статье <a href="executing-privileged-operations-using-vbscript.md">выполнение привилегированных операций с помощью VBScript</a>.</span><span class="sxs-lookup"><span data-stu-id="9b14d-138">For more information, see <a href="executing-privileged-operations-using-vbscript.md">Executing Privileged Operations Using VBScript</a>.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9b14d-139">VB</span><span class="sxs-lookup"><span data-stu-id="9b14d-139">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>dtmThisDay = Day(Date)
dtmThisMonth = Month(Date)
dtmThisYear = Year(Date)
strBackupName = dtmThisYear & &quot;_&quot; & dtmThisMonth & &quot;_&quot; & dtmThisDay
strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate,(Backup)}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colLogFiles = objWMIService.ExecQuery (&quot;Select * from Win32_NTEventLogFile &quot; & &quot;Where LogFileName=&#39;Application&#39;&quot;)
For Each objLogfile in colLogFiles
    objLogFile.BackupEventLog(&quot;c:\scripts\&quot; & strBackupName & &quot;_application.evt&quot;)
    objLogFile.ClearEventLog()
    WScript.Echo &quot;File saved: &quot; & strBackupName & &quot;_application.evt&quot;
Next</code></pre></td>
</tr>
</tbody>
</table>
<span data-codelanguage="PowerShell"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9b14d-140">PowerShell</span><span class="sxs-lookup"><span data-stu-id="9b14d-140">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$CurDate = Get-Date
$strBackupName = $curDate.Year.ToString() + &quot;_&quot; + $curDate.Month.ToString() + &quot;_&quot; + $CurDate.Day.ToString()

$strComputer = &quot;.&quot;
$colLogFiles = Get-WmiObject -Class Win32_NTEventLogFile -ComputerName $strComputer | Where-Object {$_.LogFileName -eq &#39;Application&#39;}
foreach ($objLogFile in $colLogFiles) 
{ 
    $BackupFile = $objLogFile.BackupEventlog(&quot;c:\scripts\&quot; + $strBackupName + &quot;_application.evt&quot;)
    &quot;File saved: c:\scripts\&quot; + $strBackupName + &quot;_application.evt&quot;
}</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9b14d-141">... определить количество записей в журнале событий?</span><span class="sxs-lookup"><span data-stu-id="9b14d-141">...determine the number of records in an event log?</span></span></td>
<td><p><span data-ttu-id="9b14d-142">Используйте класс <a href="/previous-versions/windows/desktop/legacy/aa394225(v=vs.85)"><strong>Win32_NTEventlogFile</strong></a> и проверьте значение свойства <strong>нумберофрекордс</strong> .</span><span class="sxs-lookup"><span data-stu-id="9b14d-142">Use the <a href="/previous-versions/windows/desktop/legacy/aa394225(v=vs.85)"><strong>Win32_NTEventlogFile</strong></a> class and check the value of the <strong>NumberOfRecords</strong> property.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9b14d-143">VB</span><span class="sxs-lookup"><span data-stu-id="9b14d-143">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colLogFiles = objWMIService.ExecQuery (&quot;Select * from Win32_NTEventLogFile &quot; & &quot;Where LogFileName=&#39;System&#39;&quot;)
For Each objLogFile in colLogFiles
    Wscript.Echo objLogFile.NumberOfRecords
Next</code></pre></td>
</tr>
</tbody>
</table>
<span data-codelanguage="PowerShell"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9b14d-144">PowerShell</span><span class="sxs-lookup"><span data-stu-id="9b14d-144">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$strComputer = &quot;.&quot;
$colLogFiles = Get-WmiObject -Class Win32_NTEventLogFile -ComputerName $strComputer | Where-Object {$_.LogFileName -eq &#39;System&#39;}

foreach ($objLogFile in $colLogFiles) 
{ 
    $objLogFile.NumberOfRecords
}</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9b14d-145">... очистить журналы событий?</span><span class="sxs-lookup"><span data-stu-id="9b14d-145">...clear my event logs?</span></span></td>
<td><p><span data-ttu-id="9b14d-146">Используйте класс <a href="/previous-versions/windows/desktop/legacy/aa394225(v=vs.85)"><strong>Win32_NTEventlogFile</strong></a> и метод <a href="/previous-versions/windows/desktop/eventlogprov/cleareventlog-method-in-class-win32-nteventlogfile"><strong>клеаревентлог</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="9b14d-146">Use the <a href="/previous-versions/windows/desktop/legacy/aa394225(v=vs.85)"><strong>Win32_NTEventlogFile</strong></a> class and the <a href="/previous-versions/windows/desktop/eventlogprov/cleareventlog-method-in-class-win32-nteventlogfile"><strong>ClearEventLog</strong></a> method.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9b14d-147">VB</span><span class="sxs-lookup"><span data-stu-id="9b14d-147">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate,(Backup, Security)}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colLogFiles = objWMIService.ExecQuery (&quot;Select * from Win32_NTEventLogFile &quot; & &quot;Where LogFileName=&#39;Application&#39;&quot;)
For Each objLogfile in colLogFiles
    objLogFile.ClearEventLog()
    WScript.Echo &quot;Cleared application event log file&quot;
Next</code></pre></td>
</tr>
</tbody>
</table>
<span data-codelanguage="PowerShell"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9b14d-148">PowerShell</span><span class="sxs-lookup"><span data-stu-id="9b14d-148">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$strComputer = &quot;.&quot;
$colLogFiles = Get-WmiObject -Class Win32_NTEventLogFile -ComputerName $strComputer | Where-Object {$_.LogFileName -eq &#39;System&#39;}

foreach ($objLogFile in $colLogFiles) 
{ 
    [void]$objLogFile.ClearEventlog()
    &quot;Cleared application event log file&quot;
}</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9b14d-149">... читать события из журналов событий?</span><span class="sxs-lookup"><span data-stu-id="9b14d-149">...read events from the event logs?</span></span></td>
<td><p><span data-ttu-id="9b14d-150">Используйте класс <a href="/previous-versions/windows/desktop/eventlogprov/win32-ntlogevent"><strong>Win32_NTLogEvent</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="9b14d-150">Use the <a href="/previous-versions/windows/desktop/eventlogprov/win32-ntlogevent"><strong>Win32_NTLogEvent</strong></a> class.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9b14d-151">VB</span><span class="sxs-lookup"><span data-stu-id="9b14d-151">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; _
    & &quot;{impersonationLevel=impersonate}!\\&quot; _
    & strComputer & &quot;\root\cimv2&quot;)
Set colLoggedEvents = objWMIService.ExecQuery _
    (&quot;Select * from Win32_NTLogEvent &quot; _
        & &quot;Where Logfile = &#39;System&#39;&quot;)
For Each objEvent in colLoggedEvents
    Wscript.Echo &quot;Category: &quot; & objEvent.Category & VBNewLine _
    & &quot;Computer Name: &quot; & objEvent.ComputerName & VBNewLine _
    & &quot;Event Code: &quot; & objEvent.EventCode & VBNewLine _
    & &quot;Message: &quot; & objEvent.Message & VBNewLine _
    & &quot;Record Number: &quot; & objEvent.RecordNumber & VBNewLine _
    & &quot;Source Name: &quot; & objEvent.SourceName & VBNewLine _
    & &quot;Time Written: &quot; & objEvent.TimeWritten & VBNewLine _
    & &quot;Event Type: &quot; & objEvent.Type & VBNewLine _
    & &quot;User: &quot; & objEvent.User
Next</code></pre></td>
</tr>
</tbody>
</table>
<span data-codelanguage="PowerShell"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9b14d-152">PowerShell</span><span class="sxs-lookup"><span data-stu-id="9b14d-152">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$strComputer = &quot;.&quot;
$colLogFiles = Get-WmiObject -Class Win32_NTLogEvent -ComputerName $strComputer | Where-Object {$_.LogFile -eq &#39;System&#39;}

foreach ($objEvent in $colLoggedEvents) 
{ 
    &quot;Category: &quot; + $objEvent.Category
    &quot;Computer Name: &quot; + $objEvent.ComputerName
    &quot;Event Code: &quot; + $objEvent.EventCode
    &quot;Message: &quot; + $objEvent.Message
    &quot;Record Number: &quot; + $objEvent.RecordNumber
    &quot;Source Name: &quot; + $objEvent.SourceName
    &quot;Time Written: &quot; + $objEvent.TimeWritten
    &quot;Event Type: &quot; + $objEvent.Type
    &quot;User: &quot; + $objEvent.Use
}</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="9b14d-153">См. также</span><span class="sxs-lookup"><span data-stu-id="9b14d-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9b14d-154">Задачи WMI для скриптов и приложений</span><span class="sxs-lookup"><span data-stu-id="9b14d-154">WMI Tasks for Scripts and Applications</span></span>](wmi-tasks-for-scripts-and-applications.md)
</dt> <dt>

[<span data-ttu-id="9b14d-155">Примеры приложений WMI на C++</span><span class="sxs-lookup"><span data-stu-id="9b14d-155">WMI C++ Application Examples</span></span>](wmi-c---application-examples.md)
</dt> <dt>

[<span data-ttu-id="9b14d-156">Скриптцентер TechNet</span><span class="sxs-lookup"><span data-stu-id="9b14d-156">TechNet ScriptCenter</span></span>](https://www.microsoft.com/technet/scriptcenter)
</dt> </dl>

