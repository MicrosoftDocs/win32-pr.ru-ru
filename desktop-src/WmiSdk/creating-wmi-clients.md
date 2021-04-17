---
description: Инструментарий WMI предоставляет стандартизированную инфраструктуру управления системой, которую можно использовать с помощью нескольких различных клиентов.
ms.assetid: 7aa0ead7-010c-4ad2-b6ba-0ef84263d5c6
ms.tgt_platform: multiple
title: Создание клиентов WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6dd6d89c63218ffd20ef66b2115e581bdb9c4373
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711743"
---
# <a name="creating-wmi-clients"></a><span data-ttu-id="15dc1-103">Создание клиентов WMI</span><span class="sxs-lookup"><span data-stu-id="15dc1-103">Creating WMI Clients</span></span>

<span data-ttu-id="15dc1-104">Инструментарий WMI предоставляет стандартизированную инфраструктуру управления системой, которую можно использовать с помощью нескольких различных клиентов.</span><span class="sxs-lookup"><span data-stu-id="15dc1-104">WMI provides a standardized system management infrastructure that can be leveraged by a number of different clients.</span></span> <span data-ttu-id="15dc1-105">Эти клиенты находятся в диапазоне от wmic.exe программы командной строки до System Center Operations Manager.</span><span class="sxs-lookup"><span data-stu-id="15dc1-105">These clients range from the wmic.exe command line tool to System Center Operations Manager.</span></span> <span data-ttu-id="15dc1-106">Вы можете создавать собственные клиенты WMI с помощью API сценариев WMI, собственного API C++ или с помощью типов в пространстве имен библиотеки классов System. Management платформа .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="15dc1-106">You can write your own WMI clients by using either the WMI Scripting API, the native C++ API or by using the types in the System.Management .NET Framework class library namespace.</span></span>

## <a name="how-to-create-a-wmi-client"></a><span data-ttu-id="15dc1-107">Создание клиента WMI</span><span class="sxs-lookup"><span data-stu-id="15dc1-107">How to create a WMI client</span></span>

<span data-ttu-id="15dc1-108">Основные функциональные возможности WMI состоят из извлечения объектов из репозитория WMI и изучения свойств этих объектов.</span><span class="sxs-lookup"><span data-stu-id="15dc1-108">The core functionality of WMI consists of retrieving objects from the WMI repository and examining the properties of those objects.</span></span> <span data-ttu-id="15dc1-109">Можно также обновить эти свойства или вызвать методы для этих свойств.</span><span class="sxs-lookup"><span data-stu-id="15dc1-109">You can also choose to update those properties, or call methods on those properties.</span></span> <span data-ttu-id="15dc1-110">В следующих примерах показано, как выполнить базовую задачу администрирования WMI: получение имени локального компьютера.</span><span class="sxs-lookup"><span data-stu-id="15dc1-110">The following examples show how to perform a basic WMI administration task: retrieving the name of the local computer.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="15dc1-111">Термин</span><span class="sxs-lookup"><span data-stu-id="15dc1-111">Term</span></span></th>
<th><span data-ttu-id="15dc1-112">Описание</span><span class="sxs-lookup"><span data-stu-id="15dc1-112">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="15dc1-113"><span id="Creating_a_client_with_PowerShell"></span><span id="creating_a_client_with_powershell"></span><span id="CREATING_A_CLIENT_WITH_POWERSHELL"></span>Создание клиента с помощью PowerShell</span><span class="sxs-lookup"><span data-stu-id="15dc1-113"><span id="Creating_a_client_with_PowerShell"></span><span id="creating_a_client_with_powershell"></span><span id="CREATING_A_CLIENT_WITH_POWERSHELL"></span>Creating a client with PowerShell</span></span><br/></td>
<td><span data-ttu-id="15dc1-114">WMI и PowerShell тесно интегрированы; Таким образом, получение объектов WMI с помощью PowerShell — это просто вопрос вызова командлета Get-WmiObject.</span><span class="sxs-lookup"><span data-stu-id="15dc1-114">WMI and PowerShell are tightly integrated; as such, retrieving WMI objects with PowerShell is simply a matter of calling the Get-WmiObject cmdlet.</span></span> <span data-ttu-id="15dc1-115">Обратите внимание, что для обеспечения согласованности в первом фрагменте кода явно указано множество значений по умолчанию. во втором предполагается, что значения по умолчанию верны.</span><span class="sxs-lookup"><span data-stu-id="15dc1-115">Note that for consistency, the first code snippet explicitly states many of the default values; the second assumes that the default values are correct.</span></span><br/> <span data-codelanguage="PowerShell"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="15dc1-116">PowerShell</span><span class="sxs-lookup"><span data-stu-id="15dc1-116">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>#explicitly states many of the default parameters
$myComputer = Get-WmiObject -ComputerName &quot;.&quot; -Namespace &quot;root\cimv2&quot; -Query &quot;SELECT * FROM Win32_ComputerSystem&quot;
foreach ($computer in $myComputer)
{ &quot;System Name: &quot; + $computer.name }

#assumes the default values are correct
Get-WmiObject Win32_ComputerSystem | Format-Table &quot;Name&quot;</code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="15dc1-117"><span id="Creating_a_client_with_VBScript"></span><span id="creating_a_client_with_vbscript"></span><span id="CREATING_A_CLIENT_WITH_VBSCRIPT"></span>Создание клиента с помощью VBScript</span><span class="sxs-lookup"><span data-stu-id="15dc1-117"><span id="Creating_a_client_with_VBScript"></span><span id="creating_a_client_with_vbscript"></span><span id="CREATING_A_CLIENT_WITH_VBSCRIPT"></span>Creating a client with VBScript</span></span></p></td>
<td><p><span data-ttu-id="15dc1-118">VBScript был исходным языком сценариев, который часто использовался в WMI.</span><span class="sxs-lookup"><span data-stu-id="15dc1-118">VBScript was the original scripting language that had common use with WMI.</span></span> <span data-ttu-id="15dc1-119">Хотя PowerShell стал более популярным, многие из существующих примеров кода в этой документации написаны на языке VBScript.</span><span class="sxs-lookup"><span data-stu-id="15dc1-119">While PowerShell has become more popular, many of the existing code samples in this documentation are written in VBScript.</span></span> <span data-ttu-id="15dc1-120">Обратите внимание, что в этом образце VBScript явным образом указывается как путь к локальному компьютеру, так и уровень олицетворения. Это не является обязательным, но часто рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="15dc1-120">Note that this particular VBScript sample explicitly states both the local machine path as well as the impersonation level; this is not required, but is often a best practice.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="15dc1-121">VB</span><span class="sxs-lookup"><span data-stu-id="15dc1-121">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colItems = objWMIService.ExecQuery(&quot;Select * from Win32_ComputerSystem&quot;)
For Each objItem in colItems
    Wscript.Echo &quot;Computer Name: &quot; & objItem.Name
Next</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="15dc1-122"><span id="Creating_a_client_with_C___Microsoft.Management.Infrastructure_"></span><span id="creating_a_client_with_c___microsoft.management.infrastructure_"></span><span id="CREATING_A_CLIENT_WITH_C___MICROSOFT.MANAGEMENT.INFRASTRUCTURE_"></span>Создание клиента с помощью C# (<a href="/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)">Microsoft. Management. Infrastructure</a>)</span><span class="sxs-lookup"><span data-stu-id="15dc1-122"><span id="Creating_a_client_with_C___Microsoft.Management.Infrastructure_"></span><span id="creating_a_client_with_c___microsoft.management.infrastructure_"></span><span id="CREATING_A_CLIENT_WITH_C___MICROSOFT.MANAGEMENT.INFRASTRUCTURE_"></span>Creating a client with C# (<a href="/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)">Microsoft.Management.Infrastructure</a>)</span></span></p></td>
<td><p><span data-ttu-id="15dc1-123">Это пространство имен содержит текущее решение для доступа к инструментарию WMI с управляемым кодом и называется инфраструктурой управления Windows (MI или WMI).</span><span class="sxs-lookup"><span data-stu-id="15dc1-123">This namespace contains the current solution for accessing WMI with managed code, and is known as the Windows Management Infrastructure (MI, or WMIv2).</span></span> <span data-ttu-id="15dc1-124">В настоящее время MI — это поддерживаемая технология для создания управляемых клиентов управления.</span><span class="sxs-lookup"><span data-stu-id="15dc1-124">Currently, MI is the supported technology for creating managed management clients.</span></span> <span data-ttu-id="15dc1-125">Дополнительные сведения см. <a href="/previous-versions/windows/desktop/wmi_v2/how-to-implement-a-managed-mi-client">в разделе Реализация управляемого клиента MI</a> и <a href="/previous-versions/windows/desktop/wmi_v2/how-to-implement-a-native-mi-client">реализация собственного клиента MI</a>.</span><span class="sxs-lookup"><span data-stu-id="15dc1-125">For more information, see <a href="/previous-versions/windows/desktop/wmi_v2/how-to-implement-a-managed-mi-client">How to Implement a Managed MI Client</a> and <a href="/previous-versions/windows/desktop/wmi_v2/how-to-implement-a-native-mi-client">How to Implement a Native MI Client</a>.</span></span></p>
<div class="code">
<span data-codelanguage="CSharp"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="15dc1-126">C#</span><span class="sxs-lookup"><span data-stu-id="15dc1-126">C#</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>using Microsoft.Management.Infrastructure;
...
CimSession session = CimSession.Create(&quot;localHost&quot;);
IEnumerable<CimInstance> queryInstance = session.QueryInstances(@&quot;root\cimv2&quot;, &quot;WQL&quot;, &quot;SELECT * FROM Win32_ComputerSystem&quot;);

foreach (CimInstance cimObj in queryInstance)
{
   Console.WriteLine(cimObj.CimInstanceProperties[&quot;Name&quot;].ToString());
}</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="15dc1-127"><span id="Creating_a_client_with_C___System.Management_"></span><span id="creating_a_client_with_c___system.management_"></span><span id="CREATING_A_CLIENT_WITH_C___SYSTEM.MANAGEMENT_"></span>Создание клиента с помощью C# (<a href="/dotnet/api/system.management">System. Management</a>)</span><span class="sxs-lookup"><span data-stu-id="15dc1-127"><span id="Creating_a_client_with_C___System.Management_"></span><span id="creating_a_client_with_c___system.management_"></span><span id="CREATING_A_CLIENT_WITH_C___SYSTEM.MANAGEMENT_"></span>Creating a client with C# (<a href="/dotnet/api/system.management">System.Management</a>)</span></span></p></td>
<td><p><span data-ttu-id="15dc1-128">Это пространство имен содержит исходное решение для доступа к инструментарию WMI с управляемым кодом.</span><span class="sxs-lookup"><span data-stu-id="15dc1-128">This namespace contains the original solution for accessing WMI with managed code.</span></span> <span data-ttu-id="15dc1-129">Хотя классы <a href="/dotnet/api/system.management">System.</a> Management по-прежнему доступны, классы <a href="/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)">Microsoft. Management. Infrastructure</a> , как правило, более эффективны и масштабируются лучше.</span><span class="sxs-lookup"><span data-stu-id="15dc1-129">While the <a href="/dotnet/api/system.management">System.Management</a> classes are still available, the <a href="/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)">Microsoft.Management.Infrastructure</a> classes are generally more efficient and scale better.</span></span> <span data-ttu-id="15dc1-130">Поэтому рекомендуется использовать классы MI, а не исходные классы WMI.</span><span class="sxs-lookup"><span data-stu-id="15dc1-130">As such, it is recommended that you use the MI classes, rather than the original WMI classes.</span></span></p>
<div class="code">
<span data-codelanguage="CSharp"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="15dc1-131">C#</span><span class="sxs-lookup"><span data-stu-id="15dc1-131">C#</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>using Microsoft.Management.Infrastructure;
...
CimSession session = CimSession.Create(&quot;localHost&quot;);
IEnumerable<CimInstance> queryInstance = session.QueryInstances(@&quot;root\cimv2&quot;, &quot;WQL&quot;, &quot;SELECT * FROM Win32_ComputerSystem&quot;);

foreach (CimInstance cimObj in queryInstance)
{
   Console.WriteLine(cimObj.CimInstanceProperties[&quot;Name&quot;].ToString());
}</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="15dc1-132">В следующей таблице приводится список подразделов этого раздела.</span><span class="sxs-lookup"><span data-stu-id="15dc1-132">The following table lists the topics covered in this section.</span></span>



| <span data-ttu-id="15dc1-133">Раздел</span><span class="sxs-lookup"><span data-stu-id="15dc1-133">Topic</span></span>                                                                                                        | <span data-ttu-id="15dc1-134">Описание</span><span class="sxs-lookup"><span data-stu-id="15dc1-134">Description</span></span>                                                                                                                                                                                    |
|--------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="15dc1-135">Подключение к инструментарию WMI на удаленном компьютере</span><span class="sxs-lookup"><span data-stu-id="15dc1-135">Connecting to WMI on a Remote Computer</span></span>](connecting-to-wmi-on-a-remote-computer.md)                         | <span data-ttu-id="15dc1-136">Описывает ряд проблем, возникающих, когда клиенты используют инфраструктуру WMI на удаленном компьютере.</span><span class="sxs-lookup"><span data-stu-id="15dc1-136">Describes a number of issues that arise when clients use the WMI infrastructure on a remote computer.</span></span>                                                                                          |
| [<span data-ttu-id="15dc1-137">Задачи WMI для скриптов и приложений</span><span class="sxs-lookup"><span data-stu-id="15dc1-137">WMI Tasks for Scripts and Applications</span></span>](wmi-tasks-for-scripts-and-applications.md)                         | <span data-ttu-id="15dc1-138">Показывает пример кода клиента WMI.</span><span class="sxs-lookup"><span data-stu-id="15dc1-138">Shows example WMI client code.</span></span>                                                                                                                                                                 |
| [<span data-ttu-id="15dc1-139">Создание приложения или скрипта WMI</span><span class="sxs-lookup"><span data-stu-id="15dc1-139">Creating a WMI Application or Script</span></span>](creating-a-wmi-application-or-script.md)                             | <span data-ttu-id="15dc1-140">Содержит сведения о создании различных клиентов WMI.</span><span class="sxs-lookup"><span data-stu-id="15dc1-140">Provides information about creating various WMI clients.</span></span>                                                                                                                                       |
| [<span data-ttu-id="15dc1-141">Мониторинг данных производительности</span><span class="sxs-lookup"><span data-stu-id="15dc1-141">Monitoring Performance Data</span></span>](monitoring-performance-data.md)                                               | <span data-ttu-id="15dc1-142">Описывает использование инструментария WMI для мониторинга данных производительности.</span><span class="sxs-lookup"><span data-stu-id="15dc1-142">Describes how to use WMI to monitor performance data.</span></span>                                                                                                                                          |
| [<span data-ttu-id="15dc1-143">Получение события WMI</span><span class="sxs-lookup"><span data-stu-id="15dc1-143">Receiving a WMI Event</span></span>](receiving-a-wmi-event.md)                                                           | <span data-ttu-id="15dc1-144">Описывает, как просматривать события WMI.</span><span class="sxs-lookup"><span data-stu-id="15dc1-144">Describes how to view WMI events.</span></span>                                                                                                                                                              |
| [<span data-ttu-id="15dc1-145">Мониторинг событий</span><span class="sxs-lookup"><span data-stu-id="15dc1-145">Monitoring Events</span></span>](monitoring-events.md)                                                                   | <span data-ttu-id="15dc1-146">Описывает, как отслеживать события WMI.</span><span class="sxs-lookup"><span data-stu-id="15dc1-146">Describes how to monitor WMI events.</span></span>                                                                                                                                                           |
| [<span data-ttu-id="15dc1-147">Запросы с помощью WQL</span><span class="sxs-lookup"><span data-stu-id="15dc1-147">Querying with WQL</span></span>](querying-with-wql.md)                                                                   | <span data-ttu-id="15dc1-148">Вводит язык запросов WMI (WQL).</span><span class="sxs-lookup"><span data-stu-id="15dc1-148">Introduces the WMI Query Language (WQL).</span></span>                                                                                                                                                       |
| [<span data-ttu-id="15dc1-149">Запрос состояния дополнительных функций</span><span class="sxs-lookup"><span data-stu-id="15dc1-149">Querying the Status of Optional Features</span></span>](querying-the-status-of-optional-features.md)                     | <span data-ttu-id="15dc1-150">В Windows 7 WMI реализовала класс [**Win32 \_ оптионалфеатуре**](/windows/desktop/CIMWin32Prov/win32-optionalfeature) .</span><span class="sxs-lookup"><span data-stu-id="15dc1-150">In Windows 7, WMI implemented the [**Win32\_OptionalFeature**](/windows/desktop/CIMWin32Prov/win32-optionalfeature) class.</span></span> <span data-ttu-id="15dc1-151">Этот класс получает состояние дополнительных компонентов, имеющихся на компьютере.</span><span class="sxs-lookup"><span data-stu-id="15dc1-151">This class retrieves the status of the optional features that are present on a computer.</span></span> |
| [<span data-ttu-id="15dc1-152">Описание расположения объекта WMI</span><span class="sxs-lookup"><span data-stu-id="15dc1-152">Describing the Location of a WMI Object</span></span>](describing-the-location-of-a-wmi-object.md)                       | <span data-ttu-id="15dc1-153">Основное внимание уделяется синтаксису, описывающему расположение управляемого объекта WMI.</span><span class="sxs-lookup"><span data-stu-id="15dc1-153">Focuses on the syntax for describing the location of a WMI managed entity.</span></span>                                                                                                                     |
| [<span data-ttu-id="15dc1-154">Доступ к другим функциям операционной системы с помощью инструментария WMI</span><span class="sxs-lookup"><span data-stu-id="15dc1-154">Accessing Other Operating System Features with WMI</span></span>](accessing-other-operating-system-features-with-wmi.md) | <span data-ttu-id="15dc1-155">Описание процесса записи клиентов WMI, обращающихся к драйверам устройств, Active Directory и SNMP-устройствам.</span><span class="sxs-lookup"><span data-stu-id="15dc1-155">Describes how to write WMI clients that access device drivers, Active Directory, and SNMP devices.</span></span>                                                                                             |
| [<span data-ttu-id="15dc1-156">Доступ к данным в пространстве имен Interop</span><span class="sxs-lookup"><span data-stu-id="15dc1-156">Accessing Data in the Interop Namespace</span></span>](accessing-data-in-the-interop-namespace.md)                       | <span data-ttu-id="15dc1-157">Поставщики ассоциаций позволяют клиентам инструментарий управления Windows (WMI) (WMI) просматривать и получать профили и связанные экземпляры классов из разных пространств имен.</span><span class="sxs-lookup"><span data-stu-id="15dc1-157">Association providers enable Windows Management Instrumentation (WMI) clients to traverse and retrieve profiles and associated class instances from different namespaces.</span></span>                      |
| [<span data-ttu-id="15dc1-158">Управление сведениями о классе и экземпляре</span><span class="sxs-lookup"><span data-stu-id="15dc1-158">Manipulating Class and Instance Information</span></span>](manipulating-class-and-instance-information.md)               | <span data-ttu-id="15dc1-159">Описывает общие задачи, которые должны выполняться клиентами WMI.</span><span class="sxs-lookup"><span data-stu-id="15dc1-159">Describes the common tasks that WMI clients must perform.</span></span>                                                                                                                                      |
| [<span data-ttu-id="15dc1-160">Совместное связывание классов</span><span class="sxs-lookup"><span data-stu-id="15dc1-160">Linking Classes Together</span></span>](linking-classes-together.md)                                                     | <span data-ttu-id="15dc1-161">Обсуждается поставщик представления и его использование для объединения информации из нескольких классов WMI.</span><span class="sxs-lookup"><span data-stu-id="15dc1-161">Discusses the view provider and how it can be used to bring together information from multiple WMI classes.</span></span>                                                                                    |
| [<span data-ttu-id="15dc1-162">Изменение системного реестра</span><span class="sxs-lookup"><span data-stu-id="15dc1-162">Modifying the System Registry</span></span>](modifying-the-system-registry.md)                                           | <span data-ttu-id="15dc1-163">Описывает, как клиенты WMI могут использовать инструментарий WMI для управления данными системного реестра.</span><span class="sxs-lookup"><span data-stu-id="15dc1-163">Describes how WMI clients can use WMI to manage system registry information.</span></span>                                                                                                                   |



 

