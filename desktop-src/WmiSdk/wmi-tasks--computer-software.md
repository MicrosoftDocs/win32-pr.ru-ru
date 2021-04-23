---
description: Задачи WMI для программного обеспечения компьютера получают такие сведения, как программное обеспечение, устанавливаемое Microsoft установщик Windows (MSI) и версии программного обеспечения. Другие примеры см. в разделе TechNet Скриптцентер по адресу https://www.microsoft.com/technet .
ms.assetid: 65a61be3-7870-4178-9e96-78b82898271f
ms.tgt_platform: multiple
title: 'Задачи WMI: программное обеспечение компьютера'
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 800a42764cbb1b9552a8ecc87debc04685d28850
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104546791"
---
# <a name="wmi-tasks-computer-software"></a><span data-ttu-id="e1af4-104">Задачи WMI: программное обеспечение компьютера</span><span class="sxs-lookup"><span data-stu-id="e1af4-104">WMI Tasks: Computer Software</span></span>

<span data-ttu-id="e1af4-105">Задачи WMI для программного обеспечения компьютера получают такие сведения, как программное обеспечение, устанавливаемое Microsoft установщик Windows (MSI) и версии программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="e1af4-105">WMI tasks for computer software obtain information such as which software is installed by the Microsoft Windows Installer (MSI) and software versions.</span></span> <span data-ttu-id="e1af4-106">Другие примеры см. в разделе TechNet Скриптцентер по адресу [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx) .</span><span class="sxs-lookup"><span data-stu-id="e1af4-106">For other examples, see the TechNet ScriptCenter at [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx).</span></span>

<span data-ttu-id="e1af4-107">Примеры сценариев, приведенные в этом разделе, получают данные только с локального компьютера.</span><span class="sxs-lookup"><span data-stu-id="e1af4-107">The script examples shown in this topic obtain data only from the local computer.</span></span> <span data-ttu-id="e1af4-108">Дополнительные сведения об использовании сценария для получения данных с удаленных компьютеров см. в разделе [Подключение к WMI на удаленном компьютере](connecting-to-wmi-on-a-remote-computer.md).</span><span class="sxs-lookup"><span data-stu-id="e1af4-108">For more information about how to use the script to obtain data from remote computers, see [Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span></span>


<span data-ttu-id="e1af4-109">В следующей процедуре описывается выполнение скрипта.</span><span class="sxs-lookup"><span data-stu-id="e1af4-109">The following procedure describes how to run a script.</span></span>

<span data-ttu-id="e1af4-110">**Запуск сценария**</span><span class="sxs-lookup"><span data-stu-id="e1af4-110">**To run a script**</span></span>

1.  <span data-ttu-id="e1af4-111">Скопируйте код и сохраните его в файле с расширением vbs, например *filename.vbs*.</span><span class="sxs-lookup"><span data-stu-id="e1af4-111">Copy the code and save it in a file with a .vbs extension, such as *filename.vbs*.</span></span> <span data-ttu-id="e1af4-112">Убедитесь, что текстовый редактор не добавляет расширение txt в файл.</span><span class="sxs-lookup"><span data-stu-id="e1af4-112">Ensure that your text editor does not add a .txt extension to the file.</span></span>
2.  <span data-ttu-id="e1af4-113">Откройте окно командной строки и перейдите в каталог, в котором был сохранен файл.</span><span class="sxs-lookup"><span data-stu-id="e1af4-113">Open a command prompt window and navigate to the directory where you saved the file.</span></span>
3.  <span data-ttu-id="e1af4-114">Введите **cscript filename.vbs** в командной строке.</span><span class="sxs-lookup"><span data-stu-id="e1af4-114">Type **cscript filename.vbs** at the command prompt.</span></span>
4.  <span data-ttu-id="e1af4-115">Если доступ к журналу событий невозможен, проверьте, выполняется ли в командной строке с повышенными привилегиями.</span><span class="sxs-lookup"><span data-stu-id="e1af4-115">If you cannot access an event log, check to see if you are running from an Elevated command prompt.</span></span> <span data-ttu-id="e1af4-116">Некоторые журналы событий, например журнал событий безопасности, могут быть защищены с помощью элементов управления доступом пользователей (UAC).</span><span class="sxs-lookup"><span data-stu-id="e1af4-116">Some Event Log, such as the Security Event Log, may be protected by User Access Controls (UAC).</span></span>

> [!Note]  
> <span data-ttu-id="e1af4-117">По умолчанию Cscript отображает выходные данные скрипта в окне командной строки.</span><span class="sxs-lookup"><span data-stu-id="e1af4-117">By default, cscript displays the output of a script in the command prompt window.</span></span> <span data-ttu-id="e1af4-118">Поскольку сценарии WMI могут создавать большие объемы выходных данных, может потребоваться перенаправить выходные данные в файл.</span><span class="sxs-lookup"><span data-stu-id="e1af4-118">Because WMI scripts can produce large amounts of output, you might want to redirect the output to a file.</span></span> <span data-ttu-id="e1af4-119">Введите **cscript filename.vbs > outfile.txt** в командной строке, чтобы перенаправить выходные данные скрипта *filename.vbs* в *outfile.txt*.</span><span class="sxs-lookup"><span data-stu-id="e1af4-119">Type **cscript filename.vbs > outfile.txt** at the command prompt to redirect the output of the *filename.vbs* script to *outfile.txt*.</span></span>

 

> [!Note]  
> <span data-ttu-id="e1af4-120">Выполнение запроса "Выбор \* из \_ продукта Win32" может привести к непредвиденному поведению.</span><span class="sxs-lookup"><span data-stu-id="e1af4-120">Running a "Select \* from Win32\_Product" query may result in unexpected behavior.</span></span> <span data-ttu-id="e1af4-121">Это связано с тем, что поставщик, поддерживающий продукт Win32, \_ не оптимизирован для запросов.</span><span class="sxs-lookup"><span data-stu-id="e1af4-121">This is because the provider that supports Win32\_Product is not query optimized.</span></span> <span data-ttu-id="e1af4-122">Дополнительные сведения см. в [статье базы знаний 974524](https://support.microsoft.com/kb/974524).</span><span class="sxs-lookup"><span data-stu-id="e1af4-122">For more information, see [KB Article 974524](https://support.microsoft.com/kb/974524).</span></span>

 

<span data-ttu-id="e1af4-123">В следующей таблице перечислены примеры сценариев, которые можно использовать для получения различных типов данных с локального компьютера.</span><span class="sxs-lookup"><span data-stu-id="e1af4-123">The following table lists script examples that can be used to obtain various types of data from the local computer.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e1af4-124">Часто выполняемые действия в новом интерфейсе</span><span class="sxs-lookup"><span data-stu-id="e1af4-124">How do I...</span></span></th>
<th><span data-ttu-id="e1af4-125">Классы или методы WMI</span><span class="sxs-lookup"><span data-stu-id="e1af4-125">WMI classes or methods</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e1af4-126">... удалить программное обеспечение с помощью сценария?</span><span class="sxs-lookup"><span data-stu-id="e1af4-126">...uninstall software using a script?</span></span></td>
<td><span data-ttu-id="e1af4-127">Если программное обеспечение было установлено с помощью Microsoft установщик Windows (MSI), используйте класс WMI <a href="/previous-versions/windows/desktop/legacy/aa394378(v=vs.85)"><strong>Win32_Product</strong></a> и метод <a href="/previous-versions/windows/desktop/msiprov/uninstall-method-in-class-win32-product"><strong>удаления</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="e1af4-127">If the software was installed using Microsoft Windows Installer (MSI), use the WMI class <a href="/previous-versions/windows/desktop/legacy/aa394378(v=vs.85)"><strong>Win32_Product</strong></a> and the <a href="/previous-versions/windows/desktop/msiprov/uninstall-method-in-class-win32-product"><strong>Uninstall</strong></a> method.</span></span><br/> <span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e1af4-128">VB</span><span class="sxs-lookup"><span data-stu-id="e1af4-128">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; _
    & &quot;{impersonationLevel=impersonate}!\\&quot; _
    & strComputer & &quot;\root\cimv2&quot;)
Set colSoftware = objWMIService.ExecQuery _
    (&quot;Select * from Win32_Product &quot; _
        & &quot;Where Name = &#39;Personnel database&#39;&quot;)
For Each objSoftware in colSoftware
    objSoftware.Uninstall()
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
<th><span data-ttu-id="e1af4-129">PowerShell</span><span class="sxs-lookup"><span data-stu-id="e1af4-129">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$colSoftware = Get-WmiObject -Class Win32_Product | Where-Object {$_.name -eq &quot;Personnel database&quot;}

foreach ($colItem in $colSoftware)
{
    $colItem.Uninstall()
}</code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="e1af4-130">... проводить инвентаризацию всех программ, установленных на компьютере с помощью сценария?</span><span class="sxs-lookup"><span data-stu-id="e1af4-130">...inventory all the software installed on a computer with a script?</span></span></td>
<td><p><span data-ttu-id="e1af4-131">Если программное обеспечение было установлено с помощью Microsoft установщик Windows (MSI), используйте класс WMI <a href="/previous-versions/windows/desktop/legacy/aa394378(v=vs.85)"><strong>Win32_Product</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="e1af4-131">If the software was installed using Microsoft Windows Installer (MSI) use the WMI class <a href="/previous-versions/windows/desktop/legacy/aa394378(v=vs.85)"><strong>Win32_Product</strong></a>.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e1af4-132">VB</span><span class="sxs-lookup"><span data-stu-id="e1af4-132">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; _
    & &quot;{impersonationLevel=impersonate}!\\&quot; _
    & strComputer & &quot;\root\cimv2&quot;)
Set colSoftware = objWMIService.ExecQuery _
    (&quot;Select * from Win32_Product&quot;)

For Each objSoftware in colSoftware
    Wscript.Echo &quot;Name: &quot; & objSoftware.Name
    Wscript.Echo &quot;Version: &quot; & objSoftware.Version
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
<th><span data-ttu-id="e1af4-133">PowerShell</span><span class="sxs-lookup"><span data-stu-id="e1af4-133">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$colSoftware = Get-WmiObject -Class Win32_Product

foreach ($colItem in $colSoftware)
{
    &quot;Name: &quot; + $colItem.Name
    &quot;Version: &quot;+ $colItem.Version
}</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e1af4-134">... определить, какая версия Microsoft Office установлена?</span><span class="sxs-lookup"><span data-stu-id="e1af4-134">...determine what version of Microsoft Office is installed?</span></span></td>
<td><p><span data-ttu-id="e1af4-135">Используйте класс <a href="/previous-versions/windows/desktop/legacy/aa394378(v=vs.85)"><strong>Win32_Product</strong></a> и проверьте значение свойства <strong>Version</strong> .</span><span class="sxs-lookup"><span data-stu-id="e1af4-135">Use the <a href="/previous-versions/windows/desktop/legacy/aa394378(v=vs.85)"><strong>Win32_Product</strong></a> class and check the value of the <strong>Version</strong> property.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e1af4-136">VB</span><span class="sxs-lookup"><span data-stu-id="e1af4-136">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;.&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; _
    & &quot;{impersonationLevel=impersonate}!\\&quot; _
    & strComputer & &quot;\root\cimv2&quot;)
Set colSoftware = objWMIService.ExecQuery(_
    &quot;Select * from Win32_Product &quot; & _
    &quot;Where IdentifyingNumber =&quot; _
        & &quot; &#39;{90280409-6000-11D3-8CFE-0050048383C9}&#39;&quot;)
For Each objItem in colSoftware
    Wscript.Echo &quot;Name: &quot; & objItem.Name
    Wscript.Echo &quot;Version: &quot; & objItem.Version
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
<th><span data-ttu-id="e1af4-137">PowerShell</span><span class="sxs-lookup"><span data-stu-id="e1af4-137">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$colSoftware = Get-WmiObject -Class Win32_Product | Where-Object {$_.IdentifyingNumber -eq &quot;{90280409-6000-11D3-8CFE-0050048383C9}&quot;}

foreach ($colItem in $colSoftware)
{
    &quot;Name: &quot; + $colItem.Name
    &quot;Version: &quot; + $colItem.Version
}</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
</tbody>
</table>



 

## <a name="examples"></a><span data-ttu-id="e1af4-138">Примеры</span><span class="sxs-lookup"><span data-stu-id="e1af4-138">Examples</span></span>

<span data-ttu-id="e1af4-139">В примере кода PowerShell для [PowerShell Remote PC info](https://Gallery.TechNet.Microsoft.Com/2a8a008c-ee30-4b50-a81a-1b7545ef3436) используется ряд аппаратных и программных классов, включая Win32Product, для поиска различных сведений об удаленном ПК с помощью WMI и удаленного реестра.</span><span class="sxs-lookup"><span data-stu-id="e1af4-139">The [Powershell Remote PC Info Script](https://Gallery.TechNet.Microsoft.Com/2a8a008c-ee30-4b50-a81a-1b7545ef3436) PowerShell code sample uses a number of hardware and software classes, including Win32Product, to find various information about a remote PC using WMI and the remote registry.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e1af4-140">См. также</span><span class="sxs-lookup"><span data-stu-id="e1af4-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e1af4-141">Задачи WMI для скриптов и приложений</span><span class="sxs-lookup"><span data-stu-id="e1af4-141">WMI Tasks for Scripts and Applications</span></span>](wmi-tasks-for-scripts-and-applications.md)
</dt> <dt>

[<span data-ttu-id="e1af4-142">Примеры приложений WMI на C++</span><span class="sxs-lookup"><span data-stu-id="e1af4-142">WMI C++ Application Examples</span></span>](wmi-c---application-examples.md)
</dt> <dt>

[<span data-ttu-id="e1af4-143">Скриптцентер TechNet</span><span class="sxs-lookup"><span data-stu-id="e1af4-143">TechNet ScriptCenter</span></span>](https://www.microsoft.com/technet/scriptcenter)
</dt> </dl>

 

