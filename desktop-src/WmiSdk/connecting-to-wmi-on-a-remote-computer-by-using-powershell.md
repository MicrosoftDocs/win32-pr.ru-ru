---
description: Удаленное подключение к инструментарию WMI с помощью PowerShell
ms.assetid: 9a06f0c3-2845-48aa-9988-79cc4607ce19
ms.tgt_platform: multiple
title: Удаленное подключение к инструментарию WMI с помощью PowerShell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a2bb1ad982a20a10dbadd89856d118f1be9bd82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103812664"
---
# <a name="connecting-to-wmi-remotely-with-powershell"></a><span data-ttu-id="4990c-103">Удаленное подключение к инструментарию WMI с помощью PowerShell</span><span class="sxs-lookup"><span data-stu-id="4990c-103">Connecting to WMI Remotely with PowerShell</span></span>

<span data-ttu-id="4990c-104">Windows PowerShell предоставляет простой механизм подключения к инструментарий управления Windows (WMI) (WMI) на удаленном компьютере.</span><span class="sxs-lookup"><span data-stu-id="4990c-104">Windows PowerShell provides a simple mechanism to connect to Windows Management Instrumentation (WMI) on a remote computer.</span></span> <span data-ttu-id="4990c-105">На удаленные подключения в WMI влияют [Брандмауэр Windows](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc754274(v=ws.11)), параметры DCOM и [Управление учетными записями пользователей (UAC)](/previous-versions/aa905108(v=msdn.10)).</span><span class="sxs-lookup"><span data-stu-id="4990c-105">Remote connections in WMI are affected by the [Windows Firewall](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc754274(v=ws.11)), DCOM settings, and [User Account Control (UAC)](/previous-versions/aa905108(v=msdn.10)).</span></span> <span data-ttu-id="4990c-106">Дополнительные сведения о настройке удаленных соединений см. [в статье удаленное подключение к WMI, начиная с Windows Vista](connecting-to-wmi-remotely-starting-with-vista.md).</span><span class="sxs-lookup"><span data-stu-id="4990c-106">For more information about configuring remote connections, see [Connecting to WMI Remotely Starting with Windows Vista](connecting-to-wmi-remotely-starting-with-vista.md).</span></span>

<span data-ttu-id="4990c-107">Примеры в этом разделе основаны на сценариях VBScript при [подключении к инструментарию WMI на удаленном компьютере](connecting-to-wmi-on-a-remote-computer.md).</span><span class="sxs-lookup"><span data-stu-id="4990c-107">The examples in this topic are based on the VBScripts from [Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span></span> <span data-ttu-id="4990c-108">Во всех примерах в этом разделе используется командлет [Get-WmiObject](/previous-versions//dd315295(v=technet.10)) .</span><span class="sxs-lookup"><span data-stu-id="4990c-108">All of the examples in this topic use the [Get-WmiObject](/previous-versions//dd315295(v=technet.10)) cmdlet.</span></span> <span data-ttu-id="4990c-109">Дополнительные сведения см. в разделе [Get-WmiObject](/previous-versions//dd315295(v=technet.10)).</span><span class="sxs-lookup"><span data-stu-id="4990c-109">For more information, see [Get-WmiObject](/previous-versions//dd315295(v=technet.10)).</span></span>

## <a name="windows-powershell-examples"></a><span data-ttu-id="4990c-110">Примеры Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="4990c-110">Windows PowerShell examples</span></span>

<span data-ttu-id="4990c-111">При создании подключения к удаленному компьютеру пользователь может указать такие сведения о соединении, как имя удаленного компьютера, учетные данные и уровень проверки подлинности для подключения.</span><span class="sxs-lookup"><span data-stu-id="4990c-111">When creating a connection to a remote computer, a user can specify the connection information such as the remote computer name, credentials, and the authentication level for the connection.</span></span> <span data-ttu-id="4990c-112">В следующих примерах показано, как подключиться к удаленному компьютеру с помощью различных наборов учетных данных и как получить доступ к сведениям WMI.</span><span class="sxs-lookup"><span data-stu-id="4990c-112">The following examples illustrate how to connect to a remote computer by using different sets of credentials and how to access WMI information.</span></span>

<span data-ttu-id="4990c-113">В следующем примере Windows PowerShell показана настройка уровня олицетворения.</span><span class="sxs-lookup"><span data-stu-id="4990c-113">The following Windows PowerShell example shows setting the impersonation level:</span></span>


```PowerShell

Get-WmiObject -Namespace "root\cimv2" -Class Win32_Process -Impersonation 3 -ComputerName Computer_B
```



<span data-ttu-id="4990c-114">В предыдущем примере пользователь подключается к удаленному компьютеру, используя те же учетные данные (домен и имя пользователя), в которых они вошли.</span><span class="sxs-lookup"><span data-stu-id="4990c-114">In the preceding example, the user connects to a remote computer by using the same credentials (domain and user name) that they logged on with.</span></span> <span data-ttu-id="4990c-115">Пользователь также запросил использовать олицетворение.</span><span class="sxs-lookup"><span data-stu-id="4990c-115">The user also requested to use impersonation.</span></span> <span data-ttu-id="4990c-116">В отличие от исходного примера VBScript, строка моникера не требуется, так как уровень олицетворения задается свойством "Impersonation".</span><span class="sxs-lookup"><span data-stu-id="4990c-116">Unlike the original VBScript example, a moniker string is not needed because the impersonation level is set by the "Impersonation" property.</span></span> <span data-ttu-id="4990c-117">По умолчанию уровень олицетворения устанавливается равным 3 (IMPERSONATE).</span><span class="sxs-lookup"><span data-stu-id="4990c-117">By default, the impersonation level is set to 3 (Impersonate).</span></span>

<span data-ttu-id="4990c-118">В примере перечисляются все экземпляры класса [**\_ процесса Win32**](/windows/desktop/CIMWin32Prov/win32-process) , которые выполняются на удаленном компьютере.</span><span class="sxs-lookup"><span data-stu-id="4990c-118">The example lists all the instances of the [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process) class that are running on remote computer.</span></span>

> [!Note]  
> <span data-ttu-id="4990c-119">Необходимо указать пространство имен WMI для подключения к удаленному компьютеру, так как пространство имен по умолчанию не совпадает на разных компьютерах.</span><span class="sxs-lookup"><span data-stu-id="4990c-119">You should specify the WMI namespace to connect to on the remote computer because it is possible that the default namespace is not the same on different computers.</span></span>

 

<span data-ttu-id="4990c-120">В следующем примере Windows PowerShell показано, как подключиться к удаленному компьютеру с другими учетными данными и установить уровень олицетворения равным 3, что является олицетворением.</span><span class="sxs-lookup"><span data-stu-id="4990c-120">The following Windows PowerShell example shows how to connect to a remote computer with different credentials and to set the impersonation level to 3, which is Impersonate:</span></span>


```PowerShell

$Computer = "atl-dc-01"

Get-WmiObject -Namespace "root\cimv2" -Class Win32_Process -Impersonation 3 -Credential `
FABRIKAM\administrator -ComputerName $Computer
```



<span data-ttu-id="4990c-121">В предыдущем примере имя компьютера было назначено переменной $Computer.</span><span class="sxs-lookup"><span data-stu-id="4990c-121">In the preceding example, the computer name was assigned to the $Computer variable.</span></span> <span data-ttu-id="4990c-122">Пользователь подключается к удаленному компьютеру, используя определенные учетные данные (имя домена и пользователя) и запрашивает олицетворение для уровня проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="4990c-122">The user connects to a remote computer by using specific credentials (domain and user name) and requests impersonation for the authentication level.</span></span>

> [!Note]  
> <span data-ttu-id="4990c-123">Знак ударения-ударения ( \` ) используется для обозначения разрыва строки.</span><span class="sxs-lookup"><span data-stu-id="4990c-123">The grave-accent character (\`) is used to indicate a line break.</span></span> <span data-ttu-id="4990c-124">Он эквивалентен символу подчеркивания ( \_ ) в VBScript.</span><span class="sxs-lookup"><span data-stu-id="4990c-124">It is equivalent to the underscore character (\_) in VBScript.</span></span>

 

<span data-ttu-id="4990c-125">Следующий пример Windows PowerShell подключается к группе удаленных компьютеров в том же домене, создавая массив имен удаленных компьютеров, а затем отображая имена самонастраивающийся устройств — экземпляры [**Win32 \_ пнпентити**](/windows/desktop/CIMWin32Prov/win32-pnpentity)— на каждом компьютере:</span><span class="sxs-lookup"><span data-stu-id="4990c-125">The following Windows PowerShell example connects to a group of remote computers in the same domain by creating an array of remote computer names and then displaying names of the Plug and Play devices—instances of [**Win32\_PnPEntity**](/windows/desktop/CIMWin32Prov/win32-pnpentity)—on each computer:</span></span>


```PowerShell
$ArrComputers = "Computer1", "Computer2", "Computer3"
foreach ($Computer in $ArrComputers) 
{
write-host ""
write-host "===================================="
write-host "Computer: $Computer"
write-host "===================================="

write-host "-----------------------------------"
write-host "Win32_PnPEntity instance"
write-host "-----------------------------------"

$ColItems = Get-WmiObject -Class Win32_PnPEntity -Namespace "root\cimv2" -Computer $Computer
$ColItems[0..47] | Format-List Name, Status
}
```



> [!Note]  
> <span data-ttu-id="4990c-126">Чтобы запустить предыдущий сценарий Windows PowerShell, необходимо быть администратором на удаленных компьютерах.</span><span class="sxs-lookup"><span data-stu-id="4990c-126">To run the preceding Windows PowerShell script, you must be an administrator on the remote computers.</span></span> <span data-ttu-id="4990c-127">Кроме того, в отношении предыдущего примера обратите внимание на следующее:</span><span class="sxs-lookup"><span data-stu-id="4990c-127">Also, relating to the preceding example, note the following:</span></span>

 

-   <span data-ttu-id="4990c-128">Имена компьютеров в массиве должны быть заключены в кавычки, так как они являются строками.</span><span class="sxs-lookup"><span data-stu-id="4990c-128">The computer names in the array must be enclosed in quotation marks because they are strings.</span></span>
-   <span data-ttu-id="4990c-129">Объекты, возвращаемые [Get-WmiObject](/previous-versions//dd315295(v=technet.10)) , присваиваются переменной $ColItems.</span><span class="sxs-lookup"><span data-stu-id="4990c-129">The objects returned by the [Get-WmiObject](/previous-versions//dd315295(v=technet.10)) are assigned to the $ColItems variable.</span></span>
-   <span data-ttu-id="4990c-130">Оператор Range \[ \] ограничивает список самонастраивающийсяных устройств до 48 экземпляров.</span><span class="sxs-lookup"><span data-stu-id="4990c-130">The range operator \[\] limited the list of Plug and Play devices to 48 instances.</span></span> <span data-ttu-id="4990c-131">Дополнительные сведения см. в разделе [About \_ Operators](/previous-versions//dd347588(v=technet.10)).</span><span class="sxs-lookup"><span data-stu-id="4990c-131">For more information, see [About\_Operators](/previous-versions//dd347588(v=technet.10)).</span></span>
-   <span data-ttu-id="4990c-132">" \| " — Это символ конвейера.</span><span class="sxs-lookup"><span data-stu-id="4990c-132">The "\|" is the pipeline character.</span></span> <span data-ttu-id="4990c-133">Объект, возвращаемый функцией Колитемс, отправляется в командлет [Format-List]( /previous-versions//dd347700(v=technet.10)) .</span><span class="sxs-lookup"><span data-stu-id="4990c-133">The object returned by ColItems is sent to the [Format-List]( /previous-versions//dd347700(v=technet.10)) cmdlet.</span></span>

<span data-ttu-id="4990c-134">Следующий пример Windows PowerShell позволяет подключиться к удаленному компьютеру в другом домене.</span><span class="sxs-lookup"><span data-stu-id="4990c-134">The following Windows PowerShell example enables you to connect to a remote computer on a different domain.</span></span> <span data-ttu-id="4990c-135">В этом примере также отображаются имена процессов для экземпляров [**\_ процесса Win32**](/windows/desktop/CIMWin32Prov/win32-process) на удаленном компьютере.</span><span class="sxs-lookup"><span data-stu-id="4990c-135">This example also displays the process names for instances of [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process) on the remote computer.</span></span>


```PowerShell
$Computer = "FullComputerName" 
$Domain = "DOMAIN"
$Credential = Get-Credential
$ColItems = Get-WmiObject -Class Win32_Process -Authority "ntlmdomain:$Domain" `
-Credential $Credential -Locale "MS_409" -Namespace "root\cimv2"  -ComputerName $Computer

foreach ($ObjItem in $colItems) 
{
write-host "Process Name:" $ObjItem.name
}
```



> [!Note]  
> <span data-ttu-id="4990c-136">Чтобы запустить предыдущий сценарий Windows PowerShell, необходимо быть администратором на удаленном компьютере.</span><span class="sxs-lookup"><span data-stu-id="4990c-136">To run the preceding Windows PowerShell script, you must be an administrator on the remote computer.</span></span>

 

<span data-ttu-id="4990c-137">В предыдущем примере пользователь подключается к удаленному компьютеру в другом домене и указывает предпочтительный языковой стандарт.</span><span class="sxs-lookup"><span data-stu-id="4990c-137">In the preceding example, the user connects to a remote computer on a different domain and specifies a preferred locale.</span></span> <span data-ttu-id="4990c-138">Команда [Get-Credential](/previous-versions//dd315327(v=technet.10)) запрашивает учетные данные пользователя и назначает учетные данные объекту.</span><span class="sxs-lookup"><span data-stu-id="4990c-138">The [Get-Credential](/previous-versions//dd315327(v=technet.10)) command requests the user's credentials and assigns the credentials to an object.</span></span> <span data-ttu-id="4990c-139">В примере также перечислены имена экземпляров класса [**\_ процесса Win32**](/windows/desktop/CIMWin32Prov/win32-process) , которые выполняются на компьютере.</span><span class="sxs-lookup"><span data-stu-id="4990c-139">The example also lists the names of instances of the [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process) class that are running on the computer.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4990c-140">См. также</span><span class="sxs-lookup"><span data-stu-id="4990c-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4990c-141">Подключение к инструментарию WMI на удаленном компьютере</span><span class="sxs-lookup"><span data-stu-id="4990c-141">Connecting to WMI on a Remote Computer</span></span>](connecting-to-wmi-on-a-remote-computer.md)
</dt> </dl>

 

 
