---
description: Запланированные задачи WMI создают и получают сведения о запланированных задачах. Другие примеры см. в разделе TechNet Скриптцентер по адресу https://www.microsoft.com/technet .
ms.assetid: 62151fe8-8880-43f2-b456-628bd9c7cc1c
ms.tgt_platform: multiple
title: 'Задачи WMI: запланированные задачи'
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4051df4348ee47710b5d2d1f5dcc3f59f607d997
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105656591"
---
# <a name="wmi-tasks-scheduled-tasks"></a><span data-ttu-id="2deeb-104">Задачи WMI: запланированные задачи</span><span class="sxs-lookup"><span data-stu-id="2deeb-104">WMI Tasks: Scheduled Tasks</span></span>

<span data-ttu-id="2deeb-105">Запланированные задачи WMI создают и получают сведения о запланированных задачах.</span><span class="sxs-lookup"><span data-stu-id="2deeb-105">WMI scheduled tasks create and get information about scheduled tasks.</span></span> <span data-ttu-id="2deeb-106">Другие примеры см. в разделе TechNet Скриптцентер по адресу [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx) .</span><span class="sxs-lookup"><span data-stu-id="2deeb-106">For other examples, see the TechNet ScriptCenter at [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx).</span></span>

<span data-ttu-id="2deeb-107">Примеры сценариев, приведенные в этом разделе, получают данные только с локального компьютера.</span><span class="sxs-lookup"><span data-stu-id="2deeb-107">The script examples shown in this topic obtain data only from the local computer.</span></span> <span data-ttu-id="2deeb-108">Дополнительные сведения об использовании сценария для получения данных с удаленных компьютеров см. в разделе [Подключение к WMI на удаленном компьютере](connecting-to-wmi-on-a-remote-computer.md).</span><span class="sxs-lookup"><span data-stu-id="2deeb-108">For more information about how to use the script to obtain data from remote computers, see [Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span></span>


<span data-ttu-id="2deeb-109">В следующей процедуре описывается выполнение скрипта.</span><span class="sxs-lookup"><span data-stu-id="2deeb-109">The following procedure describes how to run a script.</span></span>

<span data-ttu-id="2deeb-110">**Запуск сценария**</span><span class="sxs-lookup"><span data-stu-id="2deeb-110">**To run a script**</span></span>

1.  <span data-ttu-id="2deeb-111">Скопируйте код и сохраните его в файле с расширением vbs, например *filename.vbs*.</span><span class="sxs-lookup"><span data-stu-id="2deeb-111">Copy the code and save it in a file with a .vbs extension, such as *filename.vbs*.</span></span> <span data-ttu-id="2deeb-112">Убедитесь, что текстовый редактор не добавляет расширение txt в файл.</span><span class="sxs-lookup"><span data-stu-id="2deeb-112">Ensure that your text editor does not add a .txt extension to the file.</span></span>
2.  <span data-ttu-id="2deeb-113">Откройте окно командной строки и перейдите в каталог, в котором был сохранен файл.</span><span class="sxs-lookup"><span data-stu-id="2deeb-113">Open a command prompt window and navigate to the directory where you saved the file.</span></span>
3.  <span data-ttu-id="2deeb-114">Введите **cscript filename.vbs** в командной строке.</span><span class="sxs-lookup"><span data-stu-id="2deeb-114">Type **cscript filename.vbs** at the command prompt.</span></span>
4.  <span data-ttu-id="2deeb-115">Если доступ к журналу событий невозможен, проверьте, выполняется ли в командной строке с повышенными привилегиями.</span><span class="sxs-lookup"><span data-stu-id="2deeb-115">If you cannot access an event log, check to see if you are running from an Elevated command prompt.</span></span> <span data-ttu-id="2deeb-116">Некоторые журналы событий, например журнал событий безопасности, могут быть защищены с помощью элементов управления доступом пользователей (UAC).</span><span class="sxs-lookup"><span data-stu-id="2deeb-116">Some Event Log, such as the Security Event Log, may be protected by User Access Controls (UAC).</span></span>

> [!Note]  
> <span data-ttu-id="2deeb-117">По умолчанию Cscript отображает выходные данные скрипта в окне командной строки.</span><span class="sxs-lookup"><span data-stu-id="2deeb-117">By default, cscript displays the output of a script in the command prompt window.</span></span> <span data-ttu-id="2deeb-118">Поскольку сценарии WMI могут создавать большие объемы выходных данных, может потребоваться перенаправить выходные данные в файл.</span><span class="sxs-lookup"><span data-stu-id="2deeb-118">Because WMI scripts can produce large amounts of output, you might want to redirect the output to a file.</span></span> <span data-ttu-id="2deeb-119">Введите **cscript filename.vbs > outfile.txt** в командной строке, чтобы перенаправить выходные данные скрипта *filename.vbs* в *outfile.txt*.</span><span class="sxs-lookup"><span data-stu-id="2deeb-119">Type **cscript filename.vbs > outfile.txt** at the command prompt to redirect the output of the *filename.vbs* script to *outfile.txt*.</span></span>

 

<span data-ttu-id="2deeb-120">В следующей таблице перечислены примеры сценариев, которые можно использовать для получения различных типов данных с локального компьютера.</span><span class="sxs-lookup"><span data-stu-id="2deeb-120">The following table lists script examples that can be used to obtain various types of data from the local computer.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2deeb-121">Часто выполняемые действия в новом интерфейсе</span><span class="sxs-lookup"><span data-stu-id="2deeb-121">How do I...</span></span></th>
<th><span data-ttu-id="2deeb-122">Классы или методы WMI</span><span class="sxs-lookup"><span data-stu-id="2deeb-122">WMI classes or methods</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2deeb-123">... создавать запланированные задачи с помощью сценариев?</span><span class="sxs-lookup"><span data-stu-id="2deeb-123">...create scheduled tasks using scripts?</span></span></td>
<td><span data-ttu-id="2deeb-124">Используйте класс <a href="/windows/desktop/CIMWin32Prov/win32-scheduledjob"><strong>Win32_ScheduledJob</strong></a> и метод <a href="/windows/desktop/CIMWin32Prov/create-method-in-class-win32-scheduledjob"><strong>CREATE</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="2deeb-124">Use the <a href="/windows/desktop/CIMWin32Prov/win32-scheduledjob"><strong>Win32_ScheduledJob</strong></a> class and the <a href="/windows/desktop/CIMWin32Prov/create-method-in-class-win32-scheduledjob"><strong>Create</strong></a> method.</span></span> <span data-ttu-id="2deeb-125">Если у вас возникли трудности при выполнении этой задачи в Windows 7 или более поздней версии, см. раздел <strong>Win32_ScheduledJob</strong> примечания. вероятно, ваши параметры препятствуют использованию класса.</span><span class="sxs-lookup"><span data-stu-id="2deeb-125">If you are having difficulty making this task work on Windows 7 or later, see the <strong>Win32_ScheduledJob</strong> Remarks section; likely your settings are preventing you from using the class.</span></span><br/> <span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2deeb-126">VB</span><span class="sxs-lookup"><span data-stu-id="2deeb-126">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;) 
JobID = &quot;Test&quot;
Set objNewJob = objWMIService.Get(&quot;Win32_ScheduledJob&quot;)
errJobCreate = objNewJob.Create _
    (&quot;Notepad.exe&quot;, &quot;********143000.000000-420&quot;, True , 1 OR 4 OR 16, ,True, JobId) 
If errJobCreate = 0 Then
    WScript.Echo &quot;Job created successfully: &quot; & VBNewLine _
        & &quot;Notepad.exe scheduled to run repeately at 14.30 (2:30 P.M.) PST&quot; & VBNewLine _
        & &quot;on Mon, Wed, and Fri.&quot;
Else
    WScript.Echo &quot;Job not created. Error code = &quot; & errJobCreate
End If</code></pre></td>
</tr>
</tbody>
</table>

<p><span data-ttu-id="2deeb-127">В строке &quot; \* \* \* \* \* \* \* \* 143000.000000-420 &quot; (используется в значении параметра <em>StartTime</em> метода <a href="/windows/desktop/CIMWin32Prov/create-method-in-class-win32-scheduledjob"><strong>CREATE</strong></a> ), \* \* \* \* \* \* \* \* &quot; 143000,000000 &quot; указывает, что задача начинается с 14,30 (2:30 P.M.) и &quot; -420 &quot; указывает часовой пояс.</span><span class="sxs-lookup"><span data-stu-id="2deeb-127">In the string &quot;\*\*\*\*\*\*\*\*143000.000000-420&quot; (used in the <em>StartTime</em> parameter value of the <a href="/windows/desktop/CIMWin32Prov/create-method-in-class-win32-scheduledjob"><strong>Create</strong></a> method), &quot;\*\*\*\*\*\*\*\*143000.000000&quot; specifies that the task starts at 14.30 (2:30 P.M.) and &quot;-420&quot; specifies the time zone.</span></span> <span data-ttu-id="2deeb-128">Номер часового пояса — это текущий сдвиг местного перевода времени.</span><span class="sxs-lookup"><span data-stu-id="2deeb-128">The time zone number is the current bias of the local time translation.</span></span> <span data-ttu-id="2deeb-129">Смещение — это разница между временем в формате UTC и местным временем.</span><span class="sxs-lookup"><span data-stu-id="2deeb-129">The bias is the difference between the UTC time and the local time.</span></span> <span data-ttu-id="2deeb-130">Чтобы вычислить смещение для часового пояса, умножьте число часов, в течение которых часовой пояс составляет вперед или выше среднего времени по Гринвичу (GMT) на 60 (Используйте положительное число в часах, если часовой пояс находится впереди GMT и отрицательное число, если часовой пояс находится за GMT).</span><span class="sxs-lookup"><span data-stu-id="2deeb-130">To calculate the bias for your time zone, multiply the number of hours that your time zone is ahead or behind Greenwich Mean Time (GMT) by 60 (use a positive number for the number of hours if your time zone is ahead of GMT and a negative number if your time zone is behind GMT).</span></span> <span data-ttu-id="2deeb-131">Добавьте дополнительные 60 к вычислению, если часовой пояс использует летнее время.</span><span class="sxs-lookup"><span data-stu-id="2deeb-131">Add an additional 60 to your calculation if your time zone is using daylight savings time.</span></span> <span data-ttu-id="2deeb-132">Например, тихоокеанское стандартное часовое пояса составляет восемь часов после GMT, поэтому он равен-420 (-8 \* 60 + 60) при использовании летнего времени и-480 (-8 \* 60), если летнее время не используется.</span><span class="sxs-lookup"><span data-stu-id="2deeb-132">For example, the Pacific Standard Time zone is eight hours behind GMT, therefore the bias is equals to -420 (-8 \* 60 + 60) when daylight savings time is in use and -480 (-8 \* 60) when daylight savings time is not in use.</span></span> <span data-ttu-id="2deeb-133">Можно также определить значение смещения, запросив свойство смещения класса <a href="/windows/desktop/CIMWin32Prov/win32-timezone"><strong>Win32_TimeZone</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="2deeb-133">You can also determine the value of the bias by querying the bias property of the <a href="/windows/desktop/CIMWin32Prov/win32-timezone"><strong>Win32_TimeZone</strong></a> class.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2deeb-134">... возвратить список всех запланированных задач на компьютере?</span><span class="sxs-lookup"><span data-stu-id="2deeb-134">...return a list of all the scheduled tasks on a computer?</span></span></td>
<td><p><span data-ttu-id="2deeb-135">Используйте класс <a href="/windows/desktop/CIMWin32Prov/win32-scheduledjob"><strong>Win32_ScheduledJob</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="2deeb-135">Use the <a href="/windows/desktop/CIMWin32Prov/win32-scheduledjob"><strong>Win32_ScheduledJob</strong></a> class.</span></span> <span data-ttu-id="2deeb-136">Обратите внимание, что этот класс может возвращать только задания, созданные с помощью скрипта или AT.exe.</span><span class="sxs-lookup"><span data-stu-id="2deeb-136">Note that this class can only return jobs that are created using either a script or AT.exe.</span></span> <span data-ttu-id="2deeb-137">Он не может возвращать сведения о заданиях, которые либо созданы или изменены мастером планирования заданий.</span><span class="sxs-lookup"><span data-stu-id="2deeb-137">It cannot return information about jobs that are either created by or modified by the Scheduled Task wizard.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2deeb-138">VB</span><span class="sxs-lookup"><span data-stu-id="2deeb-138">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colScheduledJobs = objWMIService.ExecQuery (&quot;Select * from Win32_ScheduledJob&quot;)
For Each objJob in colScheduledJobs
    Wscript.Echo &quot;Command: &quot; & objJob.Command & VBNewLine _
    & &quot;Days Of Month: &quot; & objJob.DaysOfMonth & VBNewLine _
    & &quot;Days Of Week: &quot; & objJob.DaysOfWeek & VBNewLine _
    & &quot;Description: &quot; & objJob.Description & VBNewLine _
    & &quot;Elapsed Time: &quot; & objJob.ElapsedTime & VBNewLine _
    & &quot;Install Date: &quot; & objJob.InstallDate & VBNewLine _
    & &quot;Interact with Desktop: &quot; & objJob.InteractWithDesktop & VBNewLine _
    & &quot;Job ID: &quot; & objJob.JobId & VBNewLine _
    & &quot;Job Status: &quot; & objJob.JobStatus & VBNewLine _
    & &quot;Name: &quot; & objJob.Name & VBNewLine _
    & &quot;Notify: &quot; & objJob.Notify & VBNewLine _
    & &quot;Owner: &quot; & objJob.Owner & VBNewLine _
    & &quot;Priority: &quot; & objJob.Priority & VBNewLine _
    & &quot;Run Repeatedly: &quot; & objJob.RunRepeatedly & VBNewLine _
    & &quot;Start Time: &quot; & objJob.StartTime & VBNewLine _
    & &quot;Status: &quot; & objJob.Status & VBNewLine _
    & &quot;Time Submitted: &quot; & objJob.TimeSubmitted & VBNewLine _
    & &quot;Until Time: &quot; & objJob.UntilTime
Next</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="2deeb-139">См. также</span><span class="sxs-lookup"><span data-stu-id="2deeb-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2deeb-140">Задачи WMI для скриптов и приложений</span><span class="sxs-lookup"><span data-stu-id="2deeb-140">WMI Tasks for Scripts and Applications</span></span>](wmi-tasks-for-scripts-and-applications.md)
</dt> <dt>

[<span data-ttu-id="2deeb-141">Примеры приложений WMI на C++</span><span class="sxs-lookup"><span data-stu-id="2deeb-141">WMI C++ Application Examples</span></span>](wmi-c---application-examples.md)
</dt> <dt>

[<span data-ttu-id="2deeb-142">Скриптцентер TechNet</span><span class="sxs-lookup"><span data-stu-id="2deeb-142">TechNet ScriptCenter</span></span>](https://www.microsoft.com/technet/scriptcenter)
</dt> </dl>

 

