---
description: Задачи WMI для принтеров и печати управления и получения данных о принтерах, таких как поиск или установка принтера по умолчанию. Другие примеры см. в разделе TechNet Скриптцентер по адресу https://www.microsoft.com/technet .
ms.assetid: 56aa8043-08cc-42c9-82b0-f1328cd52ff8
ms.tgt_platform: multiple
title: 'Задачи WMI: принтеры и печать'
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2f6e580b299e32e2c003c084fb771a28e5984f7e
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2021
ms.locfileid: "122625580"
---
# <a name="wmi-tasks-printers-and-printing"></a>Задачи WMI: принтеры и печать

Задачи WMI для принтеров и печати управления и получения данных о принтерах, таких как поиск или установка принтера по умолчанию. Другие примеры см. в разделе TechNet Скриптцентер по адресу [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx) .

Примеры сценариев, приведенные в этом разделе, получают данные только с локального компьютера. Дополнительные сведения об использовании сценария для получения данных с удаленных компьютеров см. в разделе [Подключение к WMI на удаленном компьютере](connecting-to-wmi-on-a-remote-computer.md).


В следующей процедуре описывается выполнение скрипта.

**Запуск сценария**

1.  Скопируйте код и сохраните его в файле с расширением vbs, например *filename.vbs*. Убедитесь, что текстовый редактор не добавляет к файлу расширение .txt.
2.  Откройте окно командной строки и перейдите в каталог, в котором был сохранен файл.
3.  Введите **cscript filename.vbs** в командной строке.
4.  Если доступ к журналу событий невозможен, проверьте, выполняется ли в командной строке с повышенными привилегиями. Некоторые журналы событий, например журнал событий безопасности, могут быть защищены с помощью элементов управления доступом пользователей (UAC).

> [!Note]  
> По умолчанию Cscript отображает выходные данные скрипта в окне командной строки. Поскольку сценарии WMI могут создавать большие объемы выходных данных, может потребоваться перенаправить выходные данные в файл. Введите **cscript filename.vbs > outfile.txt** в командной строке, чтобы перенаправить выходные данные скрипта *filename.vbs* в *outfile.txt*.

 

В следующей таблице перечислены примеры сценариев, которые можно использовать для получения различных типов данных с локального компьютера.



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Часто выполняемые действия в новом интерфейсе</th>
<th>Классы или методы WMI</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>... Добавить новое подключение к принтеру на удаленном компьютере?</td>
<td>Используйте класс <a href="/windows/desktop/CIMWin32Prov/win32-printer"><strong>Win32_Printer</strong></a> и метод <a href="/windows/desktop/CIMWin32Prov/addprinterconnection-method-in-class-win32-printer"><strong>аддпринтерконнектион</strong></a> .<br/> <span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col  />
</colgroup>
<thead>
<tr class="header">
<th>VB</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;atl-ws-01&quot;
Set objWMIService = GetObject( &quot;winmgmts:{impersonationLevel=Impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set objPrinter = objWMIService.Get(&quot;Win32_Printer&quot;)
errReturn = objPrinter.AddPrinterConnection (&quot;\\PrintServer1\ArtDepartmentPrinter&quot;)</code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr class="even">
<td>... задать принтер по умолчанию?</td>
<td><p>Используйте класс <a href="/windows/desktop/CIMWin32Prov/win32-printer"><strong>Win32_Printer</strong></a> и метод <a href="/windows/desktop/CIMWin32Prov/setdefaultprinter-method-in-class-win32-printer"><strong>SetDefaultPrinter</strong></a> .</p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col  />
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
Set colInstalledPrinters =  objWMIService.ExecQuery (&quot;Select * from Win32_Printer Where Name = &#39;ScriptedPrinter&#39;&quot;)
For Each objPrinter in colInstalledPrinters
    objPrinter.SetDefaultPrinter()
Next</code></pre></td>
</tr>
</tbody>
</table>
<span data-codelanguage="PowerShell"></span>
<table>
<colgroup>
<col  />
</colgroup>
<thead>
<tr class="header">
<th>PowerShell</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$printerName = &quot;\\ServerName\ShareName&quot;
$printer = get-wmiObject -class win32_printer -Namespace $namespace | Where-Object { $_.Name -eq $printerName }
[void]$printer.setDefaultPrinter()</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td>... отменить задания печати с помощью инструментария WMI?</td>
<td><p>Используйте класс <a href="/windows/desktop/CIMWin32Prov/win32-printer"><strong>Win32_Printer</strong></a> и метод <a href="/windows/desktop/CIMWin32Prov/cancelalljobs-method-in-class-win32-printer"><strong>канцелаллжобс</strong></a> .</p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col  />
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
Set colPrintJobs =  objWMIService.ExecQuery (&quot;Select * from Win32_Printer&quot;)
For Each objPrintJob in colPrintJobs 
    objPrintJob.CancelAllJobs
Next</code></pre></td>
</tr>
</tbody>
</table>
<span data-codelanguage="PowerShell"></span>
<table>
<colgroup>
<col  />
</colgroup>
<thead>
<tr class="header">
<th>PowerShell</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$result = (get-wmiObject -class win32_printer -Namespace &quot;root\cimv2&quot;).CancelAllJobs()</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td>... определить принтер по умолчанию для компьютера?</td>
<td><p>Используйте класс <a href="/windows/desktop/CIMWin32Prov/win32-printer"><strong>Win32_Printer</strong></a> и проверьте, имеет ли свойство <strong>по умолчанию</strong> <strong>значение true</strong>.</p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col  />
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
Set colInstalledPrinters =  objWMIService.ExecQuery (&quot;Select * from Win32_Printer Where Default = True&quot;)
For Each objPrinter in colInstalledPrinters
    Wscript.Echo objPrinter.Name
Next</code></pre></td>
</tr>
</tbody>
</table>
<span data-codelanguage="PowerShell"></span>
<table>
<colgroup>
<col  />
</colgroup>
<thead>
<tr class="header">
<th>PowerShell</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>get-wmiObject -class win32_printer -Namespace &quot;root\cimv2&quot; | where-object { $_.Default -eq &#39;True&#39; }</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Задачи WMI для скриптов и приложений](wmi-tasks-for-scripts-and-applications.md)
</dt> <dt>

[Примеры приложений WMI на C++](wmi-c---application-examples.md)
</dt> <dt>

[Скриптцентер TechNet](https://www.microsoft.com/technet/scriptcenter)
</dt> </dl>

 

