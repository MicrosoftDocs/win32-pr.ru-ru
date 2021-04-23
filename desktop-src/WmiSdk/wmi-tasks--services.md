---
description: Задачи WMI для служб получают сведения о службах, включая зависимые или предшествующие службы. Другие примеры см. в разделе TechNet Скриптцентер по адресу https://www.microsoft.com/technet .
ms.assetid: 1cd92981-c074-4ff7-a32c-ce492e6d6aa5
ms.tgt_platform: multiple
title: 'Задачи WMI: службы'
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b786ce0e358a59922728be4e90bc8cdeaa37a298
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105656670"
---
# <a name="wmi-tasks-services"></a><span data-ttu-id="a1ab5-104">Задачи WMI: службы</span><span class="sxs-lookup"><span data-stu-id="a1ab5-104">WMI Tasks: Services</span></span>

<span data-ttu-id="a1ab5-105">Задачи WMI для служб получают сведения о службах, включая зависимые или предшествующие службы.</span><span class="sxs-lookup"><span data-stu-id="a1ab5-105">WMI tasks for services obtain information about services, including dependent or antecedent services.</span></span> <span data-ttu-id="a1ab5-106">Другие примеры см. в разделе TechNet Скриптцентер по адресу [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx) .</span><span class="sxs-lookup"><span data-stu-id="a1ab5-106">For other examples, see the TechNet ScriptCenter at [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx).</span></span>

<span data-ttu-id="a1ab5-107">Примеры сценариев, приведенные в этом разделе, получают данные только с локального компьютера.</span><span class="sxs-lookup"><span data-stu-id="a1ab5-107">The script examples shown in this topic obtain data only from the local computer.</span></span> <span data-ttu-id="a1ab5-108">Дополнительные сведения об использовании сценария для получения данных с удаленных компьютеров см. в разделе [Подключение к WMI на удаленном компьютере](connecting-to-wmi-on-a-remote-computer.md).</span><span class="sxs-lookup"><span data-stu-id="a1ab5-108">For more information about how to use the script to obtain data from remote computers, see [Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span></span>

<span data-ttu-id="a1ab5-109">В следующей процедуре описывается выполнение скрипта.</span><span class="sxs-lookup"><span data-stu-id="a1ab5-109">The following procedure describes how to run a script.</span></span>

<span data-ttu-id="a1ab5-110">**Запуск сценария**</span><span class="sxs-lookup"><span data-stu-id="a1ab5-110">**To run a script**</span></span>

1.  <span data-ttu-id="a1ab5-111">Скопируйте код и сохраните его в файле с расширением vbs, например *filename.vbs*.</span><span class="sxs-lookup"><span data-stu-id="a1ab5-111">Copy the code and save it in a file with a .vbs extension, such as *filename.vbs*.</span></span> <span data-ttu-id="a1ab5-112">Убедитесь, что текстовый редактор не добавляет расширение txt в файл.</span><span class="sxs-lookup"><span data-stu-id="a1ab5-112">Ensure that your text editor does not add a .txt extension to the file.</span></span>
2.  <span data-ttu-id="a1ab5-113">Откройте окно командной строки и перейдите в каталог, в котором был сохранен файл.</span><span class="sxs-lookup"><span data-stu-id="a1ab5-113">Open a command prompt window and navigate to the directory where you saved the file.</span></span>
3.  <span data-ttu-id="a1ab5-114">Введите **cscript filename.vbs** в командной строке.</span><span class="sxs-lookup"><span data-stu-id="a1ab5-114">Type **cscript filename.vbs** at the command prompt.</span></span>
4.  <span data-ttu-id="a1ab5-115">Если доступ к журналу событий невозможен, проверьте, выполняется ли в командной строке с повышенными привилегиями.</span><span class="sxs-lookup"><span data-stu-id="a1ab5-115">If you cannot access an event log, check to see if you are running from an Elevated command prompt.</span></span> <span data-ttu-id="a1ab5-116">Некоторые журналы событий, например журнал событий безопасности, могут быть защищены с помощью элементов управления доступом пользователей (UAC).</span><span class="sxs-lookup"><span data-stu-id="a1ab5-116">Some Event Log, such as the Security Event Log, may be protected by User Access Controls (UAC).</span></span>

> [!Note]  
> <span data-ttu-id="a1ab5-117">По умолчанию Cscript отображает выходные данные скрипта в окне командной строки.</span><span class="sxs-lookup"><span data-stu-id="a1ab5-117">By default, cscript displays the output of a script in the command prompt window.</span></span> <span data-ttu-id="a1ab5-118">Поскольку сценарии WMI могут создавать большие объемы выходных данных, может потребоваться перенаправить выходные данные в файл.</span><span class="sxs-lookup"><span data-stu-id="a1ab5-118">Because WMI scripts can produce large amounts of output, you might want to redirect the output to a file.</span></span> <span data-ttu-id="a1ab5-119">Введите **cscript filename.vbs > outfile.txt** в командной строке, чтобы перенаправить выходные данные скрипта *filename.vbs* в *outfile.txt*.</span><span class="sxs-lookup"><span data-stu-id="a1ab5-119">Type **cscript filename.vbs > outfile.txt** at the command prompt to redirect the output of the *filename.vbs* script to *outfile.txt*.</span></span>

 

<span data-ttu-id="a1ab5-120">В следующей таблице перечислены примеры сценариев, которые можно использовать для получения различных типов данных с локального компьютера.</span><span class="sxs-lookup"><span data-stu-id="a1ab5-120">The following table lists script examples that can be used to obtain various types of data from the local computer.</span></span>




<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a1ab5-121">Часто выполняемые действия в новом интерфейсе</span><span class="sxs-lookup"><span data-stu-id="a1ab5-121">How do I...</span></span></th>
<th><span data-ttu-id="a1ab5-122">Классы или методы WMI</span><span class="sxs-lookup"><span data-stu-id="a1ab5-122">WMI classes or methods</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a1ab5-123">... определить, какие службы работают, а какие нет?</span><span class="sxs-lookup"><span data-stu-id="a1ab5-123">...determine which services are running and which ones are not?</span></span></td>
<td><span data-ttu-id="a1ab5-124">Используйте класс <a href="/windows/desktop/CIMWin32Prov/win32-service"><strong>Win32_Service</strong></a> для проверки состояния всех служб.</span><span class="sxs-lookup"><span data-stu-id="a1ab5-124">Use the <a href="/windows/desktop/CIMWin32Prov/win32-service"><strong>Win32_Service</strong></a> class to check the state of all of the services.</span></span> <span data-ttu-id="a1ab5-125">Свойство State (состояние) позволяет выяснить, остановлена или запущена служба.</span><span class="sxs-lookup"><span data-stu-id="a1ab5-125">The state property lets you know if a service is stopped or running.</span></span><br/> <span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a1ab5-126">VB</span><span class="sxs-lookup"><span data-stu-id="a1ab5-126">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot; 
Set objWMIService = GetObject(&quot;winmgmts:\\&quot; & strComputer & &quot;\root\CIMV2&quot;) 
Set colItems = objWMIService.ExecQuery(&quot;SELECT * FROM Win32_Service&quot;,,48) 
For Each objItem in colItems 
    Wscript.Echo &quot;Service Name: &quot; & objItem.Name & VBNewLine & &quot;State: &quot; & objItem.State
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
<th><span data-ttu-id="a1ab5-127">PowerShell</span><span class="sxs-lookup"><span data-stu-id="a1ab5-127">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>Get-WmiObject -Class win32_service -computer &quot;.&quot; -Namespace &quot;root\cimv2&quot; | format-list Name, State</code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="a1ab5-128">... запретить опытным пользователям запускать определенные службы?</span><span class="sxs-lookup"><span data-stu-id="a1ab5-128">...stop Power Users from starting certain services?</span></span></td>
<td><p><span data-ttu-id="a1ab5-129">Используйте класс <a href="/windows/desktop/CIMWin32Prov/win32-service"><strong>Win32_Service</strong></a> и метод <a href="/windows/desktop/CIMWin32Prov/changestartmode-method-in-class-win32-service"><strong>чанжестартмоде</strong></a> , чтобы установить свойство <strong>StartMode</strong> в значение Disabled.</span><span class="sxs-lookup"><span data-stu-id="a1ab5-129">Use the <a href="/windows/desktop/CIMWin32Prov/win32-service"><strong>Win32_Service</strong></a> class and the <a href="/windows/desktop/CIMWin32Prov/changestartmode-method-in-class-win32-service"><strong>ChangeStartMode</strong></a> method to set the <strong>StartMode</strong> property to Disabled.</span></span> <span data-ttu-id="a1ab5-130">Отключенные службы не могут быть запущены, и по умолчанию опытные пользователи не могут изменить режим запуска службы.</span><span class="sxs-lookup"><span data-stu-id="a1ab5-130">Disabled services cannot be started, and, by default, Power Users cannot change the start mode of a service.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a1ab5-131">VB</span><span class="sxs-lookup"><span data-stu-id="a1ab5-131">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colServiceList = objWMIService.ExecQuery (&quot;Select * from Win32_Service where StartMode = &#39;Manual&#39;&quot;)
For Each objService in colServiceList
    errReturnCode = objService.Change( , , , , &quot;Disabled&quot;)
    WScript.Echo &quot;Changed manual service to disabled: &quot; & objService.Name   
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
<th><span data-ttu-id="a1ab5-132">PowerShell</span><span class="sxs-lookup"><span data-stu-id="a1ab5-132">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>Get-WmiObject -Class win32_service -computer &quot;.&quot; -Namespace &quot;root\cimv2&quot; | where {$_.startMode -eq &quot;Manual&quot;} | `
    foreach-object { [void]$_.changeStartMode(&#39;Disabled&#39;) }</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a1ab5-133">... запускать и прекращать работу служб?</span><span class="sxs-lookup"><span data-stu-id="a1ab5-133">...start and stop services?</span></span></td>
<td><p><span data-ttu-id="a1ab5-134">Используйте класс <a href="/windows/desktop/CIMWin32Prov/win32-service"><strong>Win32_Service</strong></a> и методы « <a href="/windows/desktop/CIMWin32Prov/stopservice-method-in-class-win32-service"><strong>а» и «</strong></a> <a href="/windows/desktop/CIMWin32Prov/startservice-method-in-class-win32-service"><strong>StartService</strong></a> ».</span><span class="sxs-lookup"><span data-stu-id="a1ab5-134">Use the <a href="/windows/desktop/CIMWin32Prov/win32-service"><strong>Win32_Service</strong></a> class and the <a href="/windows/desktop/CIMWin32Prov/stopservice-method-in-class-win32-service"><strong>StopService</strong></a> and <a href="/windows/desktop/CIMWin32Prov/startservice-method-in-class-win32-service"><strong>StartService</strong></a> methods.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a1ab5-135">VB</span><span class="sxs-lookup"><span data-stu-id="a1ab5-135">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colListOfServices = objWMIService.ExecQuery (&quot;Select * from Win32_Service Where Name =&#39;Alerter&#39;&quot;)
For Each objService in colListOfServices
    objService.StartService()
    Wscript.Echo &quot;Started Alerter service&quot;
Next
</code></pre></td>
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
<th><span data-ttu-id="a1ab5-136">PowerShell</span><span class="sxs-lookup"><span data-stu-id="a1ab5-136">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>Get-WmiObject -Class win32_service -computer &quot;.&quot; -Namespace &quot;root\cimv2&quot; | where {$_.Name -eq &quot;Alerter&quot;} | `
    foreach-object { [void]$_.StartService() }</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a1ab5-137">... изменить пароли учетной записи службы с помощью сценария?</span><span class="sxs-lookup"><span data-stu-id="a1ab5-137">...change service account passwords using a script?</span></span></td>
<td><p><span data-ttu-id="a1ab5-138">Используйте класс <a href="/windows/desktop/CIMWin32Prov/win32-service"><strong>Win32_Service</strong></a> и метод <a href="/windows/desktop/CIMWin32Prov/change-method-in-class-win32-service"><strong>Change</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="a1ab5-138">Use the <a href="/windows/desktop/CIMWin32Prov/win32-service"><strong>Win32_Service</strong></a> class and the <a href="/windows/desktop/CIMWin32Prov/change-method-in-class-win32-service"><strong>Change</strong></a> method.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a1ab5-139">VB</span><span class="sxs-lookup"><span data-stu-id="a1ab5-139">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colServiceList = objWMIService.ExecQuery (&quot;Select * from Win32_Service&quot;)
For Each objservice in colServiceList
    If objService.StartName = &quot;.\netsvc&quot; Then
        errReturn = objService.Change( , , , , , , , &quot;password&quot;)  
    End If 
Next</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a1ab5-140">.. определить, какие службы можно останавливаться?</span><span class="sxs-lookup"><span data-stu-id="a1ab5-140">..determine which services I can stop?</span></span></td>
<td><p><span data-ttu-id="a1ab5-141">Используйте класс <a href="/windows/desktop/CIMWin32Prov/win32-service"><strong>Win32_Service</strong></a> и проверьте значение свойства <strong>AcceptStop</strong> .</span><span class="sxs-lookup"><span data-stu-id="a1ab5-141">Use the <a href="/windows/desktop/CIMWin32Prov/win32-service"><strong>Win32_Service</strong></a> class, and check the value of the <strong>AcceptStop</strong> property.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a1ab5-142">VB</span><span class="sxs-lookup"><span data-stu-id="a1ab5-142">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colServices = objWMIService.ExecQuery (&quot;Select * from Win32_Service Where AcceptStop = True&quot;)
For Each objService in colServices
    Wscript.Echo objService.DisplayName 
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
<th><span data-ttu-id="a1ab5-143">PowerShell</span><span class="sxs-lookup"><span data-stu-id="a1ab5-143">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>Get-WmiObject -Class win32_service -computer &quot;.&quot; -Namespace &quot;root\cimv2&quot; | where {$_.AcceptStop -eq &quot;True&quot;} | `
     format-list DisplayName</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a1ab5-144">... найти службы, которые должны быть запущены, прежде чем можно будет запустить службу DHCP?</span><span class="sxs-lookup"><span data-stu-id="a1ab5-144">...find the services that must be running before I can start the DHCP service?</span></span></td>
<td><p><span data-ttu-id="a1ab5-145">Запрос для <a href="associators-of-statement.md">соединителей</a> <a href="/windows/desktop/CIMWin32Prov/win32-service"><strong>Win32_Service</strong></a> класса с именем &quot; DHCP, которые &quot; находятся в классе <a href="/windows/desktop/CIMWin32Prov/win32-dependentservice"><strong>Win32_DependentService</strong></a> и имеют &quot; зависимость от &quot; свойства <strong>Role</strong> .</span><span class="sxs-lookup"><span data-stu-id="a1ab5-145">Query for <a href="associators-of-statement.md">ASSOCIATORS OF</a> the <a href="/windows/desktop/CIMWin32Prov/win32-service"><strong>Win32_Service</strong></a> class named &quot;DHCP&quot; that are in the <a href="/windows/desktop/CIMWin32Prov/win32-dependentservice"><strong>Win32_DependentService</strong></a> class and have &quot;Dependent&quot; in the <strong>Role</strong> property.</span></span> <span data-ttu-id="a1ab5-146"><strong>Роль</strong> означает роль службы DHCP. в этом случае она зависит от других запущенных служб.</span><span class="sxs-lookup"><span data-stu-id="a1ab5-146"><strong>Role</strong> means the role of the DHCP service: in this case, it is dependent on the other services that are being started.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a1ab5-147">VB</span><span class="sxs-lookup"><span data-stu-id="a1ab5-147">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colServiceList = objWMIService.ExecQuery(&quot;Associators Of &quot; _ 
    & &quot;{Win32_Service.Name=&#39;dhcp&#39;} Where &quot; _
    & &quot;AssocClass=Win32_DependentService &quot; _
    & &quot;Role=Dependent&quot;) 
For Each objService in colServiceList
Wscript.Echo objService.DisplayName 
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
<th><span data-ttu-id="a1ab5-148">PowerShell</span><span class="sxs-lookup"><span data-stu-id="a1ab5-148">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$query = &quot;Associators Of {Win32_Service.Name=&#39;dhcp&#39;} Where AssocClass=Win32_DependentService Role=Dependent&quot;
Get-WmiObject -Query $query -Namespace &quot;root\cimv2&quot; | format-list DisplayName</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a1ab5-149">... Найдите службы, для которых требуется служба WMI (winmgmt), прежде чем они смогут начать работу?</span><span class="sxs-lookup"><span data-stu-id="a1ab5-149">...find the services that require the WMI service (Winmgmt) service to be running before they can start?</span></span></td>
<td><p><span data-ttu-id="a1ab5-150">Запрос для <a href="associators-of-statement.md">соединителей</a> <a href="/windows/desktop/CIMWin32Prov/win32-service"><strong>Win32_Service</strong></a> класса с именем &quot; DHCP, которые &quot; находятся в классе <a href="/windows/desktop/CIMWin32Prov/win32-dependentservice"><strong>Win32_DependentService</strong></a> и имеют &quot; антецендент &quot; в свойстве <strong>Role</strong> .</span><span class="sxs-lookup"><span data-stu-id="a1ab5-150">Query for <a href="associators-of-statement.md">ASSOCIATORS OF</a> the <a href="/windows/desktop/CIMWin32Prov/win32-service"><strong>Win32_Service</strong></a> class named &quot;DHCP&quot; that are in the <a href="/windows/desktop/CIMWin32Prov/win32-dependentservice"><strong>Win32_DependentService</strong></a> class and have &quot;Antecendent&quot; in the <strong>Role</strong> property.</span></span> <span data-ttu-id="a1ab5-151"><strong>Роль</strong> означает роль службы RASMAN: в этом случае задача должна быть запущена до зависимых служб.</span><span class="sxs-lookup"><span data-stu-id="a1ab5-151"><strong>Role</strong> means the role of the rasman service: in this case, it is antecedent to must be started before the dependent services.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a1ab5-152">VB</span><span class="sxs-lookup"><span data-stu-id="a1ab5-152">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\ & strComputer & &quot;\root\cimv2&quot;)
Set colServiceList = _
    objWMIService.ExecQuery(&quot;Associators of &quot; _
    & &quot;{Win32_Service.Name=&#39;winmgmt&#39;} Where &quot; _
    & &quot;AssocClass=Win32_DependentService &quot; _
    & &quot;Role=Antecedent&quot; )
For Each objService in colServiceList
Wscript.Echo &quot;Name: &quot; & objService.Name & VBTab & &quot;Display Name: &quot; & objService.DisplayName 
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
<th><span data-ttu-id="a1ab5-153">PowerShell</span><span class="sxs-lookup"><span data-stu-id="a1ab5-153">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$query = &quot;Associators of {Win32_Service.Name=&#39;winmgmt&#39;} Where AssocClass=Win32_DependentService Role=Antecedent&quot;
Get-WmiObject -Query $query -Namespace &quot;root\cimv2&quot; | format-list Name, DisplayName</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="a1ab5-154">См. также</span><span class="sxs-lookup"><span data-stu-id="a1ab5-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a1ab5-155">Задачи WMI для скриптов и приложений</span><span class="sxs-lookup"><span data-stu-id="a1ab5-155">WMI Tasks for Scripts and Applications</span></span>](wmi-tasks-for-scripts-and-applications.md)
</dt> <dt>

[<span data-ttu-id="a1ab5-156">Примеры приложений WMI на C++</span><span class="sxs-lookup"><span data-stu-id="a1ab5-156">WMI C++ Application Examples</span></span>](wmi-c---application-examples.md)
</dt> <dt>

[<span data-ttu-id="a1ab5-157">Скриптцентер TechNet</span><span class="sxs-lookup"><span data-stu-id="a1ab5-157">TechNet ScriptCenter</span></span>](https://www.microsoft.com/technet/scriptcenter)
</dt> </dl>

 

 



`
