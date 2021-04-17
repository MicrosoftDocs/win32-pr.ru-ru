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
# <a name="wmi-tasks-operating-systems"></a>Задачи WMI: операционные системы

Задачи WMI для операционных систем получают сведения об операционной системе, такие как версия, активирована или какие исправления установлены.

Примеры сценариев, приведенные в этом разделе, получают данные только с локального компьютера. Дополнительные сведения об использовании сценария для получения данных с удаленных компьютеров см. в разделе [Подключение к WMI на удаленном компьютере](connecting-to-wmi-on-a-remote-computer.md).


В следующей процедуре описывается выполнение скрипта.

**Запуск сценария**

1.  Скопируйте код и сохраните его в файле с расширением vbs, например *filename.vbs*. Убедитесь, что текстовый редактор не добавляет расширение txt в файл.
2.  Откройте окно командной строки и перейдите в каталог, в котором был сохранен файл.
3.  Введите **CScript filename.vbs** в командной строке.
4.  Если доступ к журналу событий невозможен, проверьте, выполняется ли в командной строке с повышенными привилегиями. Некоторые журналы событий, например журнал событий безопасности, могут быть защищены с помощью элементов управления доступом пользователей (UAC).

> [!Note]  
> По умолчанию CScript отображает выходные данные скрипта в окне командной строки. Поскольку сценарии WMI могут создавать большие объемы выходных данных, может потребоваться перенаправить выходные данные в файл. Введите **cscript filename.vbs > outfile.txt** в командной строке, чтобы перенаправить выходные данные скрипта *filename.vbs* в *outfile.txt*.

 

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
<td>... определить, установлен ли на компьютере пакет обновления?</td>
<td>Используйте класс <a href="/windows/desktop/CIMWin32Prov/win32-operatingsystem"><strong>Win32_OperatingSystem</strong></a> и проверьте значения свойств <strong>сервицепаккмажорверсион</strong> и <strong>сервицепаккминорверсион</strong> .<br/> <span data-codelanguage="VisualBasic"></span>
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
<th>PowerShell</th>
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
<td>... определить, когда операционная система была установлена на компьютере?</td>
<td><p>Используйте класс <a href="/windows/desktop/CIMWin32Prov/win32-operatingsystem"><strong>Win32_OperatingSystem</strong></a> и свойство <strong>инсталлдате</strong> .</p>
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
<th>PowerShell</th>
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
<td>... определить, какая версия операционной системы Windows установлена на компьютере?</td>
<td><p>Используйте класс <a href="/windows/desktop/CIMWin32Prov/win32-operatingsystem"><strong>Win32_OperatingSystem</strong></a> и получите свойства <strong>имени</strong> и <strong>версии</strong> .</p>
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
<th>PowerShell</th>
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
<td>... определение папки, в которой находится папка Windows (% windir%) на компьютере?</td>
<td><p>Используйте класс <a href="/windows/desktop/CIMWin32Prov/win32-operatingsystem"><strong>Win32_OperatingSystem</strong></a> и проверьте значение свойства <strong>виндовсдиректори</strong> .</p>
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
<th>PowerShell</th>
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
<td>... определить, какие исправления установлены на компьютере?</td>
<td><p>Используйте класс <a href="/windows/desktop/CIMWin32Prov/win32-quickfixengineering"><strong>Win32_QuickFixEngineering</strong></a> .</p>
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
<th>PowerShell</th>
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
<td>... определить, нужно ли активировать операционную систему на компьютере?</td>
<td><p>Используйте класс <a href="/previous-versions/windows/desktop/legacy/aa394520(v=vs.85)"><strong>Win32_WindowsProductActivation</strong></a> и проверьте значение свойства <strong>активатионрекуиред</strong> .</p>
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
<th>PowerShell</th>
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



 

## <a name="related-topics"></a>См. также

<dl> <dt>

[Задачи WMI для скриптов и приложений](wmi-tasks-for-scripts-and-applications.md)
</dt> <dt>

[Примеры приложений WMI на C++](wmi-c---application-examples.md)
</dt> <dt>

[Скриптцентер TechNet](https://www.microsoft.com/technet/scriptcenter)
</dt> </dl>

 

