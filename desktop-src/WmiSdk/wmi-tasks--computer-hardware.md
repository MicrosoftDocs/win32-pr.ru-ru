---
description: Задачи WMI для оборудования компьютера получают сведения о присутствии, состоянии или свойствах компонентов оборудования.
ms.assetid: eb4c2c38-4853-4486-b889-93a843d88edb
ms.tgt_platform: multiple
title: 'Задачи WMI: оборудование компьютера'
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d5589c634a5a7bf11b95bc2d90ebeab038eb8af0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711729"
---
# <a name="wmi-tasks-computer-hardware"></a><span data-ttu-id="5eb77-103">Задачи WMI: оборудование компьютера</span><span class="sxs-lookup"><span data-stu-id="5eb77-103">WMI Tasks: Computer Hardware</span></span>

<span data-ttu-id="5eb77-104">Задачи WMI для оборудования компьютера получают сведения о присутствии, состоянии или свойствах компонентов оборудования.</span><span class="sxs-lookup"><span data-stu-id="5eb77-104">WMI tasks for computer hardware obtain information about the presence, state, or properties of hardware components.</span></span> <span data-ttu-id="5eb77-105">Например, можно определить, является ли компьютер настольным или ноутбуком.</span><span class="sxs-lookup"><span data-stu-id="5eb77-105">For example, you can determine whether a computer is a desktop or laptop.</span></span> <span data-ttu-id="5eb77-106">Другие примеры см. в разделе TechNet Скриптцентер по адресу [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx) .</span><span class="sxs-lookup"><span data-stu-id="5eb77-106">For other examples, see the TechNet ScriptCenter at [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx).</span></span>

<span data-ttu-id="5eb77-107">Примеры сценариев, приведенные в этом разделе, получают данные только с локального компьютера.</span><span class="sxs-lookup"><span data-stu-id="5eb77-107">The script examples shown in this topic obtain data only from the local computer.</span></span> <span data-ttu-id="5eb77-108">Дополнительные сведения об использовании сценария для получения данных с удаленных компьютеров см. в разделе [Подключение к WMI на удаленном компьютере](connecting-to-wmi-on-a-remote-computer.md).</span><span class="sxs-lookup"><span data-stu-id="5eb77-108">For more information about how to use the script to obtain data from remote computers, see [Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span></span>

## <a name="to-run-a-script"></a><span data-ttu-id="5eb77-109">Запуск сценария</span><span class="sxs-lookup"><span data-stu-id="5eb77-109">To run a script</span></span>

<span data-ttu-id="5eb77-110">В следующей процедуре описывается выполнение скрипта.</span><span class="sxs-lookup"><span data-stu-id="5eb77-110">The following procedure describes how to run a script.</span></span>

1.  <span data-ttu-id="5eb77-111">Скопируйте код и сохраните его в файле с расширением vbs, например *filename.vbs*.</span><span class="sxs-lookup"><span data-stu-id="5eb77-111">Copy the code and save it in a file with a .vbs extension, such as *filename.vbs*.</span></span> <span data-ttu-id="5eb77-112">Убедитесь, что текстовый редактор не добавляет расширение txt в файл.</span><span class="sxs-lookup"><span data-stu-id="5eb77-112">Ensure that your text editor does not add a .txt extension to the file.</span></span>
2.  <span data-ttu-id="5eb77-113">Откройте окно командной строки и перейдите в каталог, в котором был сохранен файл.</span><span class="sxs-lookup"><span data-stu-id="5eb77-113">Open a command prompt window and navigate to the directory where you saved the file.</span></span>
3.  <span data-ttu-id="5eb77-114">Введите **cscript filename.vbs** в командной строке.</span><span class="sxs-lookup"><span data-stu-id="5eb77-114">Type **cscript filename.vbs** at the command prompt.</span></span>
4.  <span data-ttu-id="5eb77-115">Если доступ к журналу событий невозможен, проверьте, выполняется ли в командной строке с повышенными привилегиями.</span><span class="sxs-lookup"><span data-stu-id="5eb77-115">If you cannot access an event log, check to see if you are running from an Elevated command prompt.</span></span> <span data-ttu-id="5eb77-116">Некоторые журналы событий, например журнал событий безопасности, могут быть защищены с помощью элементов управления доступом пользователей (UAC).</span><span class="sxs-lookup"><span data-stu-id="5eb77-116">Some Event Log, such as the Security Event Log, may be protected by User Access Controls (UAC).</span></span>

> [!Note]  
> <span data-ttu-id="5eb77-117">По умолчанию Cscript отображает выходные данные скрипта в окне командной строки.</span><span class="sxs-lookup"><span data-stu-id="5eb77-117">By default, cscript displays the output of a script in the command prompt window.</span></span> <span data-ttu-id="5eb77-118">Поскольку сценарии WMI могут создавать большие объемы выходных данных, может потребоваться перенаправить выходные данные в файл.</span><span class="sxs-lookup"><span data-stu-id="5eb77-118">Because WMI scripts can produce large amounts of output, you might want to redirect the output to a file.</span></span> <span data-ttu-id="5eb77-119">Введите **cscript filename.vbs > outfile.txt** в командной строке, чтобы перенаправить выходные данные скрипта *filename.vbs* в *outfile.txt*.</span><span class="sxs-lookup"><span data-stu-id="5eb77-119">Type **cscript filename.vbs > outfile.txt** at the command prompt to redirect the output of the *filename.vbs* script to *outfile.txt*.</span></span>

 

<span data-ttu-id="5eb77-120">В следующей таблице перечислены примеры сценариев, которые можно использовать для получения различных типов данных с локального компьютера.</span><span class="sxs-lookup"><span data-stu-id="5eb77-120">The following table lists script examples that can be used to obtain various types of data from the local computer.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5eb77-121">Часто выполняемые действия в новом интерфейсе</span><span class="sxs-lookup"><span data-stu-id="5eb77-121">How do I...</span></span></th>
<th><span data-ttu-id="5eb77-122">Классы или методы WMI</span><span class="sxs-lookup"><span data-stu-id="5eb77-122">WMI classes or methods</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5eb77-123">... определить объем свободной памяти компьютера?</span><span class="sxs-lookup"><span data-stu-id="5eb77-123">...determine how much free memory a computer has?</span></span></td>
<td><span data-ttu-id="5eb77-124">Используйте класс <a href="/windows/desktop/CIMWin32Prov/win32-operatingsystem"><strong>Win32_OperatingSystem</strong></a> и свойство <strong>фрифисикалмемори</strong> .</span><span class="sxs-lookup"><span data-stu-id="5eb77-124">Use the class <a href="/windows/desktop/CIMWin32Prov/win32-operatingsystem"><strong>Win32_OperatingSystem</strong></a> and the <strong>FreePhysicalMemory</strong> property.</span></span><br/> <span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5eb77-125">VB</span><span class="sxs-lookup"><span data-stu-id="5eb77-125">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colSettings = objWMIService.ExecQuery(&quot;Select * from Win32_OperatingSystem&quot;)
For Each objOperatingSystem in colSettings 
    Wscript.Echo &quot;Available Physical Memory: &quot; & objOperatingSystem.FreePhysicalMemory
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
<th><span data-ttu-id="5eb77-126">PowerShell</span><span class="sxs-lookup"><span data-stu-id="5eb77-126">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$mem = Get-WmiObject -Class Win32_OperatingSystem
&quot;System : {0}&quot; -f $mem.csname
&quot;Free Memory: {0}&quot; -f $mem.FreePhysicalMemory</code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="5eb77-127">... как определить, есть ли у компьютера DVD-дисковод?</span><span class="sxs-lookup"><span data-stu-id="5eb77-127">...determine whether a computer has a DVD drive?</span></span></td>
<td><p><span data-ttu-id="5eb77-128">Используйте класс <a href="/windows/desktop/CIMWin32Prov/win32-cdromdrive"><strong>Win32_CDROMDrive</strong></a> и проверьте DVD-диск акронима в свойстве <strong>Name</strong> или <strong>DeviceID</strong> .</span><span class="sxs-lookup"><span data-stu-id="5eb77-128">Use the <a href="/windows/desktop/CIMWin32Prov/win32-cdromdrive"><strong>Win32_CDROMDrive</strong></a> class and check for the acronym DVD in the <strong>Name</strong> or <strong>DeviceID</strong> property.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5eb77-129">VB</span><span class="sxs-lookup"><span data-stu-id="5eb77-129">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject( &quot;winmgmts:\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colItems = objWMIService.ExecQuery(&quot;Select * from Win32_CDROMDrive&quot;)
For Each objItem in colItems
    Wscript.Echo &quot;Device ID: &quot; & objItem.DeviceID
    Wscript.Echo &quot;Description: &quot; & objItem.Description
    Wscript.Echo &quot;Name: &quot; & objItem.Name 
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
<th><span data-ttu-id="5eb77-130">PowerShell</span><span class="sxs-lookup"><span data-stu-id="5eb77-130">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$drives = Get-WmiObject -Class Win32_CDROMDrives
$drives | Format-Table DeviceID, Description, Name -autosize</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5eb77-131">... определить, какой объем ОЗУ установлен на компьютере?</span><span class="sxs-lookup"><span data-stu-id="5eb77-131">...determine how much RAM is installed in a computer?</span></span></td>
<td><p><span data-ttu-id="5eb77-132">Используйте класс <a href="/windows/desktop/CIMWin32Prov/win32-computersystem"><strong>Win32_ComputerSystem</strong></a> и проверьте значение свойства <strong>тоталфисикалмемори</strong> .</span><span class="sxs-lookup"><span data-stu-id="5eb77-132">Use the <a href="/windows/desktop/CIMWin32Prov/win32-computersystem"><strong>Win32_ComputerSystem</strong></a> class and check the value of the <strong>TotalPhysicalMemory</strong> property.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5eb77-133">VB</span><span class="sxs-lookup"><span data-stu-id="5eb77-133">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colSettings = objWMIService.ExecQuery(&quot;Select * from Win32_ComputerSystem&quot;)
For Each objComputer in colSettings 
    Wscript.Echo &quot;System Name: &quot; & objComputer.Name
    Wscript.Echo &quot;Total Physical Memory: &quot; & objComputer.TotalPhysicalMemory
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
<th><span data-ttu-id="5eb77-134">PowerShell</span><span class="sxs-lookup"><span data-stu-id="5eb77-134">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$mem = Get-WmiObject -Class Win32_ComputerSystem</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5eb77-135">... определить, имеет ли компьютер несколько процессоров?</span><span class="sxs-lookup"><span data-stu-id="5eb77-135">...determine if a computer has more than one processor?</span></span></td>
<td><p><span data-ttu-id="5eb77-136">Используйте класс <a href="/windows/desktop/CIMWin32Prov/win32-computersystem"><strong>Win32_ComputerSystem</strong></a> и свойство <strong>NumberOfProcessors</strong>.</span><span class="sxs-lookup"><span data-stu-id="5eb77-136">Use the <a href="/windows/desktop/CIMWin32Prov/win32-computersystem"><strong>Win32_ComputerSystem</strong></a> class and the property <strong>NumberOfProcessors</strong>.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5eb77-137">VB</span><span class="sxs-lookup"><span data-stu-id="5eb77-137">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colSettings = objWMIService.ExecQuery(&quot;Select * from Win32_ComputerSystem&quot;)
For Each objComputer in colSettings 
    Wscript.Echo &quot;System Name: &quot; & objComputer.Name
    Wscript.Echo &quot;Number of Processors: &quot; & objComputer.NumberOfProcessors
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
<th><span data-ttu-id="5eb77-138">PowerShell</span><span class="sxs-lookup"><span data-stu-id="5eb77-138">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>&quot;System Name : {0}&quot; -f $system.Name
&quot;Number of Processors: {0}&quot; -f $system.NumberOfProcessors</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5eb77-139">... Определение наличия гнезда PCMCIA на компьютере?</span><span class="sxs-lookup"><span data-stu-id="5eb77-139">...determine whether a computer has a PCMCIA slot?</span></span></td>
<td><p><span data-ttu-id="5eb77-140">Используйте класс <a href="/windows/desktop/CIMWin32Prov/win32-pcmciacontroller"><strong>Win32_PCMCIAController</strong></a> и проверьте значение свойства <strong>Count</strong> .</span><span class="sxs-lookup"><span data-stu-id="5eb77-140">Use the <a href="/windows/desktop/CIMWin32Prov/win32-pcmciacontroller"><strong>Win32_PCMCIAController</strong></a> class and check the value of the <strong>Count</strong> property.</span></span> <span data-ttu-id="5eb77-141">Если параметр <strong>Count</strong> равен 0, то компьютер не имеет гнезд PCMCIA.</span><span class="sxs-lookup"><span data-stu-id="5eb77-141">If <strong>Count</strong> is 0, then the computer has no PCMCIA slots.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5eb77-142">VB</span><span class="sxs-lookup"><span data-stu-id="5eb77-142">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colItems = objWMIService.ExecQuery(&quot;Select * from Win32_PCMCIAController&quot;)
Wscript.Echo &quot;Number of PCMCIA slots: &quot; & colItems.Count</code></pre></td>
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
<th><span data-ttu-id="5eb77-143">PowerShell</span><span class="sxs-lookup"><span data-stu-id="5eb77-143">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$Pcmcia = Get-WmiObject -Class Win32_PCMCIAController

if (!$pcmcia.count) {
    &quot;Number of PCMCIA Slots: {0}&quot; -f 1
}else {
    &quot;Number of PCMCIA Slots: {0}&quot; -f $pcmcia.count
}</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5eb77-144">... выявление неработающих устройств (отмеченных значком восклицательного знака в <strong>Диспетчер устройств</strong>)?</span><span class="sxs-lookup"><span data-stu-id="5eb77-144">...identify devices that are not working (those marked with an exclamation point icon in <strong>Device Manager</strong>)?</span></span></td>
<td><p><span data-ttu-id="5eb77-145">Используйте класс <a href="/windows/desktop/CIMWin32Prov/win32-pnpentity"><strong>Win32_PnPEntity</strong></a> и используйте следующее предложение в <a href="querying-with-wql.md">WQL</a> -запросе.</span><span class="sxs-lookup"><span data-stu-id="5eb77-145">Use the <a href="/windows/desktop/CIMWin32Prov/win32-pnpentity"><strong>Win32_PnPEntity</strong></a> class and use the following clause in your <a href="querying-with-wql.md">WQL</a> query.</span></span> <span data-ttu-id="5eb77-146"><strong>Где конфигманажерерроркоде <> 0</strong> Обратите внимание, что этот код может не обнаруживать USB-устройства с отсутствующими драйверами.</span><span class="sxs-lookup"><span data-stu-id="5eb77-146"><strong>WHERE ConfigManagerErrorCode <> 0</strong> Note that this code may not detect USB devices that are missing drivers.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5eb77-147">VB</span><span class="sxs-lookup"><span data-stu-id="5eb77-147">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colItems = objWMIService.ExecQuery(&quot;Select * from Win32_PnPEntity WHERE ConfigManagerErrorCode <> 0&quot;)
For Each objItem in colItems
    Wscript.Echo &quot;Class GUID: &quot; & objItem.ClassGuid
    Wscript.Echo &quot;Description: &quot; & objItem.Description
    Wscript.Echo &quot;Device ID: &quot; & objItem.DeviceID
    Wscript.Echo &quot;Manufacturer: &quot; & objItem.Manufacturer
    Wscript.Echo &quot;Name: &quot; & objItem.Name
    Wscript.Echo &quot;PNP Device ID: &quot; & objItem.PNPDeviceID
    Wscript.Echo &quot;Service: &quot; & objItem.Service
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
<th><span data-ttu-id="5eb77-148">PowerShell</span><span class="sxs-lookup"><span data-stu-id="5eb77-148">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$baddevices = Get-WmiObject Win32_PNPEntity | where {$_.ConfigManagerErrorcode -ne 0}
&quot; Total Bad devices: {0}&quot; -f $baddevices.count
foreach ($device in $baddevices) {
    &quot;Name : {0}&quot; -f $device.name
    &quot;Class Guid : {0}&quot; -f $device.Classguid
    &quot;Description : {0}&quot; -f $device.Description
    &quot;Device ID : {0}&quot; -f $device.deviceid
    &quot;Manufacturer : {0}&quot; -f $device.manufactuer
    &quot;PNP Devcice Id : {0}&quot; -f $device.PNPDeviceID
    &quot;Service Name : {0}&quot; -f $device.service
    &quot;&quot;
}</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5eb77-149">... определить свойства мыши, используемой на компьютере?</span><span class="sxs-lookup"><span data-stu-id="5eb77-149">...determine the properties of the mouse used on computer?</span></span></td>
<td><p><span data-ttu-id="5eb77-150">Используйте класс <a href="/windows/desktop/CIMWin32Prov/win32-pointingdevice"><strong>Win32_PointingDevice</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="5eb77-150">Use the <a href="/windows/desktop/CIMWin32Prov/win32-pointingdevice"><strong>Win32_PointingDevice</strong></a> class.</span></span> <span data-ttu-id="5eb77-151">Это возвращает свойства всех указывающих устройств, а не просто устройств мыши.</span><span class="sxs-lookup"><span data-stu-id="5eb77-151">This returns the properties of all pointing devices, not just mouse devices.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5eb77-152">VB</span><span class="sxs-lookup"><span data-stu-id="5eb77-152">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colItems = objWMIService.ExecQuery(&quot;Select * from Win32_PointingDevice&quot;)
For Each objItem in colItems
    Wscript.Echo &quot;Description: &quot; & objItem.Description
    Wscript.Echo &quot;Device ID: &quot; & objItem.DeviceID
    Wscript.Echo &quot;Device Interface: &quot; & objItem.DeviceInterface
    Wscript.Echo &quot;Double Speed Threshold: &quot; & objItem.DoubleSpeedThreshold
    Wscript.Echo &quot;Handedness: &quot; & objItem.Handedness
    Wscript.Echo &quot;Hardware Type: &quot; & objItem.HardwareType
    Wscript.Echo &quot;INF File Name: &quot; & objItem.InfFileName
    Wscript.Echo &quot;INF Section: &quot; & objItem.InfSection
    Wscript.Echo &quot;Manufacturer: &quot; & objItem.Manufacturer
    Wscript.Echo &quot;Name: &quot; & objItem.Name
    Wscript.Echo &quot;Number Of Buttons: &quot; & objItem.NumberOfButtons
    Wscript.Echo &quot;PNP Device ID: &quot; & objItem.PNPDeviceID
    Wscript.Echo &quot;Pointing Type: &quot; & objItem.PointingType
    Wscript.Echo &quot;Quad Speed Threshold: &quot; & objItem.QuadSpeedThreshold
    Wscript.Echo &quot;Resolution: &quot; & objItem.Resolution
    Wscript.Echo &quot;Sample Rate: &quot; & objItem.SampleRate
    Wscript.Echo &quot;Synch: &quot; & objItem.Synch
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
<th><span data-ttu-id="5eb77-153">PowerShell</span><span class="sxs-lookup"><span data-stu-id="5eb77-153">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code># Get Mouse information

$mouse = Get-WmiObject -Class Win32_PointingDevice

<# Decode detalis #>

function Deviceinterface {
    param ($value)
    switch ($value) {
        0 {&quot;Other&quot;}
        1 {&quot;Unknown&quot;}
        3 {&quot;Serial&quot;}
        4 {&quot;PS/2&quot;}
        5 {&quot;Infrared&quot;}
        6 {&quot;HP-HIL&quot;}
        7 {&quot;Bus Mouse&quot;}
        8 {&quot;ADP (Apple Desktop Bus)&quot;}
        160 {&quot;Bus Mouse DB-9&quot;}
        161 {&quot;Bus Mouse Micro-DIN&quot;}
        162 {&quot;USB&quot;}
    }
}

function Handedness {
    param ($value)
    switch ($value) {
        0 {&quot;Unknown&quot;}
        1 {&quot;Not Applicable&quot;}
        2 {&quot;Right-Handed Operation&quot;}
        3 {&quot;Left-Handed Operation&quot;}
    }
}

function Pointingtype {

param ($value)
    switch ($value) {
        1 {&quot;Other&quot;}
        2 {&quot;Unknown&quot;}
        3 {&quot;Mouse&quot;}
        4 {&quot;Track Ball&quot;}
        5 {&quot;Track Point&quot;}
        6 {&quot;Glide Point&quot;}
        7 {&quot;Touch Pad&quot;}
        8 {&quot;Touch Screen&quot;}
        9 {&quot;Mouse - Optical Sensor&quot;}
    }
}

<# Display details #>

&quot;Mouse Information on System: {0}&quot; -f $mouse.systemname
&quot;Description : {0}&quot; -f $mouse.Description
&quot;Device ID : {0}&quot; -f $mouse.DeviceID
&quot;Device Interface : {0}&quot; -f (Deviceinterface($mouse.DeviceInterface))
&quot;Double Speed Threshold : {0}&quot; -f $mouse.DoubleSpeedThreshold
&quot;Handedness : {0}&quot; -f (Handedness($mouse.handedness))
&quot;Hardware Type : {0}&quot; -f $mouse.Hardwaretype
&quot;INF FIle Name : {0}&quot; -f $mouse.InfFileName
&quot;Inf Section : {0}&quot; -f $mouse.InfSection
&quot;Manufacturer : {0}&quot; -f $mouse.Manufacturer
&quot;Name : {0}&quot; -f $mouse.Name
&quot;Number of buttons : {0}&quot; -f $mouse.NumberOfButtons
&quot;PNP Device ID : {0}&quot; -f $mouse.PNPDeviceID
&quot;Pointing Type : {0}&quot; -f (Pointingtype ($mouse.PointingType))
&quot;Quad Speed Threshold : {0}&quot; -f $mouse.QuadSpeedThreshold
&quot;Resolution : {0}&quot; -f $mouse.Resolution
&quot;Sample Rate : {0}&quot; -f $mouse.SampleRate
&quot;Synch : {0}&quot; -f $mouse.Synch</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5eb77-154">... определить скорость процессора, установленного на компьютере?</span><span class="sxs-lookup"><span data-stu-id="5eb77-154">...determine the speed of a processor installed in a computer?</span></span></td>
<td><p><span data-ttu-id="5eb77-155">Используйте класс <a href="/windows/desktop/CIMWin32Prov/win32-processor"><strong>Win32_Processor</strong></a> и проверьте значение свойства <strong>максклоккспид</strong> .</span><span class="sxs-lookup"><span data-stu-id="5eb77-155">Use the <a href="/windows/desktop/CIMWin32Prov/win32-processor"><strong>Win32_Processor</strong></a> class and check the value of the <strong>MaxClockSpeed</strong> property.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5eb77-156">VB</span><span class="sxs-lookup"><span data-stu-id="5eb77-156">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colItems = objWMIService.ExecQuery(&quot;Select * from Win32_Processor&quot;)
For Each objItem in colItems
    Wscript.Echo &quot;Processor Id: &quot; & objItem.ProcessorId
    Wscript.Echo &quot;Maximum Clock Speed: &quot; & objItem.MaxClockSpeed
Next</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5eb77-157">... как определить, является ли компьютер корпусом Tower, Мини-башня, ноутбуком и т. д.?</span><span class="sxs-lookup"><span data-stu-id="5eb77-157">...determine whether a computer is a tower, a mini-tower, a laptop, and so on?</span></span></td>
<td><p><span data-ttu-id="5eb77-158">Используйте класс <a href="/windows/desktop/CIMWin32Prov/win32-systemenclosure"><strong>Win32_SystemEnclosure</strong></a> и проверьте значение свойства <strong>чассистипе</strong> .</span><span class="sxs-lookup"><span data-stu-id="5eb77-158">Use the <a href="/windows/desktop/CIMWin32Prov/win32-systemenclosure"><strong>Win32_SystemEnclosure</strong></a> class and check the value of the <strong>ChassisType</strong> property.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5eb77-159">VB</span><span class="sxs-lookup"><span data-stu-id="5eb77-159">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colChassis = objWMIService.ExecQuery(&quot;Select * from Win32_SystemEnclosure&quot;)
For Each objChassis in colChassis
    For Each objItem in objChassis.ChassisTypes
        Wscript.Echo &quot;Chassis Type: &quot; & objItem
    Next
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
<th><span data-ttu-id="5eb77-160">PowerShell</span><span class="sxs-lookup"><span data-stu-id="5eb77-160">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$processors = Get-WmiObject -Class Win32_Processor
foreach ($proc in $processors)
{
    &quot;Processor ID: &quot; + $proc.ProcessorID
    &quot;Maximum Clock Speed: &quot; + $proc.MaxClockSpeed
}</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5eb77-161">... получить серийный номер и тег ресурса для компьютера?</span><span class="sxs-lookup"><span data-stu-id="5eb77-161">...get the serial number and asset tag of a computer?</span></span></td>
<td><p><span data-ttu-id="5eb77-162">Используйте класс <a href="/windows/desktop/CIMWin32Prov/win32-systemenclosure"><strong>Win32_SystemEnclosure</strong></a> и свойства <strong>SerialNumber</strong> и <strong>смбиосассеттаг</strong>.</span><span class="sxs-lookup"><span data-stu-id="5eb77-162">Use the <a href="/windows/desktop/CIMWin32Prov/win32-systemenclosure"><strong>Win32_SystemEnclosure</strong></a> class, and the properties <strong>SerialNumber</strong> and <strong>SMBIOSAssetTag</strong>.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5eb77-163">VB</span><span class="sxs-lookup"><span data-stu-id="5eb77-163">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colSMBIOS = objWMIService.ExecQuery(&quot;Select * from Win32_SystemEnclosure&quot;)
For Each objSMBIOS in colSMBIOS
    Wscript.Echo &quot;Part Number: &quot; & objSMBIOS.PartNumber
    Wscript.Echo &quot;Serial Number: &quot; & objSMBIOS.SerialNumber
    Wscript.Echo &quot;Asset Tag: &quot; & objSMBIOS.SMBIOSAssetTag
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
<th><span data-ttu-id="5eb77-164">PowerShell</span><span class="sxs-lookup"><span data-stu-id="5eb77-164">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$colSMBIOS = Get-WmiObject -Class Win32_SystemEnclosure

foreach ($objSMBIOS in $colSMBIOS)
{
    &quot;Part Number: &quot; + $objSMBIOS.PartNumber
    &quot;Serial Number: &quot; + $objSMBIOS.SerialNumber
    &quot;Asset Tag: &quot; + $objSMBIOS.SMBIOSAssetTag
}</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5eb77-165">... определить тип устройства, подключенного к USB-порту?</span><span class="sxs-lookup"><span data-stu-id="5eb77-165">...determine what kind of device is plugged into a USB port?</span></span></td>
<td><p><span data-ttu-id="5eb77-166">Используйте класс <a href="/previous-versions/windows/desktop/cimwin32a/win32-usbhub"><strong>Win32_USBHub</strong></a> и проверьте свойство <strong>Description</strong> .</span><span class="sxs-lookup"><span data-stu-id="5eb77-166">Use the <a href="/previous-versions/windows/desktop/cimwin32a/win32-usbhub"><strong>Win32_USBHub</strong></a> class and check the <strong>Description</strong> property.</span></span> <span data-ttu-id="5eb77-167">Это свойство может иметь такие значения, как &quot; запоминающее устройство &quot; или &quot; Поддержка печати &quot; .</span><span class="sxs-lookup"><span data-stu-id="5eb77-167">This property may have a value such as &quot;Mass Storage Device&quot; or &quot;Printing Support&quot;.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5eb77-168">VB</span><span class="sxs-lookup"><span data-stu-id="5eb77-168">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colItems = objWMIService.ExecQuery(&quot;Select * from Win32_USBHub&quot;)
For Each objItem in colItems
    Wscript.Echo &quot;Device ID: &quot; & objItem.DeviceID
    Wscript.Echo &quot;PNP Device ID: &quot; & objItem.PNPDeviceID
    Wscript.Echo &quot;Description: &quot; & objItem.Description
    Wscript.Echo
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
<th><span data-ttu-id="5eb77-169">PowerShell</span><span class="sxs-lookup"><span data-stu-id="5eb77-169">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$colItems = Get-WmiObject -Class Win32_USBHub

foreach ($objItem in $colItems)
{
    &quot;Device ID: &quot; + $objItem.DeviceID
    &quot;PNP Device ID: &quot; + $objItem.PNPDeviceID
    &quot;Description: &quot; + $objItem.Description
}</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5eb77-170">... определить, сколько ленточных накопителей установлено на компьютере?</span><span class="sxs-lookup"><span data-stu-id="5eb77-170">...determine how many tape drives are installed on a computer?</span></span></td>
<td><p><span data-ttu-id="5eb77-171">Используйте класс <a href="/windows/desktop/CIMWin32Prov/win32-tapedrive"><strong>Win32_TapeDrive</strong></a> класса, а затем используйте метод <a href="swbemobjectset-count.md"><strong>SWbemObjectSet. Count</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="5eb77-171">Use the class <a href="/windows/desktop/CIMWin32Prov/win32-tapedrive"><strong>Win32_TapeDrive</strong></a> class and then use the <a href="swbemobjectset-count.md"><strong>SWbemObjectSet.Count</strong></a> method.</span></span> <span data-ttu-id="5eb77-172">Если параметр count = 0, на компьютере не установлены ленточные накопители.</span><span class="sxs-lookup"><span data-stu-id="5eb77-172">If Count = 0, then no tape drives are installed on the computer.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5eb77-173">VB</span><span class="sxs-lookup"><span data-stu-id="5eb77-173">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colItems = objWMIService.ExecQuery(&quot;Select * from Win32_TapeDrive&quot;)
Wscript.Echo &quot;Number of tape drives: &quot; & colItems.Count</code></pre></td>
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
<th><span data-ttu-id="5eb77-174">PowerShell</span><span class="sxs-lookup"><span data-stu-id="5eb77-174">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$colItems = Get-WmiObject -Class Win32_TapeDrive

foreach ($objItem in $colItems)
{
    &quot;Number of Drives: &quot; + $colItems.Count
}</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
</tbody>
</table>



 

## <a name="examples"></a><span data-ttu-id="5eb77-175">Примеры</span><span class="sxs-lookup"><span data-stu-id="5eb77-175">Examples</span></span>

<span data-ttu-id="5eb77-176">В следующем [примере кода](https://Gallery.TechNet.Microsoft.Com/scriptcenter/List-for-several-machines-1baf6df0) коллекции TechNet описывается, как получить список свободного места для всех дисков на нескольких компьютерах.</span><span class="sxs-lookup"><span data-stu-id="5eb77-176">The following TechNet Gallery [example code](https://Gallery.TechNet.Microsoft.Com/scriptcenter/List-for-several-machines-1baf6df0) describes how to list the free space of all drives for several machines.</span></span>

<span data-ttu-id="5eb77-177">В примере PowerShell [Get-компутеринфо-запрос сведений о компьютере с локального компьютера или удаленного компьютера (WMI)](https://Gallery.TechNet.Microsoft.Com/Get-ComputerInfo-Query-23dd6042) в галерее TechNet используется ряд вызовов оборудования и программного обеспечения для вывода сведений о локальной или удаленной системе.</span><span class="sxs-lookup"><span data-stu-id="5eb77-177">The [Get-ComputerInfo - Query Computer Info From Local/Remote Computers - (WMI)](https://Gallery.TechNet.Microsoft.Com/Get-ComputerInfo-Query-23dd6042) PowerShell sample on TechNet Gallery uses a number of calls to hardware and software to display information about a local or remote system.</span></span>

<span data-ttu-id="5eb77-178">[Многопоточный сбор системных ресурсов с помощью PowerShell](https://Gallery.TechNet.Microsoft.Com/Multithreaded-System-Asset-856a8f7c) PowerShell в течнетгаллери собирает множество полезных системных сведений с помощью WMI и многопоточности с помощью PowerShell.</span><span class="sxs-lookup"><span data-stu-id="5eb77-178">The [Multithreaded System Asset Gathering with Powershell](https://Gallery.TechNet.Microsoft.Com/Multithreaded-System-Asset-856a8f7c) PowerShell sample on TechNetGallery gathers a plethora of useful system information via WMI and multithreading with powershell.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5eb77-179">См. также</span><span class="sxs-lookup"><span data-stu-id="5eb77-179">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5eb77-180">Задачи WMI для скриптов и приложений</span><span class="sxs-lookup"><span data-stu-id="5eb77-180">WMI Tasks for Scripts and Applications</span></span>](wmi-tasks-for-scripts-and-applications.md)
</dt> <dt>

[<span data-ttu-id="5eb77-181">Примеры приложений WMI на C++</span><span class="sxs-lookup"><span data-stu-id="5eb77-181">WMI C++ Application Examples</span></span>](wmi-c---application-examples.md)
</dt> <dt>

[<span data-ttu-id="5eb77-182">Скриптцентер TechNet</span><span class="sxs-lookup"><span data-stu-id="5eb77-182">TechNet ScriptCenter</span></span>](https://www.microsoft.com/technet/scriptcenter)
</dt> </dl>

