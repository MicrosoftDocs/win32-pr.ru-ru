---
description: Задачи WMI для реестра создают и изменяют разделы и значения реестра. Другие примеры см. в разделе TechNet Скриптцентер по адресу https://www.microsoft.com/technet .
ms.assetid: 0785189e-9638-4776-8414-1414d7b02524
ms.tgt_platform: multiple
title: 'Задачи WMI: реестр'
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: df6ae73d41c9cbfd6cd303b72e1b9207f3191c85
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105656669"
---
# <a name="wmi-tasks-registry"></a><span data-ttu-id="b8e18-104">Задачи WMI: реестр</span><span class="sxs-lookup"><span data-stu-id="b8e18-104">WMI Tasks: Registry</span></span>

<span data-ttu-id="b8e18-105">Задачи WMI для реестра создают и изменяют разделы и значения реестра.</span><span class="sxs-lookup"><span data-stu-id="b8e18-105">WMI tasks for the registry create and modify registry keys and values.</span></span> <span data-ttu-id="b8e18-106">Другие примеры см. в разделе TechNet Скриптцентер по адресу [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx) .</span><span class="sxs-lookup"><span data-stu-id="b8e18-106">For other examples, see the TechNet ScriptCenter at [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx).</span></span>

<span data-ttu-id="b8e18-107">Примеры сценариев, приведенные в этом разделе, получают данные только с локального компьютера.</span><span class="sxs-lookup"><span data-stu-id="b8e18-107">The script examples shown in this topic obtain data only from the local computer.</span></span> <span data-ttu-id="b8e18-108">Дополнительные сведения об использовании сценария для получения данных с удаленных компьютеров см. в разделе [Подключение к WMI на удаленном компьютере](connecting-to-wmi-on-a-remote-computer.md).</span><span class="sxs-lookup"><span data-stu-id="b8e18-108">For more information about how to use the script to obtain data from remote computers, see [Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span></span>


<span data-ttu-id="b8e18-109">В следующей процедуре описывается выполнение скрипта.</span><span class="sxs-lookup"><span data-stu-id="b8e18-109">The following procedure describes how to run a script.</span></span>

<span data-ttu-id="b8e18-110">**Запуск сценария**</span><span class="sxs-lookup"><span data-stu-id="b8e18-110">**To run a script**</span></span>

1.  <span data-ttu-id="b8e18-111">Скопируйте код и сохраните его в файле с расширением vbs, например *filename.vbs*.</span><span class="sxs-lookup"><span data-stu-id="b8e18-111">Copy the code and save it in a file with a .vbs extension, such as *filename.vbs*.</span></span> <span data-ttu-id="b8e18-112">Убедитесь, что текстовый редактор не добавляет расширение txt в файл.</span><span class="sxs-lookup"><span data-stu-id="b8e18-112">Ensure that your text editor does not add a .txt extension to the file.</span></span>
2.  <span data-ttu-id="b8e18-113">Откройте окно командной строки и перейдите в каталог, в котором был сохранен файл.</span><span class="sxs-lookup"><span data-stu-id="b8e18-113">Open a command prompt window and navigate to the directory where you saved the file.</span></span>
3.  <span data-ttu-id="b8e18-114">Введите **cscript filename.vbs** в командной строке.</span><span class="sxs-lookup"><span data-stu-id="b8e18-114">Type **cscript filename.vbs** at the command prompt.</span></span>
4.  <span data-ttu-id="b8e18-115">Если доступ к журналу событий невозможен, проверьте, выполняется ли в командной строке с повышенными привилегиями.</span><span class="sxs-lookup"><span data-stu-id="b8e18-115">If you cannot access an event log, check to see if you are running from an Elevated command prompt.</span></span> <span data-ttu-id="b8e18-116">Некоторые журналы событий, например журнал событий безопасности, могут быть защищены с помощью элементов управления доступом пользователей (UAC).</span><span class="sxs-lookup"><span data-stu-id="b8e18-116">Some Event Log, such as the Security Event Log, may be protected by User Access Controls (UAC).</span></span>

> [!Note]  
> <span data-ttu-id="b8e18-117">По умолчанию Cscript отображает выходные данные скрипта в окне командной строки.</span><span class="sxs-lookup"><span data-stu-id="b8e18-117">By default, cscript displays the output of a script in the command prompt window.</span></span> <span data-ttu-id="b8e18-118">Поскольку сценарии WMI могут создавать большие объемы выходных данных, может потребоваться перенаправить выходные данные в файл.</span><span class="sxs-lookup"><span data-stu-id="b8e18-118">Because WMI scripts can produce large amounts of output, you might want to redirect the output to a file.</span></span> <span data-ttu-id="b8e18-119">Введите **cscript filename.vbs > outfile.txt** в командной строке, чтобы перенаправить выходные данные скрипта *filename.vbs* в *outfile.txt*.</span><span class="sxs-lookup"><span data-stu-id="b8e18-119">Type **cscript filename.vbs > outfile.txt** at the command prompt to redirect the output of the *filename.vbs* script to *outfile.txt*.</span></span>

 

<span data-ttu-id="b8e18-120">В следующей таблице перечислены примеры сценариев, которые можно использовать для получения различных типов данных с локального компьютера.</span><span class="sxs-lookup"><span data-stu-id="b8e18-120">The following table lists script examples that can be used to obtain various types of data from the local computer.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b8e18-121">Часто выполняемые действия в новом интерфейсе</span><span class="sxs-lookup"><span data-stu-id="b8e18-121">How do I...</span></span></th>
<th><span data-ttu-id="b8e18-122">Классы или методы WMI</span><span class="sxs-lookup"><span data-stu-id="b8e18-122">WMI classes or methods</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b8e18-123">... считать значения разделов реестра с помощью инструментария WMI?</span><span class="sxs-lookup"><span data-stu-id="b8e18-123">...read registry key values using WMI?</span></span></td>
<td><span data-ttu-id="b8e18-124">Используйте класс <a href="/previous-versions/windows/desktop/regprov/stdregprov"><strong>стдрегпров</strong></a> , расположенный в пространстве имен root\default.</span><span class="sxs-lookup"><span data-stu-id="b8e18-124">Use the <a href="/previous-versions/windows/desktop/regprov/stdregprov"><strong>StdRegProv</strong></a> class, located in root\default namespace.</span></span> <span data-ttu-id="b8e18-125">Невозможно получить экземпляры этого класса, так как <a href="/previous-versions/windows/desktop/regprov/system-registry-provider">поставщик системного реестра</a> является только методом и поставщиком событий.</span><span class="sxs-lookup"><span data-stu-id="b8e18-125">You cannot get any instances of this class because the <a href="/previous-versions/windows/desktop/regprov/system-registry-provider">System Registry Provider</a> is a method and event provider only.</span></span> <span data-ttu-id="b8e18-126">Однако данные реестра можно получить с помощью таких методов, как <a href="/previous-versions/windows/desktop/regprov/enumkey-method-in-class-stdregprov"><strong>енумкэй</strong></a> или <a href="/previous-versions/windows/desktop/regprov/enumvalues-method-in-class-stdregprov"><strong>EnumValue</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="b8e18-126">However, you can get registry data through methods such as <a href="/previous-versions/windows/desktop/regprov/enumkey-method-in-class-stdregprov"><strong>EnumKey</strong></a> or <a href="/previous-versions/windows/desktop/regprov/enumvalues-method-in-class-stdregprov"><strong>EnumValue</strong></a>.</span></span> <span data-ttu-id="b8e18-127"><a href="/windows/desktop/CIMWin32Prov/win32-registry"><strong>Win32_Registry</strong></a>, расположенное в пространстве имен root\cimv2, получает данные о реестре в целом, например размер.</span><span class="sxs-lookup"><span data-stu-id="b8e18-127">The <a href="/windows/desktop/CIMWin32Prov/win32-registry"><strong>Win32_Registry</strong></a>, located in root\cimv2 namespace, gets data about the registry as a whole, such as how large it is.</span></span><br/> <span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b8e18-128">VB</span><span class="sxs-lookup"><span data-stu-id="b8e18-128">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>const HKEY_CURRENT_USER = &H80000001
strComputer = &quot;.&quot;
Set oReg=GetObject(&quot;winmgmts:{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\default:StdRegProv&quot;)
strKeyPath = &quot;Console&quot;
strValueName = &quot;HistoryBufferSize&quot;
oReg.GetDWORDValue HKEY_CURRENT_USER,strKeyPath,strValueName,dwValue
WScript.Echo &quot;Current History Buffer Size: &quot; & dwValue</code></pre></td>
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
<th><span data-ttu-id="b8e18-129">PowerShell</span><span class="sxs-lookup"><span data-stu-id="b8e18-129">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$HKEY_CURRENT_USER =2147483649
$computer =&#39;.&#39;
$reg = [WMIClass]&quot;ROOT\DEFAULT:StdRegProv&quot;
$Key = &quot;Console&quot;
$Value = &quot;HistoryBufferSize&quot;
$results = $reg.GetDWORDValue($HKEY_CURRENT_USER, $Key, $value)
&quot;Current History Buffer Size: {0}&quot; -f $results.uValue</code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="b8e18-130">... создать новый раздел реестра?</span><span class="sxs-lookup"><span data-stu-id="b8e18-130">...create a new registry key?</span></span></td>
<td><p><span data-ttu-id="b8e18-131">Используйте класс <a href="/previous-versions/windows/desktop/regprov/stdregprov"><strong>стдрегпров</strong></a> , расположенный в пространстве имен root\default, и метод <a href="/previous-versions/windows/desktop/regprov/createkey-method-in-class-stdregprov"><strong>CreateKey</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="b8e18-131">Use the <a href="/previous-versions/windows/desktop/regprov/stdregprov"><strong>StdRegProv</strong></a> class, located in root\default namespace, and the <a href="/previous-versions/windows/desktop/regprov/createkey-method-in-class-stdregprov"><strong>CreateKey</strong></a> method.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b8e18-132">VB</span><span class="sxs-lookup"><span data-stu-id="b8e18-132">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>const HKEY_LOCAL_MACHINE = &H80000002
strComputer = &quot;.&quot;
Set objReg=GetObject( &quot;winmgmts:{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\default:StdRegProv&quot;)

strKeyPath = &quot;SOFTWARE\NewKey&quot;
objReg.CreateKey HKEY_LOCAL_MACHINE,strKeyPath
WScript.Echo &quot;Created registry key HKEY_LOCAL_MACHINE\SOFTWARE\NewKey&quot;</code></pre></td>
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
<th><span data-ttu-id="b8e18-133">PowerShell</span><span class="sxs-lookup"><span data-stu-id="b8e18-133">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$HKEY_Local_Machine =2147483650 
$computer =&#39;.&#39;
$reg = [WMIClass]&quot;ROOT\DEFAULT:StdRegProv&quot;
$Key     = &quot;SOFTWARE\NewKey&quot;
$results   = $reg.CreateKey($HKEY_LOCAL_MACHINE, $Key)
If ($results.Returnvalue -eq 0) {&quot;Key created&quot;} </code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b8e18-134">... создать новое значение реестра в разделе?</span><span class="sxs-lookup"><span data-stu-id="b8e18-134">...create a new registry value under a key?</span></span></td>
<td><p><span data-ttu-id="b8e18-135">Используйте класс <a href="/previous-versions/windows/desktop/regprov/stdregprov"><strong>стдрегпров</strong></a> , расположенный в пространстве имен root\default, и метод <a href="/previous-versions/windows/desktop/regprov/createkey-method-in-class-stdregprov"><strong>CreateKey</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="b8e18-135">Use the <a href="/previous-versions/windows/desktop/regprov/stdregprov"><strong>StdRegProv</strong></a> class, located in the root\default namespace, and the <a href="/previous-versions/windows/desktop/regprov/createkey-method-in-class-stdregprov"><strong>CreateKey</strong></a> method.</span></span> <span data-ttu-id="b8e18-136">Затем используйте один из методов Set, в зависимости от того, какой тип данных реестра имеет значение, например <a href="/previous-versions/windows/desktop/regprov/setdwordvalue-method-in-class-stdregprov"><strong>сетдвордвалуе</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="b8e18-136">Then use one of the Set methods, depending on what registry datatype the value is, such as the <a href="/previous-versions/windows/desktop/regprov/setdwordvalue-method-in-class-stdregprov"><strong>SetDWORDValue</strong></a>.</span></span> <span data-ttu-id="b8e18-137">Методы Set создают значение, если оно еще не существует.</span><span class="sxs-lookup"><span data-stu-id="b8e18-137">The Set methods create a value if it does not already exist.</span></span> <span data-ttu-id="b8e18-138">Дополнительные сведения см. в разделе <a href="mapping-a-registry-data-type-to-a-wmi-data-type.md">сопоставление типа данных реестра с типом данных WMI</a>.</span><span class="sxs-lookup"><span data-stu-id="b8e18-138">For more information, see <a href="mapping-a-registry-data-type-to-a-wmi-data-type.md">Mapping a Registry Data Type to a WMI Data Type</a>.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b8e18-139">VB</span><span class="sxs-lookup"><span data-stu-id="b8e18-139">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>Const HKEY_LOCAL_MACHINE = &H80000002
strKeyPath = &quot;SOFTWARE\NewKey&quot;
strComputer = &quot;.&quot;
Set objReg=GetObject( &quot;winmgmts:{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\default:StdRegProv&quot;)
strValueName = &quot;Example_Expanded_String_Value&quot;
strValue = &quot;%PATHEXT%&quot;
objReg.SetExpandedStringValue HKEY_LOCAL_MACHINE,strKeyPath,strValueName,strValue
WScript.Echo &quot;Example expanded_String_Value at &quot; & &quot;HKEY_LOCAL_MACHINE\SOFTWARE\NewKey&quot;</code></pre></td>
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
<th><span data-ttu-id="b8e18-140">PowerShell</span><span class="sxs-lookup"><span data-stu-id="b8e18-140">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$HKEY_Local_Machine =2147483650 
$computer =&#39;.&#39;
$reg = [WMIClass]&quot;ROOT\DEFAULT:StdRegProv&quot;
$ValueName = &quot;Example_Expanded_String_Value&quot;
$Value     = &quot;%PATHEXT%&quot;
$Key       = &quot;SOFTWARE\NewKey&quot;
$results   = $reg.SetExpandedStringValue($HKEY_LOCAL_MACHINE, $Key, $ValueName, $Value)
If ($results.Returnvalue -eq 0) {&quot;Value created&quot;}</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b8e18-141">... не удается получить ошибку недопустимого класса при попытке записи скрипта для чтения реестра?</span><span class="sxs-lookup"><span data-stu-id="b8e18-141">...avoid getting an Invalid Class error when trying to write a script to read the registry?</span></span></td>
<td><p><span data-ttu-id="b8e18-142">Используйте пространство имен root\default при доступе к классу <a href="/previous-versions/windows/desktop/regprov/stdregprov"><strong>стдрегпров</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="b8e18-142">Use the root\default namespace when accessing the <a href="/previous-versions/windows/desktop/regprov/stdregprov"><strong>StdRegProv</strong></a> class.</span></span> <span data-ttu-id="b8e18-143"><strong>Стдрегпров</strong> не является частью пространства имен CIMV2, поэтому &quot; &quot; при попытке подключения к &quot; root\cimv2: Стдрегпров возникает ошибка недопустимого класса &quot; .</span><span class="sxs-lookup"><span data-stu-id="b8e18-143"><strong>StdRegProv</strong> is not part of the cimv2 namespace, which is why an &quot;Invalid Class&quot; error is generated if you try to connect to &quot;root\cimv2:StdRegProv&quot;.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b8e18-144">VB</span><span class="sxs-lookup"><span data-stu-id="b8e18-144">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>Const HKEY_CURRENT_USER = &H80000001
strComputer = &quot;.&quot;
Set oReg=GetObject( &quot;winmgmts:{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\default:StdRegProv&quot;) 
strKeyPath = &quot;Console&quot;
strValueName = &quot;HistoryBufferSize&quot;
oReg.GetDWORDValue HKEY_CURRENT_USER, strKeyPath, strValueName, dwValue
Wscript.Echo &quot;Current History Buffer Size: &quot; & dwValue</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b8e18-145">... проверить безопасность определенного раздела реестра?</span><span class="sxs-lookup"><span data-stu-id="b8e18-145">...check security on a specific registry key?</span></span></td>
<td><p><span data-ttu-id="b8e18-146">Используйте класс <a href="/previous-versions/windows/desktop/regprov/stdregprov"><strong>стдрегпров</strong></a> , расположенный в пространстве имен root\default и методе <a href="/previous-versions/windows/desktop/regprov/checkaccess-method-in-class-stdregprov"><strong>CheckAccess</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="b8e18-146">Use the <a href="/previous-versions/windows/desktop/regprov/stdregprov"><strong>StdRegProv</strong></a> class, located in root\default namespace and the <a href="/previous-versions/windows/desktop/regprov/checkaccess-method-in-class-stdregprov"><strong>CheckAccess</strong></a> method.</span></span> <span data-ttu-id="b8e18-147">Можно проверить только права доступа для текущего пользователя, выполняющего скрипт или приложение.</span><span class="sxs-lookup"><span data-stu-id="b8e18-147">You can only check the access rights for the current user that is running the script or application.</span></span> <span data-ttu-id="b8e18-148">Нельзя проверить права доступа для другого указанного пользователя.</span><span class="sxs-lookup"><span data-stu-id="b8e18-148">You cannot check the access rights for another specified user.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b8e18-149">... читать и записывать двоичные значения реестра?</span><span class="sxs-lookup"><span data-stu-id="b8e18-149">...read and write binary registry values?</span></span></td>
<td><p><span data-ttu-id="b8e18-150">Используйте класс <a href="/previous-versions/windows/desktop/regprov/stdregprov"><strong>стдрегпров</strong></a> , расположенный в &quot; &quot; пространстве имен Root\Default, а также методы <a href="/previous-versions/windows/desktop/regprov/getbinaryvalue-method-in-class-stdregprov"><strong>жетбинаривалуе</strong></a> и <a href="/previous-versions/windows/desktop/regprov/setbinaryvalue-method-in-class-stdregprov"><strong>сетбинаривалуе</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="b8e18-150">Use the <a href="/previous-versions/windows/desktop/regprov/stdregprov"><strong>StdRegProv</strong></a> class, located in &quot;Root\Default&quot; namespace and the <a href="/previous-versions/windows/desktop/regprov/getbinaryvalue-method-in-class-stdregprov"><strong>GetBinaryValue</strong></a> and <a href="/previous-versions/windows/desktop/regprov/setbinaryvalue-method-in-class-stdregprov"><strong>SetBinaryValue</strong></a> methods.</span></span> <span data-ttu-id="b8e18-151">Значения реестра, которые отображаются в служебной программе RegEdt32 как последовательность шестнадцатеричных значений байтов, представлены в <strong>REG_BINARY</strong> формате данных.</span><span class="sxs-lookup"><span data-stu-id="b8e18-151">Registry values that appear in the RegEdt32 utility as a series of byte hexadecimal values are in the <strong>REG_BINARY</strong> data format.</span></span> <span data-ttu-id="b8e18-152">Дополнительные сведения см. в разделе <a href="mapping-a-registry-data-type-to-a-wmi-data-type.md">сопоставление типа данных реестра с типом данных WMI</a>.</span><span class="sxs-lookup"><span data-stu-id="b8e18-152">For more information, see <a href="mapping-a-registry-data-type-to-a-wmi-data-type.md">Mapping a Registry Data Type to a WMI Data Type</a>.</span></span> <span data-ttu-id="b8e18-153">В следующем примере кода VBScript создается новый ключ с двоичным значением.</span><span class="sxs-lookup"><span data-stu-id="b8e18-153">The following VBScript code example creates a new key with a binary value.</span></span> <span data-ttu-id="b8e18-154">Двоичное значение указывается в массиве байтов <em>ивалуес</em> , указанном в шестнадцатеричном формате.</span><span class="sxs-lookup"><span data-stu-id="b8e18-154">The binary value is supplied in the <em>iValues</em> byte array specified in Hex.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b8e18-155">VB</span><span class="sxs-lookup"><span data-stu-id="b8e18-155">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>const HKEY_LOCAL_MACHINE = &H80000002
strKeyPath = &quot;SOFTWARE\NewKey&quot;
strComputer = &quot;.&quot;
iValues = Array(&H01,&Ha2,&H10)
Set oReg=GetObject(&quot;winmgmts:{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\default:StdRegProv&quot;)
oReg.CreateKey HKEY_LOCAL_MACHINE,strKeyPath
strKeyPath = &quot;SOFTWARE\NewKey&quot;
BinaryValueName = &quot;Example Binary Value&quot;

oReg.SetBinaryValue HKEY_LOCAL_MACHINE,strKeyPath,BinaryValueName,iValues</code></pre></td>
</tr>
</tbody>
</table>

</div>
<p><span data-ttu-id="b8e18-156">Следующий скрипт считывает двоичное значение.</span><span class="sxs-lookup"><span data-stu-id="b8e18-156">The following script reads the binary value.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b8e18-157">VB</span><span class="sxs-lookup"><span data-stu-id="b8e18-157">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>const HKEY_LOCAL_MACHINE = &H80000002 
strKeyPath = &quot;SOFTWARE\NewKey&quot;
strValueName = &quot;Example Binary Value&quot;
strComputer = &quot;.&quot;
dim iValues(3)
Set oReg=GetObject(&quot;winmgmts:{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\default:StdRegProv&quot;)
oReg.GetBinaryValue HKEY_LOCAL_MACHINE,strKeyPath,strValueName,iValues
For i = lBound(iValues) to uBound(iValues)
Wscript.Echo iValues(i)
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
<th><span data-ttu-id="b8e18-158">PowerShell</span><span class="sxs-lookup"><span data-stu-id="b8e18-158">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$HKEY_Local_Machine =2147483650 
$computer =&#39;.&#39;
$reg = [WMIClass]&quot;ROOT\DEFAULT:StdRegProv&quot;
$ValueName = &quot;Example Binary Value&quot;
$Values     = @(0x54, 0x46, 0x4C)
$Key       = &quot;SOFTWARE\NewKey&quot;
$results   = $reg.GetBinaryValue($HKEY_LOCAL_MACHINE, $Key, $ValueName)
Foreach ($byte in $results.uvalue) {&quot;{0}&quot; -f $byte.tostring(&quot;x&quot;)}</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b8e18-159">... читать и записывать значения реестра, содержащие несколько строк?</span><span class="sxs-lookup"><span data-stu-id="b8e18-159">...read and write registry values that contain multiple strings?</span></span></td>
<td><p><span data-ttu-id="b8e18-160">Используйте класс <a href="/previous-versions/windows/desktop/regprov/stdregprov"><strong>стдрегпров</strong></a> , расположенный в пространстве имен root\default, а также методы <a href="/previous-versions/windows/desktop/regprov/getmultistringvalue-method-in-class-stdregprov"><strong>жетмултистрингвалуе</strong></a> и <a href="/previous-versions/windows/desktop/regprov/setmultistringvalue-method-in-class-stdregprov"><strong>сетмултистрингвалуе</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="b8e18-160">Use the <a href="/previous-versions/windows/desktop/regprov/stdregprov"><strong>StdRegProv</strong></a> class, located in root\default namespace and the <a href="/previous-versions/windows/desktop/regprov/getmultistringvalue-method-in-class-stdregprov"><strong>GetMultiStringValue</strong></a> and <a href="/previous-versions/windows/desktop/regprov/setmultistringvalue-method-in-class-stdregprov"><strong>SetMultiStringValue</strong></a> methods.</span></span> <span data-ttu-id="b8e18-161">Разделы реестра, которые отображаются в служебной программе RegEdt32 как ряд строк, разделенных пробелами, находятся в <strong>REG_MULTI_SZ</strong> формате данных.</span><span class="sxs-lookup"><span data-stu-id="b8e18-161">Registry keys that appear in the RegEdt32 utility as a series of strings separated by spaces are in the <strong>REG_MULTI_SZ</strong> data format.</span></span> <span data-ttu-id="b8e18-162">Дополнительные сведения см. в разделе <a href="mapping-a-registry-data-type-to-a-wmi-data-type.md">сопоставление типа данных реестра с типом данных WMI</a>.</span><span class="sxs-lookup"><span data-stu-id="b8e18-162">For more information, see <a href="mapping-a-registry-data-type-to-a-wmi-data-type.md">Mapping a Registry Data Type to a WMI Data Type</a>.</span></span> <span data-ttu-id="b8e18-163">Следующий пример кода VBScript создает новый ключ и новое многострочное значение.</span><span class="sxs-lookup"><span data-stu-id="b8e18-163">The following VBScript code example creates a new key and a new multistring value.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b8e18-164">VB</span><span class="sxs-lookup"><span data-stu-id="b8e18-164">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>const HKEY_LOCAL_MACHINE = &H80000002
strKeyPath = &quot;SOFTWARE\NewKey&quot;
MultValueName = &quot;Example Multistring Value&quot;
strComputer = &quot;.&quot;
iValues = Array(&quot;string1&quot;, &quot;string2&quot;)
Set oReg=GetObject(&quot;winmgmts:{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\default:StdRegProv&quot;)
oReg.CreateKey HKEY_LOCAL_MACHINE,strKeyPath
oReg.SetMultiStringValue HKEY_LOCAL_MACHINE,strKeyPath,MultValueName,iValues</code></pre></td>
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
<th><span data-ttu-id="b8e18-165">PowerShell</span><span class="sxs-lookup"><span data-stu-id="b8e18-165">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$HKEY_Local_Machine =2147483650 
$computer =&#39;.&#39;
$reg = [WMIClass]&quot;ROOT\DEFAULT:StdRegProv&quot;
$Key       = &quot;SOFTWARE\NewKey&quot;
$ValueName = &quot;Example MultiString Value&quot;
$Values     = @(&quot;Thomas&quot;, &quot;Susan&quot;, &quot;Rebecca&quot;)
$Key       = &quot;SOFTWARE\NewKey&quot;
$results   = $reg.SetMultiStringValue($HKEY_LOCAL_MACHINE, $Key, $ValueName, $Values)
If ($results.Returnvalue -eq 0) {&quot;Value Set&quot;} </code></pre></td>
</tr>
</tbody>
</table>

</div>
<p><span data-ttu-id="b8e18-166">Следующий скрипт считывает многострочное значение.</span><span class="sxs-lookup"><span data-stu-id="b8e18-166">The following script reads the multistring value.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b8e18-167">VB</span><span class="sxs-lookup"><span data-stu-id="b8e18-167">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>const HKEY_LOCAL_MACHINE = &H80000002
strKeyPath = &quot;SOFTWARE\NewKey&quot;
strComputer = &quot;.&quot;
iValues = Array(&quot;string1&quot;, &quot;string2&quot;)
Set oReg=GetObject(&quot;winmgmts:{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\default:StdRegProv&quot;)
MultValueName = &quot;Example Multistring Value&quot;
oReg.GetMultiStringValue HKEY_LOCAL_MACHINE,strKeyPath,MultValueName,iValues
For Each strValue In iValues
WScript.echo strValue
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
<th><span data-ttu-id="b8e18-168">PowerShell</span><span class="sxs-lookup"><span data-stu-id="b8e18-168">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code># Define Constants
$HKEY_Local_Machine =2147483650 
$computer =&#39;.&#39;
$reg = [WMIClass]&quot;ROOT\DEFAULT:StdRegProv&quot;
$Key       = &quot;SOFTWARE\NewKey&quot;
$ValueName = &quot;Example MultiString Value&quot;
$results   = $reg.GetMultiStringValue($HKEY_LOCAL_MACHINE, $Key, $ValueName)
$results.svalue</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b8e18-169">... удалить раздел реестра?</span><span class="sxs-lookup"><span data-stu-id="b8e18-169">...remove a registry key?</span></span></td>
<td><p><span data-ttu-id="b8e18-170">Используйте класс <a href="/previous-versions/windows/desktop/regprov/stdregprov"><strong>стдрегпров</strong></a> , расположенный в пространстве имен root\default и методах <a href="/previous-versions/windows/desktop/regprov/deletevalue-method-in-class-stdregprov"><strong>DeleteKey</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="b8e18-170">Use the <a href="/previous-versions/windows/desktop/regprov/stdregprov"><strong>StdRegProv</strong></a> class, located in root\default namespace and the <a href="/previous-versions/windows/desktop/regprov/deletevalue-method-in-class-stdregprov"><strong>DeleteKey</strong></a> methods.</span></span></p>
<div class="code">
<span data-codelanguage="PowerShell"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b8e18-171">PowerShell</span><span class="sxs-lookup"><span data-stu-id="b8e18-171">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$HKEY_Local_Machine =2147483650 
$computer =&#39;.&#39;
$reg = [WMIClass]&quot;ROOT\DEFAULT:StdRegProv&quot;
$Key     = &quot;SOFTWARE\NewKey&quot;
$results   = $reg.DeleteKey($HKEY_LOCAL_MACHINE, $Key)
If ($results.Returnvalue -eq 0) {&quot;Key Removed&quot;} </code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="b8e18-172">См. также</span><span class="sxs-lookup"><span data-stu-id="b8e18-172">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b8e18-173">Задачи WMI для скриптов и приложений</span><span class="sxs-lookup"><span data-stu-id="b8e18-173">WMI Tasks for Scripts and Applications</span></span>](wmi-tasks-for-scripts-and-applications.md)
</dt> <dt>

[<span data-ttu-id="b8e18-174">Примеры приложений WMI на C++</span><span class="sxs-lookup"><span data-stu-id="b8e18-174">WMI C++ Application Examples</span></span>](wmi-c---application-examples.md)
</dt> <dt>

[<span data-ttu-id="b8e18-175">Скриптцентер TechNet</span><span class="sxs-lookup"><span data-stu-id="b8e18-175">TechNet ScriptCenter</span></span>](https://www.microsoft.com/technet/scriptcenter)
</dt> <dt>

[<span data-ttu-id="b8e18-176">Изменение системного реестра</span><span class="sxs-lookup"><span data-stu-id="b8e18-176">Modifying the System Registry</span></span>](modifying-the-system-registry.md)
</dt> <dt>

[<span data-ttu-id="b8e18-177">**стдрегпров**</span><span class="sxs-lookup"><span data-stu-id="b8e18-177">**StdRegProv**</span></span>](/previous-versions/windows/desktop/regprov/stdregprov)
</dt> </dl>
