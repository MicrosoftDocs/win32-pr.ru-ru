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
ms.openlocfilehash: 3d6a2ec1693a62b16e7b147cbbdf362eadb6dd79
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348862"
---
# <a name="wmi-tasks-printers-and-printing"></a><span data-ttu-id="9e870-104">Задачи WMI: принтеры и печать</span><span class="sxs-lookup"><span data-stu-id="9e870-104">WMI Tasks: Printers and Printing</span></span>

<span data-ttu-id="9e870-105">Задачи WMI для принтеров и печати управления и получения данных о принтерах, таких как поиск или установка принтера по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="9e870-105">WMI tasks for printers and printing manage and obtain data about printers, such as finding or setting the default printer.</span></span> <span data-ttu-id="9e870-106">Другие примеры см. в разделе TechNet Скриптцентер по адресу [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx) .</span><span class="sxs-lookup"><span data-stu-id="9e870-106">For other examples, see the TechNet ScriptCenter at [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx).</span></span>

<span data-ttu-id="9e870-107">Примеры сценариев, приведенные в этом разделе, получают данные только с локального компьютера.</span><span class="sxs-lookup"><span data-stu-id="9e870-107">The script examples shown in this topic obtain data only from the local computer.</span></span> <span data-ttu-id="9e870-108">Дополнительные сведения об использовании сценария для получения данных с удаленных компьютеров см. в разделе [Подключение к WMI на удаленном компьютере](connecting-to-wmi-on-a-remote-computer.md).</span><span class="sxs-lookup"><span data-stu-id="9e870-108">For more information about how to use the script to obtain data from remote computers, see [Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span></span>


<span data-ttu-id="9e870-109">В следующей процедуре описывается выполнение скрипта.</span><span class="sxs-lookup"><span data-stu-id="9e870-109">The following procedure describes how to run a script.</span></span>

<span data-ttu-id="9e870-110">**Запуск сценария**</span><span class="sxs-lookup"><span data-stu-id="9e870-110">**To run a script**</span></span>

1.  <span data-ttu-id="9e870-111">Скопируйте код и сохраните его в файле с расширением vbs, например *filename.vbs*.</span><span class="sxs-lookup"><span data-stu-id="9e870-111">Copy the code and save it in a file with a .vbs extension, such as *filename.vbs*.</span></span> <span data-ttu-id="9e870-112">Убедитесь, что текстовый редактор не добавляет расширение txt в файл.</span><span class="sxs-lookup"><span data-stu-id="9e870-112">Ensure that your text editor does not add a .txt extension to the file.</span></span>
2.  <span data-ttu-id="9e870-113">Откройте окно командной строки и перейдите в каталог, в котором был сохранен файл.</span><span class="sxs-lookup"><span data-stu-id="9e870-113">Open a command prompt window and navigate to the directory where you saved the file.</span></span>
3.  <span data-ttu-id="9e870-114">Введите **cscript filename.vbs** в командной строке.</span><span class="sxs-lookup"><span data-stu-id="9e870-114">Type **cscript filename.vbs** at the command prompt.</span></span>
4.  <span data-ttu-id="9e870-115">Если доступ к журналу событий невозможен, проверьте, выполняется ли в командной строке с повышенными привилегиями.</span><span class="sxs-lookup"><span data-stu-id="9e870-115">If you cannot access an event log, check to see if you are running from an Elevated command prompt.</span></span> <span data-ttu-id="9e870-116">Некоторые журналы событий, например журнал событий безопасности, могут быть защищены с помощью элементов управления доступом пользователей (UAC).</span><span class="sxs-lookup"><span data-stu-id="9e870-116">Some Event Log, such as the Security Event Log, may be protected by User Access Controls (UAC).</span></span>

> [!Note]  
> <span data-ttu-id="9e870-117">По умолчанию Cscript отображает выходные данные скрипта в окне командной строки.</span><span class="sxs-lookup"><span data-stu-id="9e870-117">By default, cscript displays the output of a script in the command prompt window.</span></span> <span data-ttu-id="9e870-118">Поскольку сценарии WMI могут создавать большие объемы выходных данных, может потребоваться перенаправить выходные данные в файл.</span><span class="sxs-lookup"><span data-stu-id="9e870-118">Because WMI scripts can produce large amounts of output, you might want to redirect the output to a file.</span></span> <span data-ttu-id="9e870-119">Введите **cscript filename.vbs > outfile.txt** в командной строке, чтобы перенаправить выходные данные скрипта *filename.vbs* в *outfile.txt*.</span><span class="sxs-lookup"><span data-stu-id="9e870-119">Type **cscript filename.vbs > outfile.txt** at the command prompt to redirect the output of the *filename.vbs* script to *outfile.txt*.</span></span>

 

<span data-ttu-id="9e870-120">В следующей таблице перечислены примеры сценариев, которые можно использовать для получения различных типов данных с локального компьютера.</span><span class="sxs-lookup"><span data-stu-id="9e870-120">The following table lists script examples that can be used to obtain various types of data from the local computer.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9e870-121">Часто выполняемые действия в новом интерфейсе</span><span class="sxs-lookup"><span data-stu-id="9e870-121">How do I...</span></span></th>
<th><span data-ttu-id="9e870-122">Классы или методы WMI</span><span class="sxs-lookup"><span data-stu-id="9e870-122">WMI classes or methods</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9e870-123">... Добавить новое подключение к принтеру на удаленном компьютере?</span><span class="sxs-lookup"><span data-stu-id="9e870-123">...add a new printer connection to a remote computer?</span></span></td>
<td><span data-ttu-id="9e870-124">Используйте класс <a href="/windows/desktop/CIMWin32Prov/win32-printer"><strong>Win32_Printer</strong></a> и метод <a href="/windows/desktop/CIMWin32Prov/addprinterconnection-method-in-class-win32-printer"><strong>аддпринтерконнектион</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="9e870-124">Use the <a href="/windows/desktop/CIMWin32Prov/win32-printer"><strong>Win32_Printer</strong></a> class and the <a href="/windows/desktop/CIMWin32Prov/addprinterconnection-method-in-class-win32-printer"><strong>AddPrinterConnection</strong></a> method.</span></span><br/> <span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9e870-125">VB</span><span class="sxs-lookup"><span data-stu-id="9e870-125">VB</span></span></th>
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
<td><span data-ttu-id="9e870-126">... задать принтер по умолчанию?</span><span class="sxs-lookup"><span data-stu-id="9e870-126">...set the default printer?</span></span></td>
<td><p><span data-ttu-id="9e870-127">Используйте класс <a href="/windows/desktop/CIMWin32Prov/win32-printer"><strong>Win32_Printer</strong></a> и метод <a href="/windows/desktop/CIMWin32Prov/setdefaultprinter-method-in-class-win32-printer"><strong>SetDefaultPrinter</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="9e870-127">Use the <a href="/windows/desktop/CIMWin32Prov/win32-printer"><strong>Win32_Printer</strong></a> class and the <a href="/windows/desktop/CIMWin32Prov/setdefaultprinter-method-in-class-win32-printer"><strong>SetDefaultPrinter</strong></a> method.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9e870-128">VB</span><span class="sxs-lookup"><span data-stu-id="9e870-128">VB</span></span></th>
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
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9e870-129">PowerShell</span><span class="sxs-lookup"><span data-stu-id="9e870-129">PowerShell</span></span></th>
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
<td><span data-ttu-id="9e870-130">... отменить задания печати с помощью инструментария WMI?</span><span class="sxs-lookup"><span data-stu-id="9e870-130">...cancel print jobs using WMI?</span></span></td>
<td><p><span data-ttu-id="9e870-131">Используйте класс <a href="/windows/desktop/CIMWin32Prov/win32-printer"><strong>Win32_Printer</strong></a> и метод <a href="/windows/desktop/CIMWin32Prov/cancelalljobs-method-in-class-win32-printer"><strong>канцелаллжобс</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="9e870-131">Use the <a href="/windows/desktop/CIMWin32Prov/win32-printer"><strong>Win32_Printer</strong></a> class, and the <a href="/windows/desktop/CIMWin32Prov/cancelalljobs-method-in-class-win32-printer"><strong>CancelAllJobs</strong></a> method.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9e870-132">VB</span><span class="sxs-lookup"><span data-stu-id="9e870-132">VB</span></span></th>
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
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9e870-133">PowerShell</span><span class="sxs-lookup"><span data-stu-id="9e870-133">PowerShell</span></span></th>
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
<td><span data-ttu-id="9e870-134">... определить принтер по умолчанию для компьютера?</span><span class="sxs-lookup"><span data-stu-id="9e870-134">...determine the default printer for a computer?</span></span></td>
<td><p><span data-ttu-id="9e870-135">Используйте класс <a href="/windows/desktop/CIMWin32Prov/win32-printer"><strong>Win32_Printer</strong></a> и проверьте, имеет ли свойство <strong>по умолчанию</strong> <strong>значение true</strong>.</span><span class="sxs-lookup"><span data-stu-id="9e870-135">Use the <a href="/windows/desktop/CIMWin32Prov/win32-printer"><strong>Win32_Printer</strong></a> class, and check whether the <strong>Default</strong> property is <strong>True</strong>.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9e870-136">VB</span><span class="sxs-lookup"><span data-stu-id="9e870-136">VB</span></span></th>
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
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9e870-137">PowerShell</span><span class="sxs-lookup"><span data-stu-id="9e870-137">PowerShell</span></span></th>
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



 

## <a name="related-topics"></a><span data-ttu-id="9e870-138">См. также</span><span class="sxs-lookup"><span data-stu-id="9e870-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9e870-139">Задачи WMI для скриптов и приложений</span><span class="sxs-lookup"><span data-stu-id="9e870-139">WMI Tasks for Scripts and Applications</span></span>](wmi-tasks-for-scripts-and-applications.md)
</dt> <dt>

[<span data-ttu-id="9e870-140">Примеры приложений WMI на C++</span><span class="sxs-lookup"><span data-stu-id="9e870-140">WMI C++ Application Examples</span></span>](wmi-c---application-examples.md)
</dt> <dt>

[<span data-ttu-id="9e870-141">Скриптцентер TechNet</span><span class="sxs-lookup"><span data-stu-id="9e870-141">TechNet ScriptCenter</span></span>](https://www.microsoft.com/technet/scriptcenter)
</dt> </dl>

 

