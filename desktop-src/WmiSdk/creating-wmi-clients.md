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
# <a name="creating-wmi-clients"></a>Создание клиентов WMI

Инструментарий WMI предоставляет стандартизированную инфраструктуру управления системой, которую можно использовать с помощью нескольких различных клиентов. Эти клиенты находятся в диапазоне от wmic.exe программы командной строки до System Center Operations Manager. Вы можете создавать собственные клиенты WMI с помощью API сценариев WMI, собственного API C++ или с помощью типов в пространстве имен библиотеки классов System. Management платформа .NET Framework.

## <a name="how-to-create-a-wmi-client"></a>Создание клиента WMI

Основные функциональные возможности WMI состоят из извлечения объектов из репозитория WMI и изучения свойств этих объектов. Можно также обновить эти свойства или вызвать методы для этих свойств. В следующих примерах показано, как выполнить базовую задачу администрирования WMI: получение имени локального компьютера.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Термин</th>
<th>Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="Creating_a_client_with_PowerShell"></span><span id="creating_a_client_with_powershell"></span><span id="CREATING_A_CLIENT_WITH_POWERSHELL"></span>Создание клиента с помощью PowerShell<br/></td>
<td>WMI и PowerShell тесно интегрированы; Таким образом, получение объектов WMI с помощью PowerShell — это просто вопрос вызова командлета Get-WmiObject. Обратите внимание, что для обеспечения согласованности в первом фрагменте кода явно указано множество значений по умолчанию. во втором предполагается, что значения по умолчанию верны.<br/> <span data-codelanguage="PowerShell"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>PowerShell</th>
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
<td><p><span id="Creating_a_client_with_VBScript"></span><span id="creating_a_client_with_vbscript"></span><span id="CREATING_A_CLIENT_WITH_VBSCRIPT"></span>Создание клиента с помощью VBScript</p></td>
<td><p>VBScript был исходным языком сценариев, который часто использовался в WMI. Хотя PowerShell стал более популярным, многие из существующих примеров кода в этой документации написаны на языке VBScript. Обратите внимание, что в этом образце VBScript явным образом указывается как путь к локальному компьютеру, так и уровень олицетворения. Это не является обязательным, но часто рекомендуется.</p>
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
<td><p><span id="Creating_a_client_with_C___Microsoft.Management.Infrastructure_"></span><span id="creating_a_client_with_c___microsoft.management.infrastructure_"></span><span id="CREATING_A_CLIENT_WITH_C___MICROSOFT.MANAGEMENT.INFRASTRUCTURE_"></span>Создание клиента с помощью C# (<a href="/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)">Microsoft. Management. Infrastructure</a>)</p></td>
<td><p>Это пространство имен содержит текущее решение для доступа к инструментарию WMI с управляемым кодом и называется инфраструктурой управления Windows (MI или WMI). В настоящее время MI — это поддерживаемая технология для создания управляемых клиентов управления. Дополнительные сведения см. <a href="/previous-versions/windows/desktop/wmi_v2/how-to-implement-a-managed-mi-client">в разделе Реализация управляемого клиента MI</a> и <a href="/previous-versions/windows/desktop/wmi_v2/how-to-implement-a-native-mi-client">реализация собственного клиента MI</a>.</p>
<div class="code">
<span data-codelanguage="CSharp"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>C#</th>
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
<td><p><span id="Creating_a_client_with_C___System.Management_"></span><span id="creating_a_client_with_c___system.management_"></span><span id="CREATING_A_CLIENT_WITH_C___SYSTEM.MANAGEMENT_"></span>Создание клиента с помощью C# (<a href="/dotnet/api/system.management">System. Management</a>)</p></td>
<td><p>Это пространство имен содержит исходное решение для доступа к инструментарию WMI с управляемым кодом. Хотя классы <a href="/dotnet/api/system.management">System.</a> Management по-прежнему доступны, классы <a href="/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)">Microsoft. Management. Infrastructure</a> , как правило, более эффективны и масштабируются лучше. Поэтому рекомендуется использовать классы MI, а не исходные классы WMI.</p>
<div class="code">
<span data-codelanguage="CSharp"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>C#</th>
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



 

В следующей таблице приводится список подразделов этого раздела.



| Раздел                                                                                                        | Описание                                                                                                                                                                                    |
|--------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Подключение к инструментарию WMI на удаленном компьютере](connecting-to-wmi-on-a-remote-computer.md)                         | Описывает ряд проблем, возникающих, когда клиенты используют инфраструктуру WMI на удаленном компьютере.                                                                                          |
| [Задачи WMI для скриптов и приложений](wmi-tasks-for-scripts-and-applications.md)                         | Показывает пример кода клиента WMI.                                                                                                                                                                 |
| [Создание приложения или скрипта WMI](creating-a-wmi-application-or-script.md)                             | Содержит сведения о создании различных клиентов WMI.                                                                                                                                       |
| [Мониторинг данных производительности](monitoring-performance-data.md)                                               | Описывает использование инструментария WMI для мониторинга данных производительности.                                                                                                                                          |
| [Получение события WMI](receiving-a-wmi-event.md)                                                           | Описывает, как просматривать события WMI.                                                                                                                                                              |
| [Мониторинг событий](monitoring-events.md)                                                                   | Описывает, как отслеживать события WMI.                                                                                                                                                           |
| [Запросы с помощью WQL](querying-with-wql.md)                                                                   | Вводит язык запросов WMI (WQL).                                                                                                                                                       |
| [Запрос состояния дополнительных функций](querying-the-status-of-optional-features.md)                     | В Windows 7 WMI реализовала класс [**Win32 \_ оптионалфеатуре**](/windows/desktop/CIMWin32Prov/win32-optionalfeature) . Этот класс получает состояние дополнительных компонентов, имеющихся на компьютере. |
| [Описание расположения объекта WMI](describing-the-location-of-a-wmi-object.md)                       | Основное внимание уделяется синтаксису, описывающему расположение управляемого объекта WMI.                                                                                                                     |
| [Доступ к другим функциям операционной системы с помощью инструментария WMI](accessing-other-operating-system-features-with-wmi.md) | Описание процесса записи клиентов WMI, обращающихся к драйверам устройств, Active Directory и SNMP-устройствам.                                                                                             |
| [Доступ к данным в пространстве имен Interop](accessing-data-in-the-interop-namespace.md)                       | Поставщики ассоциаций позволяют клиентам инструментарий управления Windows (WMI) (WMI) просматривать и получать профили и связанные экземпляры классов из разных пространств имен.                      |
| [Управление сведениями о классе и экземпляре](manipulating-class-and-instance-information.md)               | Описывает общие задачи, которые должны выполняться клиентами WMI.                                                                                                                                      |
| [Совместное связывание классов](linking-classes-together.md)                                                     | Обсуждается поставщик представления и его использование для объединения информации из нескольких классов WMI.                                                                                    |
| [Изменение системного реестра](modifying-the-system-registry.md)                                           | Описывает, как клиенты WMI могут использовать инструментарий WMI для управления данными системного реестра.                                                                                                                   |



 

