---
description: Описывает, как сценарии, приложения и поставщики могут устанавливать подключения к инструментарию WMI на удаленных компьютерах для получения данных, управления оборудованием и программным обеспечением.
ms.assetid: 16b00ee3-f721-4912-9e8e-2fdbc897a813
ms.tgt_platform: multiple
title: Подключение к инструментарию WMI на удаленном компьютере
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80d581d1be73013e57ef2193102f6e8afc287b05
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674069"
---
# <a name="connecting-to-wmi-on-a-remote-computer"></a><span data-ttu-id="4f7a6-103">Подключение к инструментарию WMI на удаленном компьютере</span><span class="sxs-lookup"><span data-stu-id="4f7a6-103">Connecting to WMI on a Remote Computer</span></span>

<span data-ttu-id="4f7a6-104">Инструментарий WMI можно использовать для управления и доступа к данным WMI на удаленных компьютерах.</span><span class="sxs-lookup"><span data-stu-id="4f7a6-104">WMI can be used to manage and access WMI data on remote computers.</span></span> <span data-ttu-id="4f7a6-105">На удаленные подключения в WMI влияют параметры [брандмауэра Windows](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc754274(v=ws.11)) и DCOM.</span><span class="sxs-lookup"><span data-stu-id="4f7a6-105">Remote connections in WMI are affected by the [Windows Firewall](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc754274(v=ws.11)) and DCOM settings.</span></span> <span data-ttu-id="4f7a6-106">Для [контроля учетных записей (UAC)](/previous-versions/aa905108(v=msdn.10)) также могут потребоваться изменения некоторых параметров.</span><span class="sxs-lookup"><span data-stu-id="4f7a6-106">[User Account Control (UAC)](/previous-versions/aa905108(v=msdn.10)) may also require changes to some settings.</span></span> <span data-ttu-id="4f7a6-107">Однако после настройки параметров вызов удаленной системы будет очень похож на локальный вызов WMI.</span><span class="sxs-lookup"><span data-stu-id="4f7a6-107">However, once your have your settings correct, the call to a remote system is very similar to a local WMI call.</span></span> <span data-ttu-id="4f7a6-108">Тем не менее, вы можете сделать его более сложным, используя разные учетные данные, альтернативные протоколы проверки подлинности и другие функции безопасности.</span><span class="sxs-lookup"><span data-stu-id="4f7a6-108">You may choose to make it more complex however, by using different credentials, alternate authentication protocols, and other security features.</span></span>

## <a name="configuring-a-computer-for-a-remote-connection"></a><span data-ttu-id="4f7a6-109">Настройка компьютера для удаленного подключения</span><span class="sxs-lookup"><span data-stu-id="4f7a6-109">Configuring a Computer for a Remote Connection</span></span>

<span data-ttu-id="4f7a6-110">Прежде чем получить доступ к удаленной системе с помощью инструментария WMI, может потребоваться проверить некоторые параметры безопасности, чтобы убедиться, что у вас есть доступ.</span><span class="sxs-lookup"><span data-stu-id="4f7a6-110">Before you can access a remote system with WMI, you may need to check some security settings to confirm that you have access.</span></span> <span data-ttu-id="4f7a6-111">В частности, внесены следующие изменения.</span><span class="sxs-lookup"><span data-stu-id="4f7a6-111">Specifically:</span></span>

-   <span data-ttu-id="4f7a6-112">Windows содержит ряд функций безопасности, которые могут блокировать доступ к сценариям в удаленных системах.</span><span class="sxs-lookup"><span data-stu-id="4f7a6-112">Windows contains a number of security features that may block access to scripts on remote systems.</span></span> <span data-ttu-id="4f7a6-113">Таким образом, может потребоваться изменить параметры системы Active Directory и брандмауэра Windows перед вызовом инструментария WMI.</span><span class="sxs-lookup"><span data-stu-id="4f7a6-113">As such, you may need to modify your system's Active Directory and Windows Firewall settings before making a WMI call.</span></span> <span data-ttu-id="4f7a6-114">Дополнительные сведения см. в разделе [Настройка удаленного WMI-подключения](connecting-to-wmi-remotely-starting-with-vista.md) и [Устранение неполадок удаленного WMI-подключения](troubleshooting-a-remote-wmi-connection.md).</span><span class="sxs-lookup"><span data-stu-id="4f7a6-114">For more information, see [Setting up a Remote WMI Connection](connecting-to-wmi-remotely-starting-with-vista.md) and [Troubleshooting a Remote WMI Connection](troubleshooting-a-remote-wmi-connection.md).</span></span>

-   <span data-ttu-id="4f7a6-115">Чтобы удаленное подключение работало, необходимо включить правильные параметры DCOM.</span><span class="sxs-lookup"><span data-stu-id="4f7a6-115">The correct DCOM settings must be enabled for a remote connection to work.</span></span> <span data-ttu-id="4f7a6-116">Изменение параметров DCOM позволяет пользователям с ограниченными правами получать доступ к компьютеру для удаленного подключения.</span><span class="sxs-lookup"><span data-stu-id="4f7a6-116">Changing DCOM settings can allow low rights users access to a computer for a remote connection.</span></span> <span data-ttu-id="4f7a6-117">Дополнительные сведения см. [в разделе Защита удаленного WMI-подключения](securing-a-remote-wmi-connection.md).</span><span class="sxs-lookup"><span data-stu-id="4f7a6-117">For more information, see [Securing a Remote WMI Connection](securing-a-remote-wmi-connection.md).</span></span>

<span data-ttu-id="4f7a6-118">Кроме того, в некоторых случаях может потребоваться запустить Инструментарий WMI, хотя фиксированный порт.</span><span class="sxs-lookup"><span data-stu-id="4f7a6-118">In addition, there may be some circumstances in which you may wish to run WMI though a fixed port.</span></span> <span data-ttu-id="4f7a6-119">Для этого также потребуется изменить параметры.</span><span class="sxs-lookup"><span data-stu-id="4f7a6-119">To do this, you will also need to change your settings.</span></span> <span data-ttu-id="4f7a6-120">Дополнительные сведения см. [в разделе Настройка фиксированного порта для WMI](setting-up-a-fixed-port-for-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="4f7a6-120">For more information, see [Setting Up a Fixed Port for WMI](setting-up-a-fixed-port-for-wmi.md).</span></span>

## <a name="connecting-to-a-remote-computer"></a><span data-ttu-id="4f7a6-121">Подключение к удаленному компьютеру</span><span class="sxs-lookup"><span data-stu-id="4f7a6-121">Connecting to a Remote Computer</span></span>

<span data-ttu-id="4f7a6-122">По сути, подключение к удаленной системе с помощью инструментария WMI состоит в том, что у вас есть соответствующие разрешения на доступ к системе и правильно настроено подключение.</span><span class="sxs-lookup"><span data-stu-id="4f7a6-122">At its heart, connecting to a remote system with WMI consists of making sure that you have the appropriate permissions to access the system, and that your connection is properly configured.</span></span> <span data-ttu-id="4f7a6-123">После получения этих двух элементов соединение само по себе является сравнительно простым.</span><span class="sxs-lookup"><span data-stu-id="4f7a6-123">Once you have those two elements, the connection itself is relatively simple.</span></span> <span data-ttu-id="4f7a6-124">Например, если вы используете учетные данные безопасности по умолчанию, вы можете получить доступ к инструментарию WMI в удаленной системе, используя следующий код:</span><span class="sxs-lookup"><span data-stu-id="4f7a6-124">For example, if you are using your default security credentials, you can access WMI on a remote system using the following code:</span></span>

<dl> <dt>

<span data-ttu-id="4f7a6-125"><span id="Connecting_to_WMI_Remotely_with_PowerShell"></span><span id="connecting_to_wmi_remotely_with_powershell"></span><span id="CONNECTING_TO_WMI_REMOTELY_WITH_POWERSHELL"></span>[Удаленное подключение к инструментарию WMI с помощью PowerShell](connecting-to-wmi-on-a-remote-computer-by-using-powershell.md)</span><span class="sxs-lookup"><span data-stu-id="4f7a6-125"><span id="Connecting_to_WMI_Remotely_with_PowerShell"></span><span id="connecting_to_wmi_remotely_with_powershell"></span><span id="CONNECTING_TO_WMI_REMOTELY_WITH_POWERSHELL"></span>[Connecting to WMI Remotely with PowerShell](connecting-to-wmi-on-a-remote-computer-by-using-powershell.md)</span></span>
</dt> <dd>

<span data-ttu-id="4f7a6-126">Используйте параметр *-ComputerName* , общий для большинства командлетов WMI, например [Get-WmiObject](/powershell/module/microsoft.powershell.management/get-wmiobject?view=powershell-5.1&preserve-view=true).</span><span class="sxs-lookup"><span data-stu-id="4f7a6-126">Use the *-ComputerName* parameter common to most WMI cmdlets, such as [Get-WmiObject](/powershell/module/microsoft.powershell.management/get-wmiobject?view=powershell-5.1&preserve-view=true).</span></span>


```PowerShell
$strComputer = "Computer_B"
$colSettings = Get-WmiObject Win32_OperatingSystem -ComputerName $strComputer
```



</dd> <dt>

<span data-ttu-id="4f7a6-127"><span id="Connecting_to_WMI_Remotely_with_VBScript"></span><span id="connecting_to_wmi_remotely_with_vbscript"></span><span id="CONNECTING_TO_WMI_REMOTELY_WITH_VBSCRIPT"></span>[Удаленное подключение к инструментарию WMI с помощью VBScript](connecting-to-wmi-remotely-with-vbscript.md)</span><span class="sxs-lookup"><span data-stu-id="4f7a6-127"><span id="Connecting_to_WMI_Remotely_with_VBScript"></span><span id="connecting_to_wmi_remotely_with_vbscript"></span><span id="CONNECTING_TO_WMI_REMOTELY_WITH_VBSCRIPT"></span>[Connecting to WMI Remotely with VBScript](connecting-to-wmi-remotely-with-vbscript.md)</span></span>
</dt> <dd>

<span data-ttu-id="4f7a6-128">Используйте моникер, содержащий имя удаленной системы в вызове [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject).</span><span class="sxs-lookup"><span data-stu-id="4f7a6-128">Use a moniker that contains the name of the remote system in the call to [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject).</span></span>


```VB
strComputer = "Computer_B"
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colSettings = objWMIService.ExecQuery("Select * from Win32_OperatingSystem")
```



</dd> <dt>

<span data-ttu-id="4f7a6-129"><span id="Connecting_to_WMI_Remotely_with_C_"></span><span id="connecting_to_wmi_remotely_with_c_"></span><span id="CONNECTING_TO_WMI_REMOTELY_WITH_C_"></span>[Удаленное подключение к инструментарию WMI с помощью C #](connecting-to-wmi-remotely-with-c-.md)</span><span class="sxs-lookup"><span data-stu-id="4f7a6-129"><span id="Connecting_to_WMI_Remotely_with_C_"></span><span id="connecting_to_wmi_remotely_with_c_"></span><span id="CONNECTING_TO_WMI_REMOTELY_WITH_C_"></span>[Connecting to WMI Remotely with C#](connecting-to-wmi-remotely-with-c-.md)</span></span>
</dt> <dd>

<span data-ttu-id="4f7a6-130">Для текущей версии управляемого интерфейса WMI ([Microsoft. Management. Infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85))) используйте объект [CimSession](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832509(v=vs.85)) для представления подключения к удаленному узлу.</span><span class="sxs-lookup"><span data-stu-id="4f7a6-130">For the current version of the WMI managed interface ([Microsoft.Management.Infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85))), use the [CimSession](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832509(v=vs.85)) object to represent a connection to a remote host.</span></span>


```CSharp
using Microsoft.Management.Infrastructure;
...
string Namespace = @"root\cimv2";
string OSQuery = "SELECT * FROM Win32_OperatingSystem";
CimSession mySession = CimSession.Create("Computer_B");
IEnumerable<CimInstance> queryInstance = mySession.QueryInstances(Namespace, "WQL", OSQuery);
```



</dd> <dt>

<span data-ttu-id="4f7a6-131"><span id="Connecting_to_WMI_Remotely_with_C_"></span><span id="connecting_to_wmi_remotely_with_c_"></span><span id="CONNECTING_TO_WMI_REMOTELY_WITH_C_"></span>[Удаленное подключение к инструментарию WMI с помощью C #](connecting-to-wmi-remotely-with-c-.md)</span><span class="sxs-lookup"><span data-stu-id="4f7a6-131"><span id="Connecting_to_WMI_Remotely_with_C_"></span><span id="connecting_to_wmi_remotely_with_c_"></span><span id="CONNECTING_TO_WMI_REMOTELY_WITH_C_"></span>[Connecting to WMI Remotely with C#](connecting-to-wmi-remotely-with-c-.md)</span></span>
</dt> <dd>

<span data-ttu-id="4f7a6-132">Для версии v1 управляемого интерфейса WMI ([System. Management](/dotnet/api/system.management)) используйте объект [манажементскопе](/dotnet/api/system.management.managementscope) для представления подключения к удаленному узлу.</span><span class="sxs-lookup"><span data-stu-id="4f7a6-132">For the v1 version of the WMI managed interface ([System.Management](/dotnet/api/system.management)), use the [ManagementScope](/dotnet/api/system.management.managementscope) object to represent a connection to a remote host.</span></span>


```CSharp
using System.Management;
...
ManagementScope scope = new ManagementScope("\\\\Computer_B\\root\\cimv2");
scope.Connect();
ObjectQuery query = new ObjectQuery("SELECT * FROM Win32_OperatingSystem");
ManagementObjectSearcher searcher = new ManagementObjectSearcher(scope, query);
```



</dd> <dt>

<span data-ttu-id="4f7a6-133"><span id="Example__Getting_WMI_Data_from_a_Remote_Computer__C___"></span><span id="example__getting_wmi_data_from_a_remote_computer__c___"></span><span id="EXAMPLE__GETTING_WMI_DATA_FROM_A_REMOTE_COMPUTER__C___"></span>[Пример. получение данных WMI с удаленного компьютера (C++)](example--getting-wmi-data-from-a-remote-computer.md)</span><span class="sxs-lookup"><span data-stu-id="4f7a6-133"><span id="Example__Getting_WMI_Data_from_a_Remote_Computer__C___"></span><span id="example__getting_wmi_data_from_a_remote_computer__c___"></span><span id="EXAMPLE__GETTING_WMI_DATA_FROM_A_REMOTE_COMPUTER__C___"></span>[Example: Getting WMI Data from a Remote Computer (C++)](example--getting-wmi-data-from-a-remote-computer.md)</span></span>
</dt> <dd>

<span data-ttu-id="4f7a6-134">Используйте метод [**ивбемлокатор:: коннектсервер**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) , чтобы указать имя удаленного компьютера в параметре *стрнетворкресаурце* .</span><span class="sxs-lookup"><span data-stu-id="4f7a6-134">Use the [**IWbemLocator::ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) method to specify the name of the remote computer in the *strNetworkResource* parameter.</span></span>


```CSharp
    hres = pLoc->ConnectServer(
        _bstr_t(L"\\\\COMPUTER_B\\root\\cimv2"),
        _bstr_t(useToken?NULL:pszName),    // User name
        _bstr_t(useToken?NULL:pszPwd),     // User password
        NULL,                              // Locale             
        NULL,                              // Security flags
        _bstr_t(useNTLM?NULL:pszAuthority),// Authority        
        NULL,                              // Context object 
        &pSvc                              // IWbemServices proxy
        );
```



</dd> </dl>

<span data-ttu-id="4f7a6-135">Предыдущие примеры кода, вероятно, являются самым простым удаленным подключением, которое можно выполнять с помощью инструментария WMI.</span><span class="sxs-lookup"><span data-stu-id="4f7a6-135">The previous code samples are arguably the most basic remote connection you can perform with WMI.</span></span> <span data-ttu-id="4f7a6-136">В частности, в примерах предполагается следующее:</span><span class="sxs-lookup"><span data-stu-id="4f7a6-136">Specifically, the samples assume the following:</span></span>

-   <span data-ttu-id="4f7a6-137">Вы являетесь администратором на удаленном компьютере.</span><span class="sxs-lookup"><span data-stu-id="4f7a6-137">You are an administrator on the remote machine.</span></span> <span data-ttu-id="4f7a6-138">Из-за [контроля учетных записей пользователя](/previous-versions/aa905108(v=msdn.10))учетная запись в удаленной системе должна быть учетной записью домена в группе администраторов.</span><span class="sxs-lookup"><span data-stu-id="4f7a6-138">Due to [User Account Control](/previous-versions/aa905108(v=msdn.10)), the account on the remote system must be a domain account in the Administrators group.</span></span> <span data-ttu-id="4f7a6-139">Дополнительные сведения см. в разделе Управление учетными записями пользователей и инструментарий WMI.</span><span class="sxs-lookup"><span data-stu-id="4f7a6-139">For more information, see User Account Control and WMI.</span></span>
-   <span data-ttu-id="4f7a6-140">Пароль на текущем локальном компьютере не пуст.</span><span class="sxs-lookup"><span data-stu-id="4f7a6-140">The password on your current local machine is not blank.</span></span> <span data-ttu-id="4f7a6-141">По сути, это требование безопасности Windows, которое необходимо войти в систему с паролем.</span><span class="sxs-lookup"><span data-stu-id="4f7a6-141">This is essentially a Windows security requirement that you must have logged onto your system with a password.</span></span>
-   <span data-ttu-id="4f7a6-142">Как локальные, так и удаленные компьютеры находятся в одном домене.</span><span class="sxs-lookup"><span data-stu-id="4f7a6-142">Both your local and remote computers are within the same domain.</span></span> <span data-ttu-id="4f7a6-143">Если необходимо использовать междоменные границы, необходимо указать дополнительные сведения или воспользоваться немного другой моделью программирования.</span><span class="sxs-lookup"><span data-stu-id="4f7a6-143">If you need to cross domain boundaries, you would need to supply additional information or use a slightly different programming model.</span></span>
-   <span data-ttu-id="4f7a6-144">Для доступа к удаленному компьютеру используется собственная учетная запись.</span><span class="sxs-lookup"><span data-stu-id="4f7a6-144">You are using your own account to access the remote machine.</span></span> <span data-ttu-id="4f7a6-145">Если вы пытались получить доступ к другой учетной записи, вам потребуется указать дополнительные учетные данные.</span><span class="sxs-lookup"><span data-stu-id="4f7a6-145">If you were trying to access a different account, you would need to supply additional credentials.</span></span> <span data-ttu-id="4f7a6-146">(Обратите внимание, что попытка доступа к инструментарию WMI локально с учетными данными, отличными от текущей учетной записи, не разрешено)</span><span class="sxs-lookup"><span data-stu-id="4f7a6-146">(Note that trying to access WMI locally with credentials different than your current account is not permitted.)</span></span>
-   <span data-ttu-id="4f7a6-147">Оба компьютера работают под управлением IPv6.</span><span class="sxs-lookup"><span data-stu-id="4f7a6-147">Both computers are running IPv6.</span></span> <span data-ttu-id="4f7a6-148">WMI поддерживает подключения к компьютерам с IPv6.</span><span class="sxs-lookup"><span data-stu-id="4f7a6-148">WMI supports connections to computers running IPv6.</span></span> <span data-ttu-id="4f7a6-149">Однако на локальном компьютере и компьютере \_ B должен быть установлен протокол IPv6.</span><span class="sxs-lookup"><span data-stu-id="4f7a6-149">However, both your local machine and "Computer\_B" must be running IPv6.</span></span> <span data-ttu-id="4f7a6-150">На одном из компьютеров может также работать протокол IPv4.</span><span class="sxs-lookup"><span data-stu-id="4f7a6-150">Either computer may be running IPv4 also.</span></span> <span data-ttu-id="4f7a6-151">Дополнительные сведения см. [в разделе Поддержка IPv6 и IPv4 в WMI](ipv6-and-ipv4-support-in-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="4f7a6-151">For more information, see [IPv6 and IPv4 Support in WMI](ipv6-and-ipv4-support-in-wmi.md).</span></span>
-   <span data-ttu-id="4f7a6-152">Ваш сценарий не обязан делегировать, т. е. ему не требуется доступ к дополнительным удаленным компьютерам через Целевой Удаленный компьютер.</span><span class="sxs-lookup"><span data-stu-id="4f7a6-152">Your script does not need to delegate - that is, it does not need to access additional remote computers through the targeted remote computer.</span></span> <span data-ttu-id="4f7a6-153">Дополнительные сведения см. в разделе [делегирование с помощью WMI](connecting-to-a-3rd-computer-delegation.md).</span><span class="sxs-lookup"><span data-stu-id="4f7a6-153">For more information, see [Delegating with WMI](connecting-to-a-3rd-computer-delegation.md).</span></span>
-   <span data-ttu-id="4f7a6-154">Вы пытаетесь выполнить конкретный вызов, а не создавать удаленный процесс.</span><span class="sxs-lookup"><span data-stu-id="4f7a6-154">You are trying to make a specific call, rather than creating a remote process.</span></span> <span data-ttu-id="4f7a6-155">Дополнительные сведения см. в статье [Удаленное создание процессов с помощью WMI](creating-processes-remotely.md).</span><span class="sxs-lookup"><span data-stu-id="4f7a6-155">For more information, see [Creating Processes Remotely using WMI](creating-processes-remotely.md).</span></span>

<span data-ttu-id="4f7a6-156">Учитывая эти ограничения, удаленный вызов WMI очень напоминает локальный вызов WMI. Единственное отличие заключается в том, что необходимо указать имя удаленной системы.</span><span class="sxs-lookup"><span data-stu-id="4f7a6-156">With those restrictions in mind, a remote WMI call is very similar to a local WMI call - the only difference being that you must specify the name of the remote system.</span></span> <span data-ttu-id="4f7a6-157">Однако вы можете изменить многие из этих функций: использовать другие учетные данные или маршрутизацию вызова через другой компьютер или доступ к другому домену.</span><span class="sxs-lookup"><span data-stu-id="4f7a6-157">However, you may choose to change many of those features: using different credentials, or routing your call through a 3rd party computer, or accessing a different domain.</span></span>

 

 
