---
description: Задачи WMI для операционных систем получают сведения об операционной системе, такие как версия, активирована или какие исправления установлены.
ms.assetid: a216ad56-2650-4d93-86e1-449b56019361
ms.tgt_platform: multiple
title: 'Задачи WMI: операционные системы'
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a8d4dff83cebf5fd3336aeec2cc45ac4d8498cdb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105656698"
---
# <a name="wmi-tasks-operating-systems"></a><span data-ttu-id="f50dc-103">Задачи WMI: операционные системы</span><span class="sxs-lookup"><span data-stu-id="f50dc-103">WMI Tasks: Operating Systems</span></span>

<span data-ttu-id="f50dc-104">Задачи WMI для операционных систем получают сведения об операционной системе, такие как версия, активирована или какие исправления установлены.</span><span class="sxs-lookup"><span data-stu-id="f50dc-104">WMI tasks for operating systems obtain information about the operating system, such as version, whether it is activated, or which hotfixes are installed.</span></span>

<span data-ttu-id="f50dc-105">Примеры сценариев, приведенные в этом разделе, получают данные только с локального компьютера.</span><span class="sxs-lookup"><span data-stu-id="f50dc-105">The script examples shown in this topic obtain data only from the local computer.</span></span> <span data-ttu-id="f50dc-106">Дополнительные сведения об использовании сценария для получения данных с удаленных компьютеров см. в разделе [Подключение к WMI на удаленном компьютере](connecting-to-wmi-on-a-remote-computer.md).</span><span class="sxs-lookup"><span data-stu-id="f50dc-106">For more information about how to use the script to obtain data from remote computers, see [Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span></span>


<span data-ttu-id="f50dc-107">В следующей процедуре описывается выполнение скрипта.</span><span class="sxs-lookup"><span data-stu-id="f50dc-107">The following procedure describes how to run a script.</span></span>

<span data-ttu-id="f50dc-108">**Запуск сценария**</span><span class="sxs-lookup"><span data-stu-id="f50dc-108">**To run a script**</span></span>

1.  <span data-ttu-id="f50dc-109">Скопируйте код и сохраните его в файле с расширением vbs, например *filename.vbs*.</span><span class="sxs-lookup"><span data-stu-id="f50dc-109">Copy the code and save it in a file with a .vbs extension, such as *filename.vbs*.</span></span> <span data-ttu-id="f50dc-110">Убедитесь, что текстовый редактор не добавляет расширение txt в файл.</span><span class="sxs-lookup"><span data-stu-id="f50dc-110">Ensure that your text editor does not add a .txt extension to the file.</span></span>
2.  <span data-ttu-id="f50dc-111">Откройте окно командной строки и перейдите в каталог, в котором был сохранен файл.</span><span class="sxs-lookup"><span data-stu-id="f50dc-111">Open a command prompt window and navigate to the directory where you saved the file.</span></span>
3.  <span data-ttu-id="f50dc-112">Введите **CScript filename.vbs** в командной строке.</span><span class="sxs-lookup"><span data-stu-id="f50dc-112">Type **CScript filename.vbs** at the command prompt.</span></span>
4.  <span data-ttu-id="f50dc-113">Если доступ к журналу событий невозможен, проверьте, выполняется ли в командной строке с повышенными привилегиями.</span><span class="sxs-lookup"><span data-stu-id="f50dc-113">If you cannot access an event log, check to see if you are running from an Elevated command prompt.</span></span> <span data-ttu-id="f50dc-114">Некоторые журналы событий, например журнал событий безопасности, могут быть защищены с помощью элементов управления доступом пользователей (UAC).</span><span class="sxs-lookup"><span data-stu-id="f50dc-114">Some Event Log, such as the Security Event Log, may be protected by User Access Controls (UAC).</span></span>

> [!Note]  
> <span data-ttu-id="f50dc-115">По умолчанию CScript отображает выходные данные скрипта в окне командной строки.</span><span class="sxs-lookup"><span data-stu-id="f50dc-115">By default, CScript displays the output of a script in the command prompt window.</span></span> <span data-ttu-id="f50dc-116">Поскольку сценарии WMI могут создавать большие объемы выходных данных, может потребоваться перенаправить выходные данные в файл.</span><span class="sxs-lookup"><span data-stu-id="f50dc-116">Because WMI scripts can produce large amounts of output, you might want to redirect the output to a file.</span></span> <span data-ttu-id="f50dc-117">Введите **cscript filename.vbs > outfile.txt** в командной строке, чтобы перенаправить выходные данные скрипта *filename.vbs* в *outfile.txt*.</span><span class="sxs-lookup"><span data-stu-id="f50dc-117">Type **cscript filename.vbs > outfile.txt** at the command prompt to redirect the output of the *filename.vbs* script to *outfile.txt*.</span></span>

 

<span data-ttu-id="f50dc-118">В следующей таблице перечислены примеры сценариев, которые можно использовать для получения различных типов данных с локального компьютера.</span><span class="sxs-lookup"><span data-stu-id="f50dc-118">The following table lists script examples that can be used to obtain various types of data from the local computer.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f50dc-119">Часто выполняемые действия в новом интерфейсе</span><span class="sxs-lookup"><span data-stu-id="f50dc-119">How do I...</span></span></th>
<th><span data-ttu-id="f50dc-120">Классы или методы WMI</span><span class="sxs-lookup"><span data-stu-id="f50dc-120">WMI classes or methods</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f50dc-121">... определить, установлен ли на компьютере пакет обновления?</span><span class="sxs-lookup"><span data-stu-id="f50dc-121">...determine if a service pack has been installed on a computer?</span></span></td>
<td><span data-ttu-id="f50dc-122">Используйте класс <a href="/windows/desktop/CIMWin32Prov/win32-operatingsystem"><strong>Win32_OperatingSystem</strong></a> и проверьте значения свойств <strong>сервицепаккмажорверсион</strong> и <strong>сервицепаккминорверсион</strong> .</span><span class="sxs-lookup"><span data-stu-id="f50dc-122">Use the <a href="/windows/desktop/CIMWin32Prov/win32-operatingsystem"><strong>Win32_OperatingSystem</strong></a> class and check the value of the <strong>ServicePackMajorVersion</strong> and <strong>ServicePackMinorVersion</strong> properties.</span></span><br/> <span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f50dc-123">VB</span><span class="sxs-lookup"><span data-stu-id="f50dc-123">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colOperatingSystems = objWMIService.ExecQuery (&quot;Select * from Win32_OperatingSystem&quot;)
For Each objOperatingSystem in colOperatingSystems
    Wscript.Echo objOperatingSystem.ServicePackMajorVersion & &quot;.&quot; & objOperatingSystem.ServicePackMinorVersion
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
<th><span data-ttu-id="f50dc-124">PowerShell</span><span class="sxs-lookup"><span data-stu-id="f50dc-124">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>Get-WmiObject -Class Win32_OperatingSystem -Namespace &quot;root\cimv2&quot; | `
   format-list ServicePackMajorVersion, ServicePackMinorVersion</code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="f50dc-125">... определить, когда операционная система была установлена на компьютере?</span><span class="sxs-lookup"><span data-stu-id="f50dc-125">...determine when the operating system was installed on a computer?</span></span></td>
<td><p><span data-ttu-id="f50dc-126">Используйте класс <a href="/windows/desktop/CIMWin32Prov/win32-operatingsystem"><strong>Win32_OperatingSystem</strong></a> и свойство <strong>инсталлдате</strong> .</span><span class="sxs-lookup"><span data-stu-id="f50dc-126">Use the <a href="/windows/desktop/CIMWin32Prov/win32-operatingsystem"><strong>Win32_OperatingSystem</strong></a> class and the <strong>InstallDate</strong> property.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f50dc-127">VB</span><span class="sxs-lookup"><span data-stu-id="f50dc-127">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colOperatingSystems = objWMIService.ExecQuery (&quot;Select * from Win32_OperatingSystem&quot;)
For Each objOperatingSystem in colOperatingSystems
    Wscript.Echo &quot;Install Date: &quot; & objOperatingSystem.InstallDate 
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
<th><span data-ttu-id="f50dc-128">PowerShell</span><span class="sxs-lookup"><span data-stu-id="f50dc-128">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>Get-WmiObject -Class Win32_OperatingSystem -Namespace &quot;root\cimv2&quot; | format-list InstallDate</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f50dc-129">... определить, какая версия операционной системы Windows установлена на компьютере?</span><span class="sxs-lookup"><span data-stu-id="f50dc-129">...determine which version of the Windows operating system is installed on a computer?</span></span></td>
<td><p><span data-ttu-id="f50dc-130">Используйте класс <a href="/windows/desktop/CIMWin32Prov/win32-operatingsystem"><strong>Win32_OperatingSystem</strong></a> и получите свойства <strong>имени</strong> и <strong>версии</strong> .</span><span class="sxs-lookup"><span data-stu-id="f50dc-130">Use the <a href="/windows/desktop/CIMWin32Prov/win32-operatingsystem"><strong>Win32_OperatingSystem</strong></a> class, and retrieve both the <strong>Name</strong> and <strong>Version</strong> properties.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f50dc-131">VB</span><span class="sxs-lookup"><span data-stu-id="f50dc-131">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colOperatingSystems = objWMIService.ExecQuery (&quot;Select * from Win32_OperatingSystem&quot;)
For Each objOperatingSystem in colOperatingSystems
    Wscript.Echo objOperatingSystem.Caption & &quot;  &quot; & objOperatingSystem.Version
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
<th><span data-ttu-id="f50dc-132">PowerShell</span><span class="sxs-lookup"><span data-stu-id="f50dc-132">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>Get-WmiObject -Class Win32_OperatingSystem -Namespace &quot;root\cimv2&quot; | format-list Caption, Version</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f50dc-133">... определение папки, в которой находится папка Windows (% windir%) на компьютере?</span><span class="sxs-lookup"><span data-stu-id="f50dc-133">...determine which folder is the Windows folder (%Windir%) on a computer?</span></span></td>
<td><p><span data-ttu-id="f50dc-134">Используйте класс <a href="/windows/desktop/CIMWin32Prov/win32-operatingsystem"><strong>Win32_OperatingSystem</strong></a> и проверьте значение свойства <strong>виндовсдиректори</strong> .</span><span class="sxs-lookup"><span data-stu-id="f50dc-134">Use the <a href="/windows/desktop/CIMWin32Prov/win32-operatingsystem"><strong>Win32_OperatingSystem</strong></a> class, and check the value of the <strong>WindowsDirectory</strong> property.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f50dc-135">VB</span><span class="sxs-lookup"><span data-stu-id="f50dc-135">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colOperatingSystems = objWMIService.ExecQuery (&quot;Select * from Win32_OperatingSystem&quot;)
For Each objOperatingSystem in colOperatingSystems
    Wscript.Echo &quot;Windows Folder: &quot; & objOperatingSystem.WindowsDirectory
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
<th><span data-ttu-id="f50dc-136">PowerShell</span><span class="sxs-lookup"><span data-stu-id="f50dc-136">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>Get-WmiObject -Class Win32_OperatingSystem -Namespace &quot;root\cimv2&quot; | format-list WindowsDirectory</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f50dc-137">... определить, какие исправления установлены на компьютере?</span><span class="sxs-lookup"><span data-stu-id="f50dc-137">...determine what hotfixes have been installed on a computer?</span></span></td>
<td><p><span data-ttu-id="f50dc-138">Используйте класс <a href="/windows/desktop/CIMWin32Prov/win32-quickfixengineering"><strong>Win32_QuickFixEngineering</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="f50dc-138">Use the <a href="/windows/desktop/CIMWin32Prov/win32-quickfixengineering"><strong>Win32_QuickFixEngineering</strong></a> class.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f50dc-139">VB</span><span class="sxs-lookup"><span data-stu-id="f50dc-139">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colQuickFixes = objWMIService.ExecQuery (&quot;Select * from Win32_QuickFixEngineering&quot;)
For Each objQuickFix in colQuickFixes
    Wscript.Echo &quot;Description: &quot; & objQuickFix.Description
    Wscript.Echo &quot;Hotfix ID: &quot; & objQuickFix.HotFixID
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
<th><span data-ttu-id="f50dc-140">PowerShell</span><span class="sxs-lookup"><span data-stu-id="f50dc-140">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>Get-WmiObject -Class Win32_QuickFixEngineering -Namespace &quot;root\cimv2&quot; | format-list Description, HotFixIDs</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f50dc-141">... определить, нужно ли активировать операционную систему на компьютере?</span><span class="sxs-lookup"><span data-stu-id="f50dc-141">...determine if I need to activate the operating system on a computer?</span></span></td>
<td><p><span data-ttu-id="f50dc-142">Используйте класс <a href="/previous-versions/windows/desktop/legacy/aa394520(v=vs.85)"><strong>Win32_WindowsProductActivation</strong></a> и проверьте значение свойства <strong>активатионрекуиред</strong> .</span><span class="sxs-lookup"><span data-stu-id="f50dc-142">Use the <a href="/previous-versions/windows/desktop/legacy/aa394520(v=vs.85)"><strong>Win32_WindowsProductActivation</strong></a> class and check the value of the <strong>ActivationRequired</strong> property.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f50dc-143">VB</span><span class="sxs-lookup"><span data-stu-id="f50dc-143">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colWPA = objWMIService.ExecQuery (&quot;Select * from Win32_WindowsProductActivation&quot;)
For Each objWPA in colWPA
    Wscript.Echo &quot;Activation Required: &quot; & objWPA.ActivationRequired
    Wscript.Echo &quot;Remaining Evaluation Period: &quot; & objWPA.RemainingEvaluationPeriod
    Wscript.Echo &quot;Remaining Grace Period: &quot; & objWPA.RemainingGracePeriod
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
<th><span data-ttu-id="f50dc-144">PowerShell</span><span class="sxs-lookup"><span data-stu-id="f50dc-144">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>Get-WmiObject -Class Win32_WindowsProductActivation -computer &quot;.&quot; -Namespace &quot;root\cimv2&quot; | `
     format-list ActivationRequired, RemainingEvaluationPeriod, RemainingGracePeriod</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="f50dc-145">См. также</span><span class="sxs-lookup"><span data-stu-id="f50dc-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f50dc-146">Задачи WMI для скриптов и приложений</span><span class="sxs-lookup"><span data-stu-id="f50dc-146">WMI Tasks for Scripts and Applications</span></span>](wmi-tasks-for-scripts-and-applications.md)
</dt> <dt>

[<span data-ttu-id="f50dc-147">Примеры приложений WMI на C++</span><span class="sxs-lookup"><span data-stu-id="f50dc-147">WMI C++ Application Examples</span></span>](wmi-c---application-examples.md)
</dt> <dt>

[<span data-ttu-id="f50dc-148">Скриптцентер TechNet</span><span class="sxs-lookup"><span data-stu-id="f50dc-148">TechNet ScriptCenter</span></span>](https://www.microsoft.com/technet/scriptcenter)
</dt> </dl>

 

