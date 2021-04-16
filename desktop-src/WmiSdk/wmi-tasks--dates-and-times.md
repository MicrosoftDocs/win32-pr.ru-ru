---
description: Существует несколько классов WMI и объект скрипта для анализа или преобразования формата даты и времени CIM. Другие примеры см. в разделе TechNet Скриптцентер по адресу https://www.microsoft.com/technet .
ms.assetid: dd01a732-5c88-4c24-a551-4d5452e712cc
ms.tgt_platform: multiple
title: 'Задачи WMI: даты и время'
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8864deb4f76b8ce6b76017c0348cdb86bf38b697
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712890"
---
# <a name="wmi-tasks-dates-and-times"></a><span data-ttu-id="2a1c5-104">Задачи WMI: даты и время</span><span class="sxs-lookup"><span data-stu-id="2a1c5-104">WMI Tasks: Dates and Times</span></span>

<span data-ttu-id="2a1c5-105">Существует несколько классов WMI и объект скрипта для анализа или преобразования формата даты и [времени CIM](date-and-time-format.md) .</span><span class="sxs-lookup"><span data-stu-id="2a1c5-105">There are several WMI classes and a scripting object to parse or convert the [CIM datetime](date-and-time-format.md) format.</span></span> <span data-ttu-id="2a1c5-106">Другие примеры см. в разделе TechNet Скриптцентер по адресу [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx) .</span><span class="sxs-lookup"><span data-stu-id="2a1c5-106">For other examples, see the TechNet ScriptCenter at [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx).</span></span>

<span data-ttu-id="2a1c5-107">Примеры сценариев, приведенные в этом разделе, получают данные только с локального компьютера.</span><span class="sxs-lookup"><span data-stu-id="2a1c5-107">The script examples shown in this topic obtain data only from the local computer.</span></span> <span data-ttu-id="2a1c5-108">Дополнительные сведения об использовании сценария для получения данных с удаленных компьютеров см. в разделе [Подключение к WMI на удаленном компьютере](connecting-to-wmi-on-a-remote-computer.md).</span><span class="sxs-lookup"><span data-stu-id="2a1c5-108">For more information about how to use the script to obtain data from remote computers, see [Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span></span>

## <a name="to-run-a-script"></a><span data-ttu-id="2a1c5-109">Запуск сценария</span><span class="sxs-lookup"><span data-stu-id="2a1c5-109">To run a script</span></span>

<span data-ttu-id="2a1c5-110">В следующей процедуре описывается выполнение скрипта.</span><span class="sxs-lookup"><span data-stu-id="2a1c5-110">The following procedure describes how to run a script.</span></span>

1.  <span data-ttu-id="2a1c5-111">Скопируйте код и сохраните его в файле с расширением vbs, например *filename.vbs*.</span><span class="sxs-lookup"><span data-stu-id="2a1c5-111">Copy the code and save it in a file with a .vbs extension, such as *filename.vbs*.</span></span> <span data-ttu-id="2a1c5-112">Убедитесь, что текстовый редактор не добавляет расширение txt в файл.</span><span class="sxs-lookup"><span data-stu-id="2a1c5-112">Ensure that your text editor does not add a .txt extension to the file.</span></span>
2.  <span data-ttu-id="2a1c5-113">Откройте окно командной строки и перейдите в каталог, в котором был сохранен файл.</span><span class="sxs-lookup"><span data-stu-id="2a1c5-113">Open a command prompt window and navigate to the directory where you saved the file.</span></span>
3.  <span data-ttu-id="2a1c5-114">Введите **cscript filename.vbs** в командной строке.</span><span class="sxs-lookup"><span data-stu-id="2a1c5-114">Type **cscript filename.vbs** at the command prompt.</span></span>
4.  <span data-ttu-id="2a1c5-115">Если доступ к журналу событий невозможен, проверьте, выполняется ли в командной строке с повышенными привилегиями.</span><span class="sxs-lookup"><span data-stu-id="2a1c5-115">If you cannot access an event log, check to see if you are running from an Elevated command prompt.</span></span> <span data-ttu-id="2a1c5-116">Некоторые журналы событий, например журнал событий безопасности, могут быть защищены с помощью элементов управления доступом пользователей (UAC).</span><span class="sxs-lookup"><span data-stu-id="2a1c5-116">Some Event Log, such as the Security Event Log, may be protected by User Access Controls (UAC).</span></span>

> [!Note]  
> <span data-ttu-id="2a1c5-117">По умолчанию Cscript отображает выходные данные скрипта в окне командной строки.</span><span class="sxs-lookup"><span data-stu-id="2a1c5-117">By default, cscript displays the output of a script in the command prompt window.</span></span> <span data-ttu-id="2a1c5-118">Поскольку сценарии WMI могут создавать большие объемы выходных данных, может потребоваться перенаправить выходные данные в файл.</span><span class="sxs-lookup"><span data-stu-id="2a1c5-118">Because WMI scripts can produce large amounts of output, you might want to redirect the output to a file.</span></span> <span data-ttu-id="2a1c5-119">Введите **cscript filename.vbs > outfile.txt** в командной строке, чтобы перенаправить выходные данные скрипта *filename.vbs* в *outfile.txt*.</span><span class="sxs-lookup"><span data-stu-id="2a1c5-119">Type **cscript filename.vbs > outfile.txt** at the command prompt to redirect the output of the *filename.vbs* script to *outfile.txt*.</span></span>

 

<span data-ttu-id="2a1c5-120">В следующей таблице перечислены примеры сценариев, которые можно использовать для получения различных типов данных с локального компьютера.</span><span class="sxs-lookup"><span data-stu-id="2a1c5-120">The following table lists script examples that can be used to obtain various types of data from the local computer.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2a1c5-121">Часто выполняемые действия в новом интерфейсе</span><span class="sxs-lookup"><span data-stu-id="2a1c5-121">How do I...</span></span></th>
<th><span data-ttu-id="2a1c5-122">Классы или методы WMI</span><span class="sxs-lookup"><span data-stu-id="2a1c5-122">WMI classes or methods</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2a1c5-123">... преобразовывать даты WMI в стандартные даты и время?</span><span class="sxs-lookup"><span data-stu-id="2a1c5-123">...convert WMI dates to standard dates and times?</span></span><br/></td>
<td><span data-ttu-id="2a1c5-124">Используйте объект <a href="swbemdatetime.md"><strong>SWbemDateTime</strong></a> для преобразования их в обычные даты и время.</span><span class="sxs-lookup"><span data-stu-id="2a1c5-124">Use the <a href="swbemdatetime.md"><strong>SWbemDateTime</strong></a> object to convert these to regular dates and times.</span></span><br/> <span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2a1c5-125">VB</span><span class="sxs-lookup"><span data-stu-id="2a1c5-125">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>Set dtmInstallDate = CreateObject(&quot;WbemScripting.SWbemDateTime&quot;)
strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set objOS = objWMIService.ExecQuery(&quot;Select * from Win32_OperatingSystem&quot;)
For Each strOS in objOS
    dtmInstallDate.Value = strOS.InstallDate
    Wscript.Echo dtmInstallDate.GetVarDate
Next</code></pre></td>
</tr>
</tbody>
</table>

<p><span data-ttu-id="2a1c5-126">Или попросите своего кода выполнить задачу вручную.</span><span class="sxs-lookup"><span data-stu-id="2a1c5-126">Or have your code do the task manually.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2a1c5-127">VB</span><span class="sxs-lookup"><span data-stu-id="2a1c5-127">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>Function WMIDateStringToDate(dtmInstallDate) 
    WMIDateStringToDate = CDate(Mid(dtmInstallDate, 5, 2) & &quot;/&quot; & Mid(dtmInstallDate, 7, 2) _
                        & &quot;/&quot; & Left(dtmInstallDate, 4) & &quot; &quot; & Mid (dtmInstallDate, 9, 2) & &quot;:&quot; _
                        & Mid(dtmInstallDate, 11, 2) & &quot;:&quot; & Mid(dtmInstallDate,13, 2)) 
End Function </code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2a1c5-128">... определить текущее время, настроенное на компьютере?</span><span class="sxs-lookup"><span data-stu-id="2a1c5-128">...determine the time currently configured on a computer?</span></span></p></td>
<td><p><span data-ttu-id="2a1c5-129">Используйте класс <a href="/previous-versions/windows/desktop/wmitimepprov/win32-localtime"><strong>Win32_LocalTime</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="2a1c5-129">Use the <a href="/previous-versions/windows/desktop/wmitimepprov/win32-localtime"><strong>Win32_LocalTime</strong></a> class.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2a1c5-130">VB</span><span class="sxs-lookup"><span data-stu-id="2a1c5-130">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colItems = objWMIService.ExecQuery(&quot;Select * from Win32_LocalTime&quot;)
For Each objItem in colItems
    Wscript.Echo &quot;Day:           &quot; & objItem.Day & VBNewLine _
               & &quot;Day Of Week:   &quot; & objItem.DayOfWeek & VBNewLine _
               & &quot;Hour:          &quot; & objItem.Hour & VBNewLine _
               & &quot;Minute:        &quot; & objItem.Minute & VBNewLine _
               & &quot;Month:         &quot; & objItem.Month & VBNewLine _
               & &quot;Quarter:       &quot; & objItem.Quarter & VBNewLine _
               & &quot;Second:        &quot; & objItem.Second & VBNewLine _
               & &quot;Week In Month: &quot; & objItem.WeekInMonth & VBNewLine _
               & &quot;Year:          &quot; & objItem.Year 
Next</code></pre></td>
</tr>
</tbody>
</table>

</div>
<div class="code">
<span data-codelanguage="PowerShell"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2a1c5-131">PowerShell</span><span class="sxs-lookup"><span data-stu-id="2a1c5-131">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code># Specify computer and get Local Time
$Computer = &quot;.&quot;
$times = Get-WmiObject Win32_LocalTime -computer $computer

<# Now display the result #>

Foreach ($time in $times) {
    &quot;Day : {0}&quot; -f $Time.Day
    &quot;Day Of Week : {0}&quot; -f $Time.DayOfWeek
    &quot;Hour : {0}&quot; -f $Time.Hour
    &quot;Minute : {0}&quot; -f $Time.Minute
    &quot;Month : {0}&quot; -f $Time.Month
    &quot;Quarter : {0}&quot; -f $Time.Quarter
    &quot;Second : {0}&quot; -f $time.Second 
    &quot;Week In Month: {0}&quot; -f $Time.WeekInMonth 
    &quot;Year : {0}&quot; -f $Time.Year 
}</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2a1c5-132">... определить имя часового пояса, в котором работает компьютер?</span><span class="sxs-lookup"><span data-stu-id="2a1c5-132">...determine the name of the time zone in which a computer is running?</span></span></p></td>
<td><p><span data-ttu-id="2a1c5-133">Используйте класс <a href="/windows/desktop/CIMWin32Prov/win32-timezone"><strong>Win32_TimeZone</strong></a> и проверьте значение свойства <strong>Description</strong> .</span><span class="sxs-lookup"><span data-stu-id="2a1c5-133">Use the <a href="/windows/desktop/CIMWin32Prov/win32-timezone"><strong>Win32_TimeZone</strong></a> class and check the value of the <strong>Description</strong> property.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2a1c5-134">VB</span><span class="sxs-lookup"><span data-stu-id="2a1c5-134">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colItems = objWMIService.ExecQuery(&quot;Select * from Win32_TimeZone&quot;)
For Each objItem in colItems
    Wscript.Echo &quot;Description:   &quot; & objItem.Description
    Wscript.Echo &quot;Daylight Name: &quot; & objItem.DaylightName
    Wscript.Echo &quot;Standard Name: &quot; & objItem.StandardName
    Wscript.Echo
Next</code></pre></td>
</tr>
</tbody>
</table>

</div>
<div class="code">
<span data-codelanguage="PowerShell"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2a1c5-135">PowerShell</span><span class="sxs-lookup"><span data-stu-id="2a1c5-135">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$Computer = &quot;.&quot;  
$timezone = Get-WMIObject -class Win32_TimeZone -ComputerName $computer  
  
<# Display details  #>
if ($computer -eq &quot;.&quot;) {$computer = Hostname}  
&quot;Time zone information on computer `&quot;{0}`&quot;&quot; -f $computer  
&quot;Time Zone Description   : {0}&quot; -f $timezone.Description  
&quot;Daylight Name           : {0}&quot; -f $timezone.DaylightName  
&quot;Standard Name           : {0}&quot; -f $timezone.StandardName  </code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2a1c5-136">... Убедитесь, что &quot; 10/02/2000 &quot; интерпретируется как Oct. 2, 2000, а не &quot; 10 февраля, 2000 &quot; ?</span><span class="sxs-lookup"><span data-stu-id="2a1c5-136">...ensure that &quot;10/02/2000&quot; is interpreted as Oct. 2, 2000, not &quot;10 Feb, 2000&quot;?</span></span></p></td>
<td><p><span data-ttu-id="2a1c5-137">Управление датами в формате <a href="datetime.md">даты и времени</a> <a href="gloss-c.md"><em>CIM</em></a> и использование методов <a href="swbemdatetime.md"><strong>SWbemDateTime</strong></a> , таких как <a href="swbemdatetime-getvardate.md"><strong>GetVarDate</strong></a> , для преобразования в них в форматах <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime"><strong>fileTime</strong></a> или <strong>VT_Date</strong> .</span><span class="sxs-lookup"><span data-stu-id="2a1c5-137">Manage dates in <a href="gloss-c.md"><em>CIM</em></a> <a href="datetime.md">DATETIME</a> format and use <a href="swbemdatetime.md"><strong>SWbemDateTime</strong></a> methods, such as <a href="swbemdatetime-getvardate.md"><strong>GetVarDate</strong></a> to convert to them to and from either <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime"><strong>FILETIME</strong></a> or <strong>VT_Date</strong> formats.</span></span> <span data-ttu-id="2a1c5-138">Так как формат DATETIME не зависит от языкового стандарта, можно написать сценарий, который выполняется на любом компьютере.</span><span class="sxs-lookup"><span data-stu-id="2a1c5-138">Because DATETIME format is locale-independent, you can write a script that runs on any machine.</span></span> <span data-ttu-id="2a1c5-139">Используйте объект <strong>SWbemDateTime</strong> для преобразования их в обычные даты и время.</span><span class="sxs-lookup"><span data-stu-id="2a1c5-139">Use the <strong>SWbemDateTime</strong> object to convert these to regular dates and times.</span></span> <span data-ttu-id="2a1c5-140">Дополнительные сведения о преобразовании даты и времени см. в разделе <a href="date-and-time-format.md">Формат даты и времени</a> .</span><span class="sxs-lookup"><span data-stu-id="2a1c5-140">See <a href="date-and-time-format.md">Date and Time Format</a> for more information on converting dates and times.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2a1c5-141">... преобразовать DateTime WMI в значение даты и времени .NET?</span><span class="sxs-lookup"><span data-stu-id="2a1c5-141">...convert a WMI datetime to a .NET DateTime value?</span></span></p></td>
<td><p><span data-ttu-id="2a1c5-142">Вручную Проанализируйте строку, а затем помещайте извлеченные значения в объект <a href="/dotnet/api/system.datetime">DateTime</a> .</span><span class="sxs-lookup"><span data-stu-id="2a1c5-142">Manually parse the string, then put the retrieved values into a <a href="/dotnet/api/system.datetime">DateTime</a> object.</span></span></p>
<div class="code">
<span data-codelanguage="PowerShell"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2a1c5-143">PowerShell</span><span class="sxs-lookup"><span data-stu-id="2a1c5-143">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>function WMIDateStringToDateTime( [String] $strWmiDate ) 
{ 
    $strWmiDate.Trim() > $null 
    $iYear   = [Int32]::Parse($strWmiDate.SubString( 0, 4)) 
    $iMonth  = [Int32]::Parse($strWmiDate.SubString( 4, 2)) 
    $iDay    = [Int32]::Parse($strWmiDate.SubString( 6, 2)) 
    $iHour   = [Int32]::Parse($strWmiDate.SubString( 8, 2)) 
    $iMinute = [Int32]::Parse($strWmiDate.SubString(10, 2)) 
    $iSecond = [Int32]::Parse($strWmiDate.SubString(12, 2)) 
<# decimal point is at $strWmiDate.Substring(14, 1) #> 
    $iMicroseconds = [Int32]::Parse($strWmiDate.Substring(15, 6)) 
    $iMilliseconds = $iMicroseconds / 1000 
    $iUtcOffsetMinutes = [Int32]::Parse($strWmiDate.Substring(21, 4)) 
    if ( $iUtcOffsetMinutes -ne 0 ) 
    { 
        $dtkind = [DateTimeKind]::Local 
    } 
    else 
    { 
        $dtkind = [DateTimeKind]::Utc 
    } 
    return New-Object -TypeName DateTime ` 
                      -ArgumentList $iYear, $iMonth, $iDay, ` 
                                    $iHour, $iMinute, $iSecond, ` 
                                    $iMilliseconds, $dtkind 
} </code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="2a1c5-144">См. также</span><span class="sxs-lookup"><span data-stu-id="2a1c5-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2a1c5-145">Задачи WMI для скриптов и приложений</span><span class="sxs-lookup"><span data-stu-id="2a1c5-145">WMI Tasks for Scripts and Applications</span></span>](wmi-tasks-for-scripts-and-applications.md)
</dt> <dt>

[<span data-ttu-id="2a1c5-146">Примеры приложений WMI на C++</span><span class="sxs-lookup"><span data-stu-id="2a1c5-146">WMI C++ Application Examples</span></span>](wmi-c---application-examples.md)
</dt> <dt>

[<span data-ttu-id="2a1c5-147">Формат даты и времени</span><span class="sxs-lookup"><span data-stu-id="2a1c5-147">Date and Time Format</span></span>](date-and-time-format.md)
</dt> <dt>

[<span data-ttu-id="2a1c5-148">Скриптцентер TechNet</span><span class="sxs-lookup"><span data-stu-id="2a1c5-148">TechNet ScriptCenter</span></span>](https://www.microsoft.com/technet/scriptcenter)
</dt> </dl>

 

 



`
