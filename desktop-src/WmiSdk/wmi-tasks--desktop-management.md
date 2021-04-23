---
description: Задачи WMI для управления настольными системами могут контролировать и получать данные с удаленного рабочего стола или с локального компьютера.
ms.assetid: bb8356bf-de38-4925-a501-6ad47d23ea8f
ms.tgt_platform: multiple
title: 'Задачи WMI: управление рабочими столами '
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 33f027c808a30463f2747d11020f45d1b8d40edf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103898777"
---
# <a name="wmi-tasks-desktop-management"></a><span data-ttu-id="de7f5-103">Задачи WMI: управление рабочими столами </span><span class="sxs-lookup"><span data-stu-id="de7f5-103">WMI Tasks: Desktop Management</span></span>

<span data-ttu-id="de7f5-104">Задачи WMI для управления настольными системами могут контролировать и получать данные с удаленного рабочего стола или с локального компьютера.</span><span class="sxs-lookup"><span data-stu-id="de7f5-104">WMI tasks for desktop management can exert control and obtain data from either a remote desktop or a local computer.</span></span> <span data-ttu-id="de7f5-105">Например, можно определить, требуется ли пароль для экранной заставки на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="de7f5-105">For example, you can determine whether the screensaver on a local computer requires a password.</span></span> <span data-ttu-id="de7f5-106">Инструментарий WMI также дает возможность завершить работу удаленного компьютера.</span><span class="sxs-lookup"><span data-stu-id="de7f5-106">WMI also gives you the ability shut down a remote computer.</span></span> <span data-ttu-id="de7f5-107">Другие примеры см. в разделе TechNet Скриптцентер по адресу [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx) .</span><span class="sxs-lookup"><span data-stu-id="de7f5-107">For other examples, see the TechNet ScriptCenter at [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx).</span></span>

<span data-ttu-id="de7f5-108">Примеры сценариев, приведенные в этом разделе, получают данные только с локального компьютера.</span><span class="sxs-lookup"><span data-stu-id="de7f5-108">The script examples shown in this topic obtain data only from the local computer.</span></span> <span data-ttu-id="de7f5-109">Дополнительные сведения об использовании сценария для получения данных с удаленных компьютеров см. в разделе [Подключение к WMI на удаленном компьютере](connecting-to-wmi-on-a-remote-computer.md).</span><span class="sxs-lookup"><span data-stu-id="de7f5-109">For more information about how to use the script to obtain data from remote computers, see [Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span></span>


<span data-ttu-id="de7f5-110">В следующей процедуре описывается выполнение скрипта.</span><span class="sxs-lookup"><span data-stu-id="de7f5-110">The following procedure describes how to run a script.</span></span>

<span data-ttu-id="de7f5-111">**Запуск сценария**</span><span class="sxs-lookup"><span data-stu-id="de7f5-111">**To run a script**</span></span>

1.  <span data-ttu-id="de7f5-112">Скопируйте код и сохраните его в файле с расширением vbs, например *filename.vbs*.</span><span class="sxs-lookup"><span data-stu-id="de7f5-112">Copy the code and save it in a file with a .vbs extension, such as *filename.vbs*.</span></span> <span data-ttu-id="de7f5-113">Убедитесь, что текстовый редактор не добавляет расширение txt в файл.</span><span class="sxs-lookup"><span data-stu-id="de7f5-113">Ensure that your text editor does not add a .txt extension to the file.</span></span>
2.  <span data-ttu-id="de7f5-114">Откройте окно командной строки и перейдите в каталог, в котором был сохранен файл.</span><span class="sxs-lookup"><span data-stu-id="de7f5-114">Open a command prompt window and navigate to the directory where you saved the file.</span></span>
3.  <span data-ttu-id="de7f5-115">Введите **cscript filename.vbs** в командной строке.</span><span class="sxs-lookup"><span data-stu-id="de7f5-115">Type **cscript filename.vbs** at the command prompt.</span></span>
4.  <span data-ttu-id="de7f5-116">Если доступ к журналу событий невозможен, проверьте, выполняется ли в командной строке с повышенными привилегиями.</span><span class="sxs-lookup"><span data-stu-id="de7f5-116">If you cannot access an event log, check to see if you are running from an Elevated command prompt.</span></span> <span data-ttu-id="de7f5-117">Некоторые журналы событий, например журнал событий безопасности, могут быть защищены с помощью элементов управления доступом пользователей (UAC).</span><span class="sxs-lookup"><span data-stu-id="de7f5-117">Some Event Log, such as the Security Event Log, may be protected by User Access Controls (UAC).</span></span>

> [!Note]  
> <span data-ttu-id="de7f5-118">По умолчанию Cscript отображает выходные данные скрипта в окне командной строки.</span><span class="sxs-lookup"><span data-stu-id="de7f5-118">By default, cscript displays the output of a script in the command prompt window.</span></span> <span data-ttu-id="de7f5-119">Поскольку сценарии WMI могут создавать большие объемы выходных данных, может потребоваться перенаправить выходные данные в файл.</span><span class="sxs-lookup"><span data-stu-id="de7f5-119">Because WMI scripts can produce large amounts of output, you might want to redirect the output to a file.</span></span> <span data-ttu-id="de7f5-120">Введите **cscript filename.vbs > outfile.txt** в командной строке, чтобы перенаправить выходные данные скрипта *filename.vbs* в *outfile.txt*.</span><span class="sxs-lookup"><span data-stu-id="de7f5-120">Type **cscript filename.vbs > outfile.txt** at the command prompt to redirect the output of the *filename.vbs* script to *outfile.txt*.</span></span>

 

<span data-ttu-id="de7f5-121">В следующей таблице перечислены примеры сценариев, которые можно использовать для получения различных типов данных с локального компьютера.</span><span class="sxs-lookup"><span data-stu-id="de7f5-121">The following table lists script examples that can be used to obtain various types of data from the local computer.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="de7f5-122">Часто выполняемые действия в новом интерфейсе</span><span class="sxs-lookup"><span data-stu-id="de7f5-122">How do I...</span></span></th>
<th><span data-ttu-id="de7f5-123">Классы или методы WMI</span><span class="sxs-lookup"><span data-stu-id="de7f5-123">WMI classes or methods</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="de7f5-124">... как определить, загружен ли удаленный компьютер в защищенном режиме с состоянием сети?</span><span class="sxs-lookup"><span data-stu-id="de7f5-124">...determine if a remote computer has booted up in the Safe Mode with Networking state?</span></span></td>
<td><span data-ttu-id="de7f5-125">Используйте класс <a href="/windows/desktop/CIMWin32Prov/win32-computersystem"><strong>Win32_ComputerSystem</strong></a> и проверьте значение свойства <strong>примарйовнернаме</strong> .</span><span class="sxs-lookup"><span data-stu-id="de7f5-125">Use the <a href="/windows/desktop/CIMWin32Prov/win32-computersystem"><strong>Win32_ComputerSystem</strong></a> class and check the value of the <strong>PrimaryOwnerName</strong> property.</span></span><br/> <span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="de7f5-126">VB</span><span class="sxs-lookup"><span data-stu-id="de7f5-126">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colSettings = objWMIService.ExecQuery (&quot;Select * from Win32_ComputerSystem&quot;)
For Each objComputer in colSettings 
    Wscript.Echo &quot;System Name: &quot; & objComputer.Name
    Wscript.Echo &quot;Registered owner: &quot; & objComputer.PrimaryOwnerName
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
<th><span data-ttu-id="de7f5-127">PowerShell</span><span class="sxs-lookup"><span data-stu-id="de7f5-127">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$colSettings = Get-WmiObject -Class Win32_ComputerSystem
foreach ($objComputer in $colSettings)
{
    &quot;System Name: &quot; + $objComputer.Name
    &quot;Registered owner: &quot; + $objComputer.PrimaryOwnerName
}</code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="de7f5-128">... как определить, требуется ли пароль для заставки компьютера?</span><span class="sxs-lookup"><span data-stu-id="de7f5-128">...determine if a computer screensaver requires a password?</span></span></td>
<td><p><span data-ttu-id="de7f5-129">Используйте класс <a href="/windows/desktop/CIMWin32Prov/win32-desktop"><strong>Win32_Desktop</strong></a> и проверьте значение свойства <strong>скринсаверсекуре</strong> .</span><span class="sxs-lookup"><span data-stu-id="de7f5-129">Use the <a href="/windows/desktop/CIMWin32Prov/win32-desktop"><strong>Win32_Desktop</strong></a> class and check the value of the <strong>ScreenSaverSecure</strong> property.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="de7f5-130">VB</span><span class="sxs-lookup"><span data-stu-id="de7f5-130">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colItems = objWMIService.ExecQuery(&quot;Select * from Win32_Desktop&quot;)
For Each objItem in colItems
    Wscript.Echo &quot;Screen Saver Secure: &quot; & objItem.ScreenSaverSecure
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
<th><span data-ttu-id="de7f5-131">PowerShell</span><span class="sxs-lookup"><span data-stu-id="de7f5-131">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$Computer = &quot;.&quot;
$Desktops = Get-WMIObject -class Win32_Desktop -ComputerName $computer
&quot;{0} desktops found as follows&quot; -f $desktops.count
foreach ($desktop in $desktops) {
     &quot;Desktop      : {0}&quot;  -f $Desktop.Name
     &quot;Screen Saver : {0}&quot;  -f $desktop.ScreensaverExecutable
     &quot;Secure       : {0} &quot; -f $desktop.ScreenSaverSecure
     &quot;&quot;
}</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="de7f5-132">... Убедитесь, что экран компьютера установлен на 800 пикселей на 600 пикселей?</span><span class="sxs-lookup"><span data-stu-id="de7f5-132">...verify that a computer screen has been set for 800 pixels by 600 pixels?</span></span></td>
<td><p><span data-ttu-id="de7f5-133">Используйте класс <a href="/windows/desktop/CIMWin32Prov/win32-desktopmonitor"><strong>Win32_DesktopMonitor</strong></a> и проверьте значения свойств <strong>скринхеигхт</strong> и <strong>скринвидс</strong>.</span><span class="sxs-lookup"><span data-stu-id="de7f5-133">Use the <a href="/windows/desktop/CIMWin32Prov/win32-desktopmonitor"><strong>Win32_DesktopMonitor</strong></a> class and check the values of the properties <strong>ScreenHeight</strong> and <strong>ScreenWidth</strong>.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="de7f5-134">VB</span><span class="sxs-lookup"><span data-stu-id="de7f5-134">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(_
    &quot;winmgmts:\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colItems = objWMIService.ExecQuery(&quot;Select * from Win32_DesktopMonitor&quot;)
For Each objItem in colItems
    Wscript.Echo &quot;Screen Height: &quot; & objItem.ScreenHeight
    Wscript.Echo &quot;Screen Width: &quot; & objItem.ScreenWidth
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
<th><span data-ttu-id="de7f5-135">PowerShell</span><span class="sxs-lookup"><span data-stu-id="de7f5-135">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code><# Get desktop information #>
$computer = &quot;.&quot;
$desktops = Get-WmiObject -Class Win32_DesktopMonitor
$hostname = hostname

<span data-ttu-id="de7f5-136">< # Показать сведения о рабочем столе # > имеются &quot; {0} следующие настольные системы {1} : &quot; -f $desktops. Число, $hostname &quot; &quot; $i = 1 # число настольных систем в этой системе</span><span class="sxs-lookup"><span data-stu-id="de7f5-136"><# Display desktop details #> &quot;There are {0} Desktops on {1} as follows:&quot; -f $desktops.Count, $hostname &quot;&quot; $i=1 # count of desktops on this system</span></span>

<span data-ttu-id="de7f5-137">foreach ($Desktop в $desktops) { &quot; Desktop {0} : {1} &quot; -f $i + +, $Desktop. &quot; Высота экрана заголовка: {0} &quot; -f $Desktop. &quot;Ширина экрана скринхеигхт: {0} &quot; -f $Desktop. Скринвидс &quot; &quot; }</code></span><span class="sxs-lookup"><span data-stu-id="de7f5-137">foreach ($desktop in $desktops) { &quot;Desktop {0}: {1}&quot; -f  $i++, $Desktop.Caption &quot;Screen Height : {0}&quot; -f $desktop.ScreenHeight &quot;Screen Width  : {0}&quot; -f $desktop.ScreenWidth &quot;&quot; }</code></span></span></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="de7f5-138">... определить, как долго работает компьютер?</span><span class="sxs-lookup"><span data-stu-id="de7f5-138">...determine how long a computer has been running?</span></span></td>
<td><p><span data-ttu-id="de7f5-139">Используйте класс <a href="/windows/desktop/CIMWin32Prov/win32-operatingsystem"><strong>Win32_OperatingSystem</strong></a> и свойство <strong>LastBootUpTime</strong> .</span><span class="sxs-lookup"><span data-stu-id="de7f5-139">Use the <a href="/windows/desktop/CIMWin32Prov/win32-operatingsystem"><strong>Win32_OperatingSystem</strong></a> class and the <strong>LastBootUpTime</strong> property.</span></span> <span data-ttu-id="de7f5-140">Вычтите это значение из текущего времени, чтобы получить время непрерывной работы системы.</span><span class="sxs-lookup"><span data-stu-id="de7f5-140">Subtract that value from the current time to get the system uptime.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="de7f5-141">VB</span><span class="sxs-lookup"><span data-stu-id="de7f5-141">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colOperatingSystems = objWMIService.ExecQuery (&quot;Select * from Win32_OperatingSystem&quot;)
 
For Each objOS in colOperatingSystems
    dtmBootup = objOS.LastBootUpTime
    dtmLastBootUpTime = WMIDateStringToDate(dtmBootup)
    dtmSystemUptime = DateDiff(&quot;h&quot;, dtmLastBootUpTime, Now)
    Wscript.Echo dtmSystemUptime 
Next
 
Function WMIDateStringToDate(dtmBootup)
    WMIDateStringToDate =  CDate(Mid(dtmBootup, 5, 2) & &quot;/&quot; & _
        Mid(dtmBootup, 7, 2) & &quot;/&quot; & Left(dtmBootup, 4) & &quot; &quot; & Mid (dtmBootup, 9, 2) & &quot;:&quot; & _
        Mid(dtmBootup, 11, 2) & &quot;:&quot; & Mid(dtmBootup, 13, 2))
End Function</code></pre></td>
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
<th><span data-ttu-id="de7f5-142">PowerShell</span><span class="sxs-lookup"><span data-stu-id="de7f5-142">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>function WMIDateStringToDate($Bootup) {
[System.Management.ManagementDateTimeconverter]::ToDateTime($Bootup)
}

<# Main script #>
$Computer = &quot;.&quot; # adjust as needed
$computers = Get-WMIObject -class Win32_OperatingSystem -computer $computer

foreach ($system in $computers) {
    $Bootup = $system.LastBootUpTime
    $LastBootUpTime = WMIDateStringToDate($Bootup)
    $now = Get-Date
 $Uptime = $now-$lastBootUpTime
    &quot;System Up for: {0}&quot; -f $UpTime
} </code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="de7f5-143">... перезагрузить или завершить работу удаленного компьютера?</span><span class="sxs-lookup"><span data-stu-id="de7f5-143">...reboot or shut down a remote computer?</span></span></td>
<td><p><span data-ttu-id="de7f5-144">Используйте класс <a href="/windows/desktop/CIMWin32Prov/win32-operatingsystem"><strong>Win32_OperatingSystem</strong></a> и метод <a href="/windows/desktop/CIMWin32Prov/win32shutdown-method-in-class-win32-operatingsystem"><strong>Win32Shutdown</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="de7f5-144">Use the <a href="/windows/desktop/CIMWin32Prov/win32-operatingsystem"><strong>Win32_OperatingSystem</strong></a> class and the <a href="/windows/desktop/CIMWin32Prov/win32shutdown-method-in-class-win32-operatingsystem"><strong>Win32Shutdown</strong></a> method.</span></span> <span data-ttu-id="de7f5-145">При подключении к WMI необходимо включить привилегию <a href="privilege-constants.md">ремотешутдовн</a> .</span><span class="sxs-lookup"><span data-stu-id="de7f5-145">You must include the <a href="privilege-constants.md">RemoteShutdown</a> privilege when connecting to WMI.</span></span> <span data-ttu-id="de7f5-146">Дополнительные сведения см. в статье <a href="executing-privileged-operations-using-vbscript.md">выполнение привилегированных операций с помощью VBScript</a>.</span><span class="sxs-lookup"><span data-stu-id="de7f5-146">For more information, see <a href="executing-privileged-operations-using-vbscript.md">Executing Privileged Operations Using VBScript</a>.</span></span> <span data-ttu-id="de7f5-147">В отличие от метода <a href="/windows/desktop/CIMWin32Prov/shutdown-method-in-class-win32-operatingsystem"><strong>Shutdown</strong></a> в <strong>Win32_OperatingSystem</strong>, метод <strong>Win32Shutdown</strong> позволяет устанавливать флаги для управления поведением при завершении работы.</span><span class="sxs-lookup"><span data-stu-id="de7f5-147">Unlike the <a href="/windows/desktop/CIMWin32Prov/shutdown-method-in-class-win32-operatingsystem"><strong>Shutdown</strong></a> method on <strong>Win32_OperatingSystem</strong>, the <strong>Win32Shutdown</strong> method allows you to set flags to control the shutdown behavior.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="de7f5-148">VB</span><span class="sxs-lookup"><span data-stu-id="de7f5-148">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;atl-dc-01&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate,(Shutdown)}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colOperatingSystems = objWMIService.ExecQuery (&quot;Select * from Win32_OperatingSystem&quot;)
For Each objOperatingSystem in colOperatingSystems
    ObjOperatingSystem.Shutdown(1)
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
<th><span data-ttu-id="de7f5-149">PowerShell</span><span class="sxs-lookup"><span data-stu-id="de7f5-149">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;atl-dc-01&quot;
$colOperatingSystem = Get-WmiObject -Class Win32_OperatingSystem -ComputerName $strComputer -Namespace &quot;wmi\cimv2&quot;
foreach ($objOperatingSystem in $colOperatingSystem)
{
    [void]$objOperatingSystem.Shutdown()
}</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="de7f5-150">... Определите, какие приложения автоматически запускаются при каждом запуске Windows?</span><span class="sxs-lookup"><span data-stu-id="de7f5-150">...determine what applications automatically run each time I start Windows?</span></span></td>
<td><p><span data-ttu-id="de7f5-151">Используйте класс <a href="/windows/desktop/CIMWin32Prov/win32-startupcommand"><strong>Win32_StartupCommand</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="de7f5-151">Use the <a href="/windows/desktop/CIMWin32Prov/win32-startupcommand"><strong>Win32_StartupCommand</strong></a> class.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="de7f5-152">VB</span><span class="sxs-lookup"><span data-stu-id="de7f5-152">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; _
    & &quot;{impersonationLevel=impersonate}!\\&quot; _
    & strComputer & &quot;\root\cimv2&quot;)
Set colStartupCommands = objWMIService.ExecQuery _
    (&quot;Select * from Win32_StartupCommand&quot;)
For Each objStartupCommand in colStartupCommands
    Wscript.Echo &quot;Command: &quot; & objStartupCommand.Command & VBNewLine _
    & &quot;Description: &quot; & objStartupCommand.Description & VBNewLine _
    & &quot;Location: &quot; & objStartupCommand.Location & VBNewLine _
    & &quot;Name: &quot; & objStartupCommand.Name & VBNewLine _
    & &quot;SettingID: &quot; & objStartupCommand.SettingID & VBNewLine _
    & &quot;User: &quot; & objStartupCommand.User
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
<th><span data-ttu-id="de7f5-153">PowerShell</span><span class="sxs-lookup"><span data-stu-id="de7f5-153">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$strComputer = &quot;.&quot;
$colItems = Get-WmiObject -Class Win32_StartupCommand -ComputerName $strComputer
foreach ($objStartupCommand in $colItems) 
{ 
    &quot;Command: &quot; + $objStartupCommand.Command
    &quot;Description: &quot; + $objStartupCommand.Description 
    &quot;Location: &quot; + $objStartupCommand.Location 
    &quot;Name: &quot; + $objStartupCommand.Name 
    &quot;SettingID: &quot; + $objStartupCommand.SettingID 
    &quot;User: &quot; + $objStartupCommand.User
}</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="de7f5-154">См. также</span><span class="sxs-lookup"><span data-stu-id="de7f5-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="de7f5-155">Задачи WMI для скриптов и приложений</span><span class="sxs-lookup"><span data-stu-id="de7f5-155">WMI Tasks for Scripts and Applications</span></span>](wmi-tasks-for-scripts-and-applications.md)
</dt> <dt>

[<span data-ttu-id="de7f5-156">Примеры приложений WMI на C++</span><span class="sxs-lookup"><span data-stu-id="de7f5-156">WMI C++ Application Examples</span></span>](wmi-c---application-examples.md)
</dt> <dt>

[<span data-ttu-id="de7f5-157">Скриптцентер TechNet</span><span class="sxs-lookup"><span data-stu-id="de7f5-157">TechNet ScriptCenter</span></span>](https://www.microsoft.com/technet/scriptcenter)
</dt> </dl>

