---
description: Для получения данных из инструментария WMI (на локальном или удаленном компьютере) необходимо подключиться к службе WMI, подключившись к определенному пространству имен.
ms.assetid: 71ff6b06-af7d-43ee-ae6e-1964ec249472
ms.tgt_platform: multiple
title: Задачи WMI. подключение к службе WMI
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 751c6c0802c30e113f4a2b7ddc646cdf5646b7dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105702055"
---
# <a name="wmi-tasks-connecting-to-the-wmi-service"></a><span data-ttu-id="ec14b-103">Задачи WMI. подключение к службе WMI</span><span class="sxs-lookup"><span data-stu-id="ec14b-103">WMI Tasks: Connecting to the WMI Service</span></span>

<span data-ttu-id="ec14b-104">Для получения данных из инструментария WMI (на локальном или удаленном компьютере) необходимо подключиться к службе WMI, подключившись к определенному [*пространству имен*](gloss-n.md).</span><span class="sxs-lookup"><span data-stu-id="ec14b-104">To get data from WMI, either on the local computer or from a remote computer, you must connect to the WMI service by connecting to a specific [*namespace*](gloss-n.md).</span></span> <span data-ttu-id="ec14b-105">В большинстве случаев используйте сокращенное подключение [моникера](creating-a-wmi-script.md) или подключение [**локатора**](swbemlocator-connectserver.md) .</span><span class="sxs-lookup"><span data-stu-id="ec14b-105">In most cases, use either the shorthand [moniker](creating-a-wmi-script.md) connection or the [**Locator**](swbemlocator-connectserver.md) connection.</span></span> <span data-ttu-id="ec14b-106">Другие примеры см. в разделе TechNet Скриптцентер по адресу [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx) .</span><span class="sxs-lookup"><span data-stu-id="ec14b-106">For other examples, see the TechNet ScriptCenter at [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx).</span></span>

<span data-ttu-id="ec14b-107">Для удаленных подключений требуются соответствующие параметры брандмауэра Windows и DCOM.</span><span class="sxs-lookup"><span data-stu-id="ec14b-107">Remote connections require proper settings for the Windows Firewall and DCOM.</span></span> <span data-ttu-id="ec14b-108">Дополнительные сведения см. в статьях [Подключение к WMI на удаленном компьютере](connecting-to-wmi-on-a-remote-computer.md) и [подключение через брандмауэр Windows](/windows/desktop/WmiSdk/connecting-to-wmi-remotely-starting-with-vista).</span><span class="sxs-lookup"><span data-stu-id="ec14b-108">For more information, see [Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md) and [Connecting Through Windows Firewall](/windows/desktop/WmiSdk/connecting-to-wmi-remotely-starting-with-vista).</span></span> <span data-ttu-id="ec14b-109">Начиная с Windows Vista Управление учетными записями пользователей (UAC) может повлиять на доступ к WMI.</span><span class="sxs-lookup"><span data-stu-id="ec14b-109">Starting with Windows Vista, User Account Control (UAC) can affect WMI access.</span></span> <span data-ttu-id="ec14b-110">Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](user-account-control-and-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="ec14b-110">For more information, see [User Account Control and WMI](user-account-control-and-wmi.md).</span></span>

<span data-ttu-id="ec14b-111">Примеры сценариев, приведенные в этом разделе, получают данные только с локального компьютера.</span><span class="sxs-lookup"><span data-stu-id="ec14b-111">The script examples shown in this topic obtain data only from the local computer.</span></span> <span data-ttu-id="ec14b-112">Дополнительные сведения об использовании сценария для получения данных с удаленных компьютеров см. в разделе [Подключение к WMI на удаленном компьютере](connecting-to-wmi-on-a-remote-computer.md).</span><span class="sxs-lookup"><span data-stu-id="ec14b-112">For more information about how to use the script to obtain data from remote computers, see [Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span></span>


<span data-ttu-id="ec14b-113">В следующей процедуре описывается выполнение скрипта.</span><span class="sxs-lookup"><span data-stu-id="ec14b-113">The following procedure describes how to run a script.</span></span>

<span data-ttu-id="ec14b-114">**Запуск сценария**</span><span class="sxs-lookup"><span data-stu-id="ec14b-114">**To run a script**</span></span>

1.  <span data-ttu-id="ec14b-115">Скопируйте код и сохраните его в файле с расширением vbs, например *filename.vbs*.</span><span class="sxs-lookup"><span data-stu-id="ec14b-115">Copy the code and save it in a file with a .vbs extension, such as *filename.vbs*.</span></span> <span data-ttu-id="ec14b-116">Убедитесь, что текстовый редактор не добавляет расширение txt в файл.</span><span class="sxs-lookup"><span data-stu-id="ec14b-116">Ensure that your text editor does not add a .txt extension to the file.</span></span>
2.  <span data-ttu-id="ec14b-117">Откройте окно командной строки и перейдите в каталог, в котором был сохранен файл.</span><span class="sxs-lookup"><span data-stu-id="ec14b-117">Open a command prompt window and navigate to the directory where you saved the file.</span></span>
3.  <span data-ttu-id="ec14b-118">Введите **cscript filename.vbs** в командной строке.</span><span class="sxs-lookup"><span data-stu-id="ec14b-118">Type **cscript filename.vbs** at the command prompt.</span></span>
4.  <span data-ttu-id="ec14b-119">Если доступ к журналу событий невозможен, проверьте, выполняется ли в командной строке с повышенными привилегиями.</span><span class="sxs-lookup"><span data-stu-id="ec14b-119">If you cannot access an event log, check to see if you are running from an Elevated command prompt.</span></span> <span data-ttu-id="ec14b-120">Некоторые журналы событий, например журнал событий безопасности, могут быть защищены с помощью элементов управления доступом пользователей (UAC).</span><span class="sxs-lookup"><span data-stu-id="ec14b-120">Some Event Log, such as the Security Event Log, may be protected by User Access Controls (UAC).</span></span>

> [!Note]  
> <span data-ttu-id="ec14b-121">По умолчанию Cscript отображает выходные данные скрипта в окне командной строки.</span><span class="sxs-lookup"><span data-stu-id="ec14b-121">By default, cscript displays the output of a script in the command prompt window.</span></span> <span data-ttu-id="ec14b-122">Поскольку сценарии WMI могут создавать большие объемы выходных данных, может потребоваться перенаправить выходные данные в файл.</span><span class="sxs-lookup"><span data-stu-id="ec14b-122">Because WMI scripts can produce large amounts of output, you might want to redirect the output to a file.</span></span> <span data-ttu-id="ec14b-123">Введите **cscript filename.vbs > outfile.txt** в командной строке, чтобы перенаправить выходные данные скрипта *filename.vbs* в *outfile.txt*.</span><span class="sxs-lookup"><span data-stu-id="ec14b-123">Type **cscript filename.vbs > outfile.txt** at the command prompt to redirect the output of the *filename.vbs* script to *outfile.txt*.</span></span>

 

<span data-ttu-id="ec14b-124">В следующей таблице перечислены примеры сценариев, которые можно использовать для получения различных типов данных с локального компьютера.</span><span class="sxs-lookup"><span data-stu-id="ec14b-124">The following table lists script examples that can be used to obtain various types of data from the local computer.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ec14b-125">Часто выполняемые действия в новом интерфейсе</span><span class="sxs-lookup"><span data-stu-id="ec14b-125">How do I...</span></span></th>
<th><span data-ttu-id="ec14b-126">Классы или методы WMI</span><span class="sxs-lookup"><span data-stu-id="ec14b-126">WMI classes or methods</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ec14b-127">... подключиться к удаленному компьютеру с помощью инструментария WMI?</span><span class="sxs-lookup"><span data-stu-id="ec14b-127">...connect to a remote computer using WMI?</span></span></td>
<td><span data-ttu-id="ec14b-128">Укажите один из следующих элементов в строке подключения <a href="constructing-a-moniker-string.md">моникера</a> :</span><span class="sxs-lookup"><span data-stu-id="ec14b-128">Specify one of the following as part of your <a href="constructing-a-moniker-string.md">moniker</a> connection string:</span></span><br/>
<ul>
<li><span data-ttu-id="ec14b-129">Имя компьютера NetBIOS, например &quot; ATL-DC-01&quot;</span><span class="sxs-lookup"><span data-stu-id="ec14b-129">A NetBIOS computer name, such as &quot;atl-dc-01&quot;</span></span></li>
<li><span data-ttu-id="ec14b-130">Полное доменное имя, например &quot; ATL-DC-01.fabrikam.com&quot;</span><span class="sxs-lookup"><span data-stu-id="ec14b-130">A fully qualified domain name, such as &quot;atl-dc-01.fabrikam.com&quot;</span></span></li>
<li><span data-ttu-id="ec14b-131">IPv4-адрес, например &quot; 192.168.1.1&quot;</span><span class="sxs-lookup"><span data-stu-id="ec14b-131">An IPv4 address, such as &quot;192.168.1.1&quot;</span></span></li>
<li><span data-ttu-id="ec14b-132">Начиная с Windows Vista, можно указать IPv6-адрес, если конечный компьютер и компьютер, с которого устанавливается подключение, используют протокол IPv6.</span><span class="sxs-lookup"><span data-stu-id="ec14b-132">Starting with Windows Vista, you can specify an IPv6 address if the target computer and the computer from which you are making the connection both run IPv6.</span></span><br/></li>
</ul>
<span data-ttu-id="ec14b-133">Дополнительные сведения см. в разделе <a href="connecting-to-wmi-on-a-remote-computer.md">Подключение к WMI на удаленном компьютере</a> и <a href="ipv6-and-ipv4-support-in-wmi.md">Поддержка IPv6 и IPv4 в WMI</a>.</span><span class="sxs-lookup"><span data-stu-id="ec14b-133">For more information, see <a href="connecting-to-wmi-on-a-remote-computer.md">Connecting to WMI on a Remote Computer</a> and <a href="ipv6-and-ipv4-support-in-wmi.md">IPv6 and IPv4 Support in WMI</a>.</span></span><br/> <span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ec14b-134">VB</span><span class="sxs-lookup"><span data-stu-id="ec14b-134">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;atl-dc-01&quot;
Set objWMIService = GetObject(&quot;winmgmts:&quot; & &quot;{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\cimv2&quot;)
Set colProcessList = objWMIService.ExecQuery (&quot;Select * from Win32_Process&quot;)
For Each objProcess in colProcessList
    Wscript.Echo &quot;Process Name: &quot; & objProcess.Name 
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
<th><span data-ttu-id="ec14b-135">PowerShell</span><span class="sxs-lookup"><span data-stu-id="ec14b-135">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;atl-dc-01&quot;
Get-WmiObject -Class Win32_Process -ComputerName $strComputer -Namespace &quot;root\cimv2&quot; | format-list -Property Name</code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="ec14b-136">... запустить сценарий WMI в разделе "альтернативные учетные данные"?</span><span class="sxs-lookup"><span data-stu-id="ec14b-136">...run a WMI script under alternate credentials?</span></span></td>
<td><p><span data-ttu-id="ec14b-137">Используйте метод <a href="swbemlocator-connectserver.md"><strong>SWbemLocator. коннектсервер</strong></a> или <a href="/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver"><strong>Ивбемлокатор:: коннектсервер</strong></a> в C++ и укажите соответствующие имя пользователя и пароль.</span><span class="sxs-lookup"><span data-stu-id="ec14b-137">Use the <a href="swbemlocator-connectserver.md"><strong>SWbemLocator.ConnectServer</strong></a> method, or <a href="/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver"><strong>IWbemLocator::ConnectServer</strong></a> in C++, and include the appropriate user name and password.</span></span> <span data-ttu-id="ec14b-138">При подключении к локальному компьютеру изменить учетные данные нельзя.</span><span class="sxs-lookup"><span data-stu-id="ec14b-138">You cannot change credentials when connecting to the local computer.</span></span> <span data-ttu-id="ec14b-139">Дополнительные сведения см. в статьях <a href="creating-a-wmi-script.md">Создание сценария WMI</a> и <a href="connecting-to-wmi-on-a-remote-computer.md">Подключение к WMI на удаленном компьютере</a>.</span><span class="sxs-lookup"><span data-stu-id="ec14b-139">For more information, see <a href="creating-a-wmi-script.md">Creating a WMI Script</a> and <a href="connecting-to-wmi-on-a-remote-computer.md">Connecting to WMI on a Remote Computer</a>.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ec14b-140">VB</span><span class="sxs-lookup"><span data-stu-id="ec14b-140">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>strComputer = &quot;atl-dc-01&quot;
Set objSWbemLocator = CreateObject(&quot;WbemScripting.SWbemLocator&quot;)
Set objSWbemServices = objSWbemLocator.ConnectServer (strComputer, &quot;root\cimv2&quot;, &quot;fabrikam\administrator&quot;, &quot;password&quot;)
Set colProcessList = objSWbemServices.ExecQuery(&quot;Select * From Win32_Process&quot;)
For Each objProcess in colProcessList
    Wscript.Echo &quot;Process Name: &quot; & objProcess.Name 
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
<th><span data-ttu-id="ec14b-141">PowerShell</span><span class="sxs-lookup"><span data-stu-id="ec14b-141">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$StrComputer = &quot;atl-dc-01&quot;
$strCredentials = &quot;FABRIKAM\administrator&quot;
Get-WmiObject -Class Win32_Process -ComputerName $strComputer -Namespace &quot;root\cimv2&quot; -credential $strCredentials `
   -Impersonation Impersonate | format-list -Property Name</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="ec14b-142">См. также</span><span class="sxs-lookup"><span data-stu-id="ec14b-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ec14b-143">Задачи WMI для скриптов и приложений</span><span class="sxs-lookup"><span data-stu-id="ec14b-143">WMI Tasks for Scripts and Applications</span></span>](wmi-tasks-for-scripts-and-applications.md)
</dt> <dt>

[<span data-ttu-id="ec14b-144">Примеры приложений WMI на C++</span><span class="sxs-lookup"><span data-stu-id="ec14b-144">WMI C++ Application Examples</span></span>](wmi-c---application-examples.md)
</dt> <dt>

[<span data-ttu-id="ec14b-145">Скриптцентер TechNet</span><span class="sxs-lookup"><span data-stu-id="ec14b-145">TechNet ScriptCenter</span></span>](https://www.microsoft.com/technet/scriptcenter)
</dt> </dl>

 

 



`
