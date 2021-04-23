---
description: Задачи WMI для файлов и папок изменяют свойства файла или папки с помощью WMI, включая создание общего ресурса или переименование файла.
ms.assetid: 91281fe1-0461-48da-ac5c-cab7e8e1b285
ms.tgt_platform: multiple
title: 'Задачи WMI: файлы и папки'
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b24d5f7708b88507cd08b73c0b08a83c94f6bb28
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712889"
---
# <a name="wmi-tasks-files-and-folders"></a><span data-ttu-id="c368b-103">Задачи WMI: файлы и папки</span><span class="sxs-lookup"><span data-stu-id="c368b-103">WMI Tasks: Files and Folders</span></span>

<span data-ttu-id="c368b-104">Задачи WMI для файлов и папок изменяют свойства файла или папки с помощью WMI, включая создание общего ресурса или переименование файла.</span><span class="sxs-lookup"><span data-stu-id="c368b-104">WMI tasks for files and folders change file or folder properties through WMI, including creating a share or renaming a file.</span></span> <span data-ttu-id="c368b-105">Чтобы скопировать файл или выполнить чтение и запись файла, проще всего использовать сервер сценариев Windows, [а не WMI](/previous-versions/visualstudio/visual-basic-6/aa242706(v=vs.60)) .</span><span class="sxs-lookup"><span data-stu-id="c368b-105">If you want to copy a file or read and write a file, the easiest way is to use the Windows Script Host [FileSystemObject](/previous-versions/visualstudio/visual-basic-6/aa242706(v=vs.60)) rather than WMI.</span></span> <span data-ttu-id="c368b-106">Другие примеры см. в разделе [файлы и папки](/previous-versions/tn-archive/ee176985(v=technet.10)) раздела [TechNet скриптцентер](https://www.microsoft.com/technet/scriptcenter).</span><span class="sxs-lookup"><span data-stu-id="c368b-106">For other examples, see the [Files and Folders](/previous-versions/tn-archive/ee176985(v=technet.10)) section of the [TechNet ScriptCenter](https://www.microsoft.com/technet/scriptcenter).</span></span>

<span data-ttu-id="c368b-107">[**Модель CIM \_ Файл**](/windows/desktop/CIMWin32Prov/cim-datafile) данных является одним из нескольких [классов CIM](cimclas.md) в инструментарии WMI, который реализован.</span><span class="sxs-lookup"><span data-stu-id="c368b-107">[**CIM\_DataFile**](/windows/desktop/CIMWin32Prov/cim-datafile) is one of the few [CIM classes](cimclas.md) in WMI that is implemented.</span></span> <span data-ttu-id="c368b-108">Избегайте перечисления или запроса для всех экземпляров **\_ файла данных CIM** на компьютере, так как объем данных, скорее всего, повлияет на производительность или приводит к зависанию компьютера.</span><span class="sxs-lookup"><span data-stu-id="c368b-108">Avoid enumerating or querying for all instances of **CIM\_DataFile** on a computer because the volume of data is likely to either affect performance or cause the computer to stop responding.</span></span>

<span data-ttu-id="c368b-109">Примеры сценариев, приведенные в этом разделе, получают данные только с локального компьютера.</span><span class="sxs-lookup"><span data-stu-id="c368b-109">The script examples shown in this topic obtain data only from the local computer.</span></span> <span data-ttu-id="c368b-110">Дополнительные сведения об использовании сценария для получения данных с удаленных компьютеров см. в разделе [Подключение к WMI на удаленном компьютере](connecting-to-wmi-on-a-remote-computer.md).</span><span class="sxs-lookup"><span data-stu-id="c368b-110">For more information about how to use the script to obtain data from remote computers, see [Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span></span>


<span data-ttu-id="c368b-111">В следующей процедуре описывается выполнение скрипта.</span><span class="sxs-lookup"><span data-stu-id="c368b-111">The following procedure describes how to run a script.</span></span>

<span data-ttu-id="c368b-112">**Запуск сценария**</span><span class="sxs-lookup"><span data-stu-id="c368b-112">**To run a script**</span></span>

1.  <span data-ttu-id="c368b-113">Скопируйте код и сохраните его в файле с расширением vbs, например *filename.vbs*.</span><span class="sxs-lookup"><span data-stu-id="c368b-113">Copy the code and save it in a file with a .vbs extension, such as *filename.vbs*.</span></span> <span data-ttu-id="c368b-114">Убедитесь, что текстовый редактор не добавляет расширение txt в файл.</span><span class="sxs-lookup"><span data-stu-id="c368b-114">Ensure that your text editor does not add a .txt extension to the file.</span></span>
2.  <span data-ttu-id="c368b-115">Откройте окно командной строки и перейдите в каталог, в котором был сохранен файл.</span><span class="sxs-lookup"><span data-stu-id="c368b-115">Open a command prompt window and navigate to the directory where you saved the file.</span></span>
3.  <span data-ttu-id="c368b-116">Введите **cscript filename.vbs** в командной строке.</span><span class="sxs-lookup"><span data-stu-id="c368b-116">Type **cscript filename.vbs** at the command prompt.</span></span>
4.  <span data-ttu-id="c368b-117">Если доступ к журналу событий невозможен, проверьте, выполняется ли в командной строке с повышенными привилегиями.</span><span class="sxs-lookup"><span data-stu-id="c368b-117">If you cannot access an event log, check to see if you are running from an Elevated command prompt.</span></span> <span data-ttu-id="c368b-118">Некоторые журналы событий, например журнал событий безопасности, могут быть защищены с помощью элементов управления доступом пользователей (UAC).</span><span class="sxs-lookup"><span data-stu-id="c368b-118">Some Event Log, such as the Security Event Log, may be protected by User Access Controls (UAC).</span></span>

> [!Note]  
> <span data-ttu-id="c368b-119">По умолчанию Cscript отображает выходные данные скрипта в окне командной строки.</span><span class="sxs-lookup"><span data-stu-id="c368b-119">By default, cscript displays the output of a script in the command prompt window.</span></span> <span data-ttu-id="c368b-120">Поскольку сценарии WMI могут создавать большие объемы выходных данных, может потребоваться перенаправить выходные данные в файл.</span><span class="sxs-lookup"><span data-stu-id="c368b-120">Because WMI scripts can produce large amounts of output, you might want to redirect the output to a file.</span></span> <span data-ttu-id="c368b-121">Введите **cscript filename.vbs > outfile.txt** в командной строке, чтобы перенаправить выходные данные скрипта *filename.vbs* в *outfile.txt*.</span><span class="sxs-lookup"><span data-stu-id="c368b-121">Type **cscript filename.vbs > outfile.txt** at the command prompt to redirect the output of the *filename.vbs* script to *outfile.txt*.</span></span>

 

<span data-ttu-id="c368b-122">В следующей таблице перечислены примеры сценариев, которые можно использовать для получения различных типов данных с локального компьютера.</span><span class="sxs-lookup"><span data-stu-id="c368b-122">The following table lists script examples that can be used to obtain various types of data from the local computer.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c368b-123">Часто выполняемые действия в новом интерфейсе</span><span class="sxs-lookup"><span data-stu-id="c368b-123">How do I...</span></span></th>
<th><span data-ttu-id="c368b-124">Классы или методы WMI</span><span class="sxs-lookup"><span data-stu-id="c368b-124">WMI classes or methods</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c368b-125">... переименовать файл без получения сообщения об ошибке?</span><span class="sxs-lookup"><span data-stu-id="c368b-125">...rename a file without getting an error message?</span></span></td>
<td><span data-ttu-id="c368b-126">Используйте класс <a href="/windows/desktop/CIMWin32Prov/cim-datafile"><strong>CIM_DataFile</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="c368b-126">Use the <a href="/windows/desktop/CIMWin32Prov/cim-datafile"><strong>CIM_DataFile</strong></a> class.</span></span> <span data-ttu-id="c368b-127">Убедитесь, что при вызове метода <a href="/windows/desktop/CIMWin32Prov/rename-method-in-class-cim-datafile"><strong>Rename</strong></a> передается полное имя пути, например &quot;C:\Scripts\Test.txt&quot; вместо &quot;Text.txt&quot; .</span><span class="sxs-lookup"><span data-stu-id="c368b-127">Ensure that you pass the entire path name when calling the <a href="/windows/desktop/CIMWin32Prov/rename-method-in-class-cim-datafile"><strong>Rename</strong></a> method, for example, &quot;C:\Scripts\Test.txt&quot; instead of &quot;Text.txt&quot;.</span></span> <span data-ttu-id="c368b-128">Для PowerShell использование <strong>CIM_DataFile</strong> может оказаться неэффективным.</span><span class="sxs-lookup"><span data-stu-id="c368b-128">For PowerShell, using <strong>CIM_DataFile</strong> may be inefficient.</span></span> <span data-ttu-id="c368b-129">Таким образом, вы можете просто использовать командлет Rename-Item.</span><span class="sxs-lookup"><span data-stu-id="c368b-129">As such, you may simply use the Rename-Item cmdlet.</span></span><br/> <span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c368b-130">VB</span><span class="sxs-lookup"><span data-stu-id="c368b-130">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colFiles = objWMIService.ExecQuery (&quot;Select * from CIM_DataFile where Name = &quot; & &quot;&#39;c:\\scripts\\toggle_service.vbs&#39;&quot;)
For Each objFile in colFiles
    errResult = objFile.Rename(&quot;c:\scripts\toggle_service.old&quot;)
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
<th><span data-ttu-id="c368b-131">PowerShell</span><span class="sxs-lookup"><span data-stu-id="c368b-131">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>rename-item c:\scripts\toggle_service.vbs toggle_service.old</code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="c368b-132">... Определите, есть ли у пользователей. Файлы MP3, хранящиеся на их компьютере?</span><span class="sxs-lookup"><span data-stu-id="c368b-132">...determine whether users have .MP3 files stored on their computer?</span></span></td>
<td><p><span data-ttu-id="c368b-133">Используйте класс <a href="/windows/desktop/CIMWin32Prov/cim-datafile"><strong>CIM_DataFile</strong></a> и выберите файлы с помощью следующего предложения <a href="querying-with-wql.md"></a> <strong>WHERE</strong> WQL: где Extension = &quot; MP3 &quot; .</span><span class="sxs-lookup"><span data-stu-id="c368b-133">Use the <a href="/windows/desktop/CIMWin32Prov/cim-datafile"><strong>CIM_DataFile</strong></a> class and select files using the following <a href="querying-with-wql.md">WQL</a> <strong>WHERE</strong> clause: Where Extension = &quot;MP3&quot;.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c368b-134">VB</span><span class="sxs-lookup"><span data-stu-id="c368b-134">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colFiles = objWMIService.ExecQuery(&quot;Select * from CIM_DataFile where Extension = &#39;mp3&#39;&quot;)
For Each objFile in colFiles
    Wscript.Echo &quot;File Name: &quot; & objFile.Name & &quot;.&quot; & objFile.Extension
    Wscript.Echo &quot;Path: &quot; & objFile.Path
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
<th><span data-ttu-id="c368b-135">PowerShell</span><span class="sxs-lookup"><span data-stu-id="c368b-135">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>Get-WmiObject -Class CIM_DataFile -namespace &quot;root\cimv2&quot; -Filter &quot;Extension = &#39;mp3&#39;&quot; | `
   format-list Name, Extension, Path</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c368b-136">... создавать общие папки на компьютере?</span><span class="sxs-lookup"><span data-stu-id="c368b-136">...create shared folders on a computer?</span></span></td>
<td><p><span data-ttu-id="c368b-137">Используйте класс <a href="/windows/desktop/CIMWin32Prov/win32-share"><strong>Win32_Share</strong></a> и метод <a href="/windows/desktop/CIMWin32Prov/create-method-in-class-win32-share"><strong>CREATE</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="c368b-137">Use the <a href="/windows/desktop/CIMWin32Prov/win32-share"><strong>Win32_Share</strong></a> class and the <a href="/windows/desktop/CIMWin32Prov/create-method-in-class-win32-share"><strong>Create</strong></a> method.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c368b-138">VB</span><span class="sxs-lookup"><span data-stu-id="c368b-138">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>Const FILE_SHARE = 0
Const MAXIMUM_CONNECTIONS = 25
strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set objNewShare = objWMIService.Get(&quot;Win32_Share&quot;)
errReturn = objNewShare.Create(&quot;C:\Finance&quot;, &quot;FinanceShare&quot;, FILE_SHARE, MAXIMUM_CONNECTIONS, &quot;Public share for the Finance group.&quot;)</code></pre></td>
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
<th><span data-ttu-id="c368b-139">PowerShell</span><span class="sxs-lookup"><span data-stu-id="c368b-139">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$FILE_SHARE = 0
$MAXIMUM_CONNECTIONS = 25

$NewDir = new-item C:\Finance -type directory 
$Shares= [WMICLASS]&quot;Win32_Share&quot;
[void]$Shares.Create(&quot;C:\Finance&quot;,&quot;FinanceShare&quot;, $FILE_SHARE, $MAXIMUM_CONNECTIONS, &quot;Public share for the Finance group.&quot;) </code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c368b-140">... копировать папку?</span><span class="sxs-lookup"><span data-stu-id="c368b-140">...copy a folder?</span></span></td>
<td><p><span data-ttu-id="c368b-141">Используйте класс <a href="/windows/desktop/CIMWin32Prov/win32-directory"><strong>Win32_Directory</strong></a> и метод <a href="/windows/desktop/CIMWin32Prov/copy-method-in-class-win32-directory"><strong>Copy</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="c368b-141">Use the <a href="/windows/desktop/CIMWin32Prov/win32-directory"><strong>Win32_Directory</strong></a> class and the <a href="/windows/desktop/CIMWin32Prov/copy-method-in-class-win32-directory"><strong>Copy</strong></a> method.</span></span> <span data-ttu-id="c368b-142">Для PowerShell можно просто использовать командлет Copy-Item.</span><span class="sxs-lookup"><span data-stu-id="c368b-142">For PowerShell, you can simply use the Copy-Item cmdlet.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c368b-143">VB</span><span class="sxs-lookup"><span data-stu-id="c368b-143">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot; 
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;) 
 
Set colFolders = objWMIService.ExecQuery(&quot;Select * from Win32_Directory where Name = &#39;c:\\Scripts&#39;&quot;) 
 
For Each objFolder in colFolders 
    errResults  = objFolder.Copy(&quot;D:\Archive&quot;) 
Next </code></pre></td>
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
<th><span data-ttu-id="c368b-144">PowerShell</span><span class="sxs-lookup"><span data-stu-id="c368b-144">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>Copy-Item C:\Scripts -Destination D:\Archive -Recurse</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c368b-145">... переместить папку?</span><span class="sxs-lookup"><span data-stu-id="c368b-145">...move a folder?</span></span></td>
<td><p><span data-ttu-id="c368b-146">Используйте класс <a href="/windows/desktop/CIMWin32Prov/win32-directory"><strong>Win32_Directory</strong></a> и метод <a href="/windows/desktop/CIMWin32Prov/rename-method-in-class-win32-directory"><strong>Rename</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="c368b-146">Use the <a href="/windows/desktop/CIMWin32Prov/win32-directory"><strong>Win32_Directory</strong></a> class and the <a href="/windows/desktop/CIMWin32Prov/rename-method-in-class-win32-directory"><strong>Rename</strong></a> method.</span></span> <span data-ttu-id="c368b-147">Для PowerShell можно просто использовать командлет Move-Item.</span><span class="sxs-lookup"><span data-stu-id="c368b-147">For PowerShell, you can simply use the Move-Item cmdlet.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c368b-148">VB</span><span class="sxs-lookup"><span data-stu-id="c368b-148">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot; 
Set objWMIService = GetObject(&quot;winmgmts:&quot; _ 
    & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;) 
 
Set colFolders = objWMIService.ExecQuery _ 
    (&quot;Select * from Win32_Directory where name = &#39;c:\\Scripts&#39;&quot;) 
 
For Each objFolder in colFolders 
    errResults = objFolder.Rename(&quot;C:\Admins\Documents\Archive\VBScript&quot;) 
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
<th><span data-ttu-id="c368b-149">PowerShell</span><span class="sxs-lookup"><span data-stu-id="c368b-149">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>move-item -path C:\Scripts -destination C:\Admins\Documents\Archive\PowerShell</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="c368b-150">См. также</span><span class="sxs-lookup"><span data-stu-id="c368b-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c368b-151">Задачи WMI для скриптов и приложений</span><span class="sxs-lookup"><span data-stu-id="c368b-151">WMI Tasks for Scripts and Applications</span></span>](wmi-tasks-for-scripts-and-applications.md)
</dt> <dt>

[<span data-ttu-id="c368b-152">Примеры приложений WMI на C++</span><span class="sxs-lookup"><span data-stu-id="c368b-152">WMI C++ Application Examples</span></span>](wmi-c---application-examples.md)
</dt> <dt>

[<span data-ttu-id="c368b-153">Скриптцентер TechNet</span><span class="sxs-lookup"><span data-stu-id="c368b-153">TechNet ScriptCenter</span></span>](https://www.microsoft.com/technet/scriptcenter)
</dt> </dl>

 

 



`
