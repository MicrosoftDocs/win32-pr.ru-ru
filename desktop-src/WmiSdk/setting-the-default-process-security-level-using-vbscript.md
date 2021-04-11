---
title: Задание уровня безопасности процесса по умолчанию с помощью VBScript
description: Скрипт может использовать параметры проверки подлинности и олицетворения WMI по умолчанию. Однако скрипту может потребоваться подключение с большей безопасностью или подключение к пространству имен, для которого требуется зашифрованное соединение.
ms.assetid: cb477224-3117-45e4-9271-613b58e48b6e
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03fe69228021fe8d3f36f03e60cb2366b6132f59
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272576"
---
# <a name="set-the-default-process-security-level-with-vbscript"></a><span data-ttu-id="85da5-104">Задание уровня безопасности процесса по умолчанию с помощью VBScript</span><span class="sxs-lookup"><span data-stu-id="85da5-104">Set the default process security level with VBScript</span></span>

<span data-ttu-id="85da5-105">Скрипт может использовать параметры проверки подлинности и олицетворения WMI по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="85da5-105">A script can use the default WMI authentication and impersonation settings.</span></span> <span data-ttu-id="85da5-106">Однако скрипту может потребоваться подключение с большей безопасностью или подключение к пространству имен, для которого требуется зашифрованное соединение.</span><span class="sxs-lookup"><span data-stu-id="85da5-106">However, the script may need a connection with more security or may connect to a namespace that requires an encrypted connection.</span></span> <span data-ttu-id="85da5-107">Дополнительные сведения см. в разделе [Setting Намепаце Security дескрипторы](setting-namespace-security-descriptors.md) и [требуется зашифрованное соединение с пространством имен](requiring-an-encrypted-connection-to-a-namespace.md).</span><span class="sxs-lookup"><span data-stu-id="85da5-107">For more information, see [Setting Namepace Security Descriptors](setting-namespace-security-descriptors.md) and [Requiring an Encrypted Connection to a Namespace](requiring-an-encrypted-connection-to-a-namespace.md).</span></span>

<span data-ttu-id="85da5-108">В самом простом случае скрипт может использовать параметры проверки подлинности и олицетворения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="85da5-108">In the simplest case, a script can use the default authentication and impersonation settings.</span></span> <span data-ttu-id="85da5-109">Как правило, WMI работает на узле общей службы и использует ту же проверку подлинности, что и другие процессы в узле.</span><span class="sxs-lookup"><span data-stu-id="85da5-109">WMI normally runs in a shared service host and shares the same authentication as other processes in the host.</span></span> <span data-ttu-id="85da5-110">Если вы хотите запустить процесс WMI с другим уровнем проверки подлинности, запустите WMI с помощью команды [**Winmgmt**](winmgmt.md) с параметром **/стандалонехост** и установите уровень проверки подлинности для WMI как обычно.</span><span class="sxs-lookup"><span data-stu-id="85da5-110">If you want to run the WMI process with a different level of authentication, run WMI with the [**winmgmt**](winmgmt.md) command with the **/standalonehost** switch and set the authentication level for WMI generally.</span></span> <span data-ttu-id="85da5-111">Дополнительные сведения см. в разделе [обслуживание безопасности WMI](maintaining-wmi-security.md).</span><span class="sxs-lookup"><span data-stu-id="85da5-111">For more information, see [Maintaining WMI Security](maintaining-wmi-security.md).</span></span>

<span data-ttu-id="85da5-112">Следующий скрипт использует параметры по умолчанию для уровней олицетворения и проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="85da5-112">The following script uses default settings for impersonation and authentication levels.</span></span>


```VB
strComputer = "." 
Set objServices = GetObject("winmgmts:\\" _
    & strComputer & "\root\CIMV2") 
set objProcessSet = objServices.ExecQuery _
     ("SELECT Name FROM Win32_Process",,48)
For Each Process in objProcessSet
    WScript.Echo Process.Name
Next
```



<span data-ttu-id="85da5-113">Можно также использовать [моникер](constructing-a-moniker-string.md) в вызове [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx)и задать параметры безопасности по умолчанию, как показано в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="85da5-113">You can also use a [moniker](constructing-a-moniker-string.md) in a call to [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx), and set the default security settings, as in the following example.</span></span>


```VB
strComputer = "." 
Set objServices = GetObject( _
    "winmgmts:{impersonationLevel=impersonate," _
    & "authenticationLevel=pktPrivacy}!root/cimv2")
set objProcessSet = objServices.ExecQuery _
     ("SELECT Name FROM Win32_Process",,48)
For Each Process in objProcessSet
    WScript.Echo Process.Name
Next
```



<span data-ttu-id="85da5-114">Дополнительные сведения о настройке различных уровней олицетворения или проверки подлинности в сценарии, а также о настройке значений по умолчанию для компьютера см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="85da5-114">For more information about setting different impersonation or authentication levels in a script, or for setting the default values for a computer, see the following topics:</span></span>

-   [<span data-ttu-id="85da5-115">Изменение учетных данных проверки подлинности по умолчанию с помощью VBScript</span><span class="sxs-lookup"><span data-stu-id="85da5-115">Changing the Default Authentication Credentials Using VBScript</span></span>](#changing-the-default-authentication-credentials-using-vbscript)
-   [<span data-ttu-id="85da5-116">Изменение параметров олицетворения по умолчанию с помощью VBScript</span><span class="sxs-lookup"><span data-stu-id="85da5-116">Changing the Default Impersonation Settings Using VBScript</span></span>](#changing-the-default-impersonation-levels-using-vbscript)
-   [<span data-ttu-id="85da5-117">Настройка уровня олицетворения по умолчанию с помощью реестра</span><span class="sxs-lookup"><span data-stu-id="85da5-117">Setting the Default Impersonation Level Using the Registry</span></span>](#setting-the-default-impersonation-level-using-the-registry)
-   [<span data-ttu-id="85da5-118">Доступ к объекту Свбемсекурити в VBScript</span><span class="sxs-lookup"><span data-stu-id="85da5-118">Accessing the SWbemSecurity Object in VBScript</span></span>](#accessing-the-swbemsecurity-object-in-vbscript)
-   [<span data-ttu-id="85da5-119">**свбемсекурити**</span><span class="sxs-lookup"><span data-stu-id="85da5-119">**SWbemSecurity**</span></span>](swbemsecurity.md)

## <a name="changing-the-default-authentication-credentials-using-vbscript"></a><span data-ttu-id="85da5-120">Изменение учетных данных проверки подлинности по умолчанию с помощью VBScript</span><span class="sxs-lookup"><span data-stu-id="85da5-120">Changing the Default Authentication Credentials Using VBScript</span></span>

<span data-ttu-id="85da5-121">Можно изменить уровень проверки подлинности в скрипте, используя строку [моникера](constructing-a-moniker-string.md) , а также объекты [**SWbemLocator**](swbemlocator.md) и [**свбемсекурити**](swbemsecurity.md) .</span><span class="sxs-lookup"><span data-stu-id="85da5-121">You can change the authentication level in a script using a [moniker](constructing-a-moniker-string.md) string, and the [**SWbemLocator**](swbemlocator.md) and [**SWbemSecurity**](swbemsecurity.md) objects.</span></span>

<span data-ttu-id="85da5-122">Уровень проверки подлинности должен быть установлен в соответствии с требованиями целевой операционной системы, к которой выполняется подключение.</span><span class="sxs-lookup"><span data-stu-id="85da5-122">The authentication level must be set according to the requirements of the target operating system to which you are connecting.</span></span> <span data-ttu-id="85da5-123">Дополнительные сведения см. в разделе [подключение между разными операционными системами](/windows/desktop/WmiSdk/troubleshooting-a-remote-wmi-connection).</span><span class="sxs-lookup"><span data-stu-id="85da5-123">For more information, see [Connecting Between Different Operating Systems](/windows/desktop/WmiSdk/troubleshooting-a-remote-wmi-connection).</span></span>

<span data-ttu-id="85da5-124">В следующем примере кода VBScript показано, как изменить уровень проверки подлинности в скрипте, получающем данные о свободном месте с удаленного компьютера с именем "Server1".</span><span class="sxs-lookup"><span data-stu-id="85da5-124">The following VBScript code example shows how to change the authentication level in a script that obtains the free space data from a remote computer named "Server1".</span></span>


```VB
strComputer = "Server1"
Set objWMIService = GetObject("winmgmts:{authenticationLevel=Pkt}!\\" _
    & strComputer & "\root\cimv2")
Set colDisks = objWMIService.ExecQuery ("Select * from Win32_LogicalDisk")
For each objDisk in colDisks
    Wscript.Echo "DeviceID: " & vbTab & objDisk.DeviceID & vbNewLine & _
        "FreeSpace: " & vbTab & objDisk.FreeSpace 
    NextstrComputer = "." 
    Set objServices = GetObject( "winmgmts:{impersonationLevel=impersonate," _
                               & "authenticationLevel=pktPrivacy}!root/cimv2")
    Set objProcessSet = objServices.ExecQuery("SELECT Name FROM Win32_Process",,48)
    For Each Process in objProcessSet
        WScript.Echo Process.Name
    Next
Next
```



<span data-ttu-id="85da5-125">В поднаборе моникера скрипта соединения с WMI используйте короткое имя, указанное в столбце "имя моникера/описание" приведенной ниже таблицы.</span><span class="sxs-lookup"><span data-stu-id="85da5-125">In script moniker connections to WMI, use the short name shown in the "Moniker name/description" column of the table below.</span></span> <span data-ttu-id="85da5-126">Например, в следующем сценарии для уровня проверки подлинности задано значение **вбемаусентикатионлевелпктинтегрити**.</span><span class="sxs-lookup"><span data-stu-id="85da5-126">For example, in the following script, the authentication level is set to **WbemAuthenticationLevelPktIntegrity**.</span></span>


```VB
SetobjWMIService = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!root\cimv2")
```



<span data-ttu-id="85da5-127">В следующей таблице перечислены уровни проверки подлинности, которые можно задать.</span><span class="sxs-lookup"><span data-stu-id="85da5-127">The following table lists the authentication levels you can set.</span></span> <span data-ttu-id="85da5-128">Эти уровни определяются в Wbemdisp. tlb в перечислении [вбемаусентикатионлевеленум](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemauthenticationlevelenum).</span><span class="sxs-lookup"><span data-stu-id="85da5-128">These levels are defined in Wbemdisp.tlb in the enumeration [WbemAuthenticationLevelEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemauthenticationlevelenum).</span></span>



| <span data-ttu-id="85da5-129">Имя/значение</span><span class="sxs-lookup"><span data-stu-id="85da5-129">Name/value</span></span>                                                      | <span data-ttu-id="85da5-130">Описание</span><span class="sxs-lookup"><span data-stu-id="85da5-130">Description</span></span>                                                                                                                                                                                                                                                                                            |
|-----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="85da5-131">**вбемаусентикатионлевелдефаулт**</span><span class="sxs-lookup"><span data-stu-id="85da5-131">**WbemAuthenticationLevelDefault**</span></span><br/> <span data-ttu-id="85da5-132">0</span><span class="sxs-lookup"><span data-stu-id="85da5-132">0</span></span><br/>      | <span data-ttu-id="85da5-133">Моникер: по умолчанию</span><span class="sxs-lookup"><span data-stu-id="85da5-133">Moniker: Default</span></span><br/> <span data-ttu-id="85da5-134">Инструментарий WMI использует параметр проверки подлинности Windows по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="85da5-134">WMI uses the default Windows authentication setting.</span></span> <span data-ttu-id="85da5-135">Это рекомендуемый параметр, позволяющий инструментарию WMI согласовывать уровень, требуемый сервером, который возвращает данные.</span><span class="sxs-lookup"><span data-stu-id="85da5-135">This is the recommended setting that allows WMI to negotiate to the level required by the server returning data.</span></span> <span data-ttu-id="85da5-136">Однако если для пространства имен требуется шифрование, используйте **вбемаусентикатионлевелпктприваци**.</span><span class="sxs-lookup"><span data-stu-id="85da5-136">However, if the namespace requires encryption, use **WbemAuthenticationLevelPktPrivacy**.</span></span><br/> |
| <span data-ttu-id="85da5-137">**вбемаусентикатионлевелноне**</span><span class="sxs-lookup"><span data-stu-id="85da5-137">**WbemAuthenticationLevelNone**</span></span><br/> <span data-ttu-id="85da5-138">1</span><span class="sxs-lookup"><span data-stu-id="85da5-138">1</span></span><br/>         | <span data-ttu-id="85da5-139">Моникер: нет</span><span class="sxs-lookup"><span data-stu-id="85da5-139">Moniker: None</span></span><br/> <span data-ttu-id="85da5-140">Не использует проверку подлинности.</span><span class="sxs-lookup"><span data-stu-id="85da5-140">Uses no authentication.</span></span><br/>                                                                                                                                                                                                                                            |
| <span data-ttu-id="85da5-141">**вбемаусентикатионлевелконнект**</span><span class="sxs-lookup"><span data-stu-id="85da5-141">**WbemAuthenticationLevelConnect**</span></span><br/> <span data-ttu-id="85da5-142">2</span><span class="sxs-lookup"><span data-stu-id="85da5-142">2</span></span><br/>      | <span data-ttu-id="85da5-143">Моникер: Connect</span><span class="sxs-lookup"><span data-stu-id="85da5-143">Moniker: Connect</span></span><br/> <span data-ttu-id="85da5-144">Проверяет подлинность учетных данных клиента только в том случае, если клиент устанавливает связь с сервером.</span><span class="sxs-lookup"><span data-stu-id="85da5-144">Authenticates the credentials of the client only when the client establishes a relationship with the server.</span></span><br/>                                                                                                                                                    |
| <span data-ttu-id="85da5-145">**вбемаусентикатионлевелкалл**</span><span class="sxs-lookup"><span data-stu-id="85da5-145">**WbemAuthenticationLevelCall**</span></span><br/> <span data-ttu-id="85da5-146">3</span><span class="sxs-lookup"><span data-stu-id="85da5-146">3</span></span><br/>         | <span data-ttu-id="85da5-147">Вызов</span><span class="sxs-lookup"><span data-stu-id="85da5-147">Call</span></span><br/> <span data-ttu-id="85da5-148">Проверка подлинности выполняется только в начале каждого вызова, когда сервер получает запрос.</span><span class="sxs-lookup"><span data-stu-id="85da5-148">Authenticates only at the beginning of each call when the server receives the request.</span></span><br/>                                                                                                                                                                                      |
| <span data-ttu-id="85da5-149">**вбемаусентикатионлевелпкт**</span><span class="sxs-lookup"><span data-stu-id="85da5-149">**WbemAuthenticationLevelPkt**</span></span><br/> <span data-ttu-id="85da5-150">4</span><span class="sxs-lookup"><span data-stu-id="85da5-150">4</span></span><br/>          | <span data-ttu-id="85da5-151">Моникер: PKT</span><span class="sxs-lookup"><span data-stu-id="85da5-151">Moniker: Pkt</span></span><br/> <span data-ttu-id="85da5-152">Проверяет, что все полученные данные получены от ожидаемого клиента.</span><span class="sxs-lookup"><span data-stu-id="85da5-152">Authenticates that all data received is from the expected client.</span></span><br/>                                                                                                                                                                                                   |
| <span data-ttu-id="85da5-153">**вбемаусентикатионлевелпктинтегрити**</span><span class="sxs-lookup"><span data-stu-id="85da5-153">**WbemAuthenticationLevelPktIntegrity**</span></span><br/> <span data-ttu-id="85da5-154">5</span><span class="sxs-lookup"><span data-stu-id="85da5-154">5</span></span><br/> | <span data-ttu-id="85da5-155">Моникер: Пктинтегрити</span><span class="sxs-lookup"><span data-stu-id="85da5-155">Moniker: PktIntegrity</span></span><br/> <span data-ttu-id="85da5-156">Проверка подлинности и проверка того, что ни один из данных, передаваемых между клиентом и сервером, не был изменен.</span><span class="sxs-lookup"><span data-stu-id="85da5-156">Authenticates and verifies that none of the data transferred between client and server has been modified.</span></span><br/>                                                                                                                                                  |
| <span data-ttu-id="85da5-157">**вбемаусентикатионлевелпктприваци**</span><span class="sxs-lookup"><span data-stu-id="85da5-157">**WbemAuthenticationLevelPktPrivacy**</span></span><br/> <span data-ttu-id="85da5-158">6</span><span class="sxs-lookup"><span data-stu-id="85da5-158">6</span></span><br/>   | <span data-ttu-id="85da5-159">Моникер: Пктприваци</span><span class="sxs-lookup"><span data-stu-id="85da5-159">Moniker: PktPrivacy</span></span><br/> <span data-ttu-id="85da5-160">Проверяет подлинность всех предыдущих уровней олицетворения и шифрует значение аргумента для каждого удаленного вызова процедуры.</span><span class="sxs-lookup"><span data-stu-id="85da5-160">Authenticates all previous impersonation levels and encrypts the argument value of each remote procedure call.</span></span> <span data-ttu-id="85da5-161">Используйте этот параметр, если для пространства имен, к которому выполняется подключение, требуется зашифрованное соединение.</span><span class="sxs-lookup"><span data-stu-id="85da5-161">Use this setting if the namespace to which you are connecting requires an encrypted connection.</span></span><br/>                                               |



 

<span data-ttu-id="85da5-162">Чтобы определить успешный вызов, проверьте возвращаемое значение после изменения уровня проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="85da5-162">To determine a successful call, check the return value after you change the authentication level.</span></span>

<span data-ttu-id="85da5-163">Например, поскольку локальные соединения всегда имеют уровень проверки подлинности **вбемаусентикатионлевелпктприваци**, в следующем примере не удается установить уровень проверки подлинности, так как он подключается к локальному компьютеру.</span><span class="sxs-lookup"><span data-stu-id="85da5-163">For example, because local connections always have an authentication level of **wbemAuthenticationLevelPktPrivacy**, the following example fails to set the authentication level because it connects to the local computer.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
    & "{impersonationLevel=impersonate," _
    & "authenticationLevel=pktPrivacy}!" _
    & "\\" & strComputer & "\root\cimv2")
```



<span data-ttu-id="85da5-164">Поставщик может установить безопасность для пространства имен таким образом, чтобы никакие данные не возвращались, если только вы не используете конфиденциальность пакетов (Пктприваци) в подключении к этому пространству имен.</span><span class="sxs-lookup"><span data-stu-id="85da5-164">A provider can set the security on a namespace so that no data is returned unless you use packet privacy (PktPrivacy) in your connection to that namespace.</span></span> <span data-ttu-id="85da5-165">Это гарантирует, что данные шифруются по мере пересечения сети.</span><span class="sxs-lookup"><span data-stu-id="85da5-165">This ensures that data is encrypted as it crosses the network.</span></span> <span data-ttu-id="85da5-166">При попытке задать более низкий уровень проверки подлинности будет получено сообщение об отказе в доступе.</span><span class="sxs-lookup"><span data-stu-id="85da5-166">If you try to set a lower authentication level, you will get an access denied message.</span></span> <span data-ttu-id="85da5-167">Дополнительные сведения см. в разделе [Защита пространств имен WMI](securing-wmi-namespaces.md).</span><span class="sxs-lookup"><span data-stu-id="85da5-167">For more information, see [Securing WMI Namespaces](securing-wmi-namespaces.md).</span></span>

## <a name="changing-the-default-impersonation-levels-using-vbscript"></a><span data-ttu-id="85da5-168">Изменение уровней олицетворения по умолчанию с помощью VBScript</span><span class="sxs-lookup"><span data-stu-id="85da5-168">Changing the Default Impersonation Levels Using VBScript</span></span>

<span data-ttu-id="85da5-169">При вызове API скриптов для WMI рекомендуется использовать значения по умолчанию, которые WMI предоставляет для уровня олицетворения.</span><span class="sxs-lookup"><span data-stu-id="85da5-169">When you make calls to the Scripting API for WMI, it is recommended that you use the defaults that WMI provides for the impersonation level.</span></span> <span data-ttu-id="85da5-170">Для удаленных вызовов и некоторых поставщиков с более чем одним прыжком к сети требуется более высокий уровень олицетворения, чем использование WMI.</span><span class="sxs-lookup"><span data-stu-id="85da5-170">Remote calls and some providers with more than one network hop require a higher impersonation level than WMI uses.</span></span> <span data-ttu-id="85da5-171">Если уровень олицетворения недостаточно, поставщик может отказаться от запроса или предоставить неполные сведения.</span><span class="sxs-lookup"><span data-stu-id="85da5-171">If the impersonation level is not sufficient, a provider might refuse a request or provide incomplete information.</span></span>

<span data-ttu-id="85da5-172">Если уровень олицетворения не задан ни в моникере, ни при установке [**свбемсекурити. имперсонатионлевел**](swbemsecurity-impersonationlevel.md) защищаемого объекта, установите уровень олицетворения DCOM по умолчанию для операционной системы.</span><span class="sxs-lookup"><span data-stu-id="85da5-172">If you do not set the impersonation level in either a moniker or by setting [**SWbemSecurity.ImpersonationLevel**](swbemsecurity-impersonationlevel.md) on a securable object, then set the default DCOM impersonation level for the operating system.</span></span> <span data-ttu-id="85da5-173">Уровень олицетворения должен быть установлен в соответствии с требованиями целевой операционной системы, к которой выполняется подключение.</span><span class="sxs-lookup"><span data-stu-id="85da5-173">The impersonation level must be set according to the requirements of the target operating system to which you are connecting.</span></span> <span data-ttu-id="85da5-174">Дополнительные сведения см. в разделе [подключение между разными операционными системами](/windows/desktop/WmiSdk/troubleshooting-a-remote-wmi-connection).</span><span class="sxs-lookup"><span data-stu-id="85da5-174">For more information, see [Connecting Between Different Operating Systems](/windows/desktop/WmiSdk/troubleshooting-a-remote-wmi-connection).</span></span>

<span data-ttu-id="85da5-175">В следующем примере кода VBScript показано изменение уровня олицетворения в том же скрипте, показанном выше.</span><span class="sxs-lookup"><span data-stu-id="85da5-175">The following VBScript code example shows changing the impersonation level in the same script shown above.</span></span>


```VB
strComputer = "Server1"
Set objWMIService = GetObject("winmgmts:{impersonationLevel=Impersonate}!\\" _
                              & strComputer & "\root\cimv2")
Set colDisks = objWMIService.ExecQuery("Select * from Win32_LogicalDisk")
For each objDisk in colDisks
Wscript.Echo "DeviceID: " & vbTab & objDisk.DeviceID & vbNewLine & _
             "FreeSpace: " & vbTab & objDisk.FreeSpace 
Next
```



<span data-ttu-id="85da5-176">В следующей таблице перечислены уровни проверки подлинности в [вбемимперсонатионлевеленум](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemimpersonationlevelenum) , использующие.</span><span class="sxs-lookup"><span data-stu-id="85da5-176">The following table lists the authentication levels in [WbemImpersonationLevelEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemimpersonationlevelenum) that use.</span></span>



| <span data-ttu-id="85da5-177">Имя/значение</span><span class="sxs-lookup"><span data-stu-id="85da5-177">Name/value</span></span>                                                    | <span data-ttu-id="85da5-178">Описание</span><span class="sxs-lookup"><span data-stu-id="85da5-178">Description</span></span>                                                                                                                                                                                                                         |
|---------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="85da5-179">**вбемимперсонатионлевеланонимаус**</span><span class="sxs-lookup"><span data-stu-id="85da5-179">**wbemImpersonationLevelAnonymous**</span></span><br/> <span data-ttu-id="85da5-180">1</span><span class="sxs-lookup"><span data-stu-id="85da5-180">1</span></span><br/>   | <span data-ttu-id="85da5-181">Моникер: Anonymous</span><span class="sxs-lookup"><span data-stu-id="85da5-181">Moniker: Anonymous</span></span><br/> <span data-ttu-id="85da5-182">Скрывает учетные данные вызывающей стороны.</span><span class="sxs-lookup"><span data-stu-id="85da5-182">Hides the credentials of the caller.</span></span> <span data-ttu-id="85da5-183">При этом уровне олицетворения во время вызовов, адресованных WMI, возможны сбои.</span><span class="sxs-lookup"><span data-stu-id="85da5-183">Calls to WMI may fail with this impersonation level.</span></span><br/>                                                                                                  |
| <span data-ttu-id="85da5-184">**вбемимперсонатионлевелидентифи**</span><span class="sxs-lookup"><span data-stu-id="85da5-184">**wbemImpersonationLevelIdentify**</span></span><br/> <span data-ttu-id="85da5-185">2</span><span class="sxs-lookup"><span data-stu-id="85da5-185">2</span></span><br/>    | <span data-ttu-id="85da5-186">Моникер: Identify</span><span class="sxs-lookup"><span data-stu-id="85da5-186">Moniker: Identify</span></span><br/> <span data-ttu-id="85da5-187">позволяет объектам запрашивать учетные данные вызывающей стороны.</span><span class="sxs-lookup"><span data-stu-id="85da5-187">Allows objects to query the credentials of the caller.</span></span> <span data-ttu-id="85da5-188">При этом уровне олицетворения во время вызовов, адресованных WMI, возможны сбои.</span><span class="sxs-lookup"><span data-stu-id="85da5-188">Calls to WMI may fail with this impersonation level.</span></span><br/>                                                                                 |
| <span data-ttu-id="85da5-189">**вбемимперсонатионлевелимперсонате**</span><span class="sxs-lookup"><span data-stu-id="85da5-189">**wbemImpersonationLevelImpersonate**</span></span><br/> <span data-ttu-id="85da5-190">3</span><span class="sxs-lookup"><span data-stu-id="85da5-190">3</span></span><br/> | <span data-ttu-id="85da5-191">Моникер: IMPERSONATE</span><span class="sxs-lookup"><span data-stu-id="85da5-191">Moniker: Impersonate</span></span><br/> <span data-ttu-id="85da5-192">позволяет объектам использовать учетные данные вызывающей стороны.</span><span class="sxs-lookup"><span data-stu-id="85da5-192">Allows objects to use the credentials of the caller.</span></span> <span data-ttu-id="85da5-193">Это рекомендуемый уровень олицетворения для API-интерфейсов сценариев для вызовов WMI.</span><span class="sxs-lookup"><span data-stu-id="85da5-193">This is the recommended impersonation level for Scripting API for WMI calls.</span></span><br/>                                                        |
| <span data-ttu-id="85da5-194">**вбемимперсонатионлевелделегате**</span><span class="sxs-lookup"><span data-stu-id="85da5-194">**wbemImpersonationLevelDelegate**</span></span><br/> <span data-ttu-id="85da5-195">4</span><span class="sxs-lookup"><span data-stu-id="85da5-195">4</span></span><br/>    | <span data-ttu-id="85da5-196">Моникер: Delegate</span><span class="sxs-lookup"><span data-stu-id="85da5-196">Moniker: Delegate</span></span><br/> <span data-ttu-id="85da5-197">Позволяет объектам разрешать другим объектам использовать учетные данные вызывающей стороны.</span><span class="sxs-lookup"><span data-stu-id="85da5-197">Allows objects to permit other objects to use the credentials of the caller.</span></span> <span data-ttu-id="85da5-198">Это олицетворение будет работать с API-интерфейсом сценариев для вызовов инструментария WMI, но может представлять ненужные риски безопасности.</span><span class="sxs-lookup"><span data-stu-id="85da5-198">This impersonation will work with Scripting API for WMI calls but may constitute an unnecessary security risk.</span></span><br/> |



 

<span data-ttu-id="85da5-199">В следующем примере показано, как задать олицетворение в строке моникера при получении конкретного экземпляра [**\_ процесса Win32**](/windows/desktop/CIMWin32Prov/win32-process).</span><span class="sxs-lookup"><span data-stu-id="85da5-199">The following example shows how to set the impersonation in a moniker string when obtaining a specific instance of [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process).</span></span>


```VB
Set object = GetObject("winmgmts:{impersonationLevel=impersonate}!root\cimv2:Win32_Process.Handle='0'")
```



<span data-ttu-id="85da5-200">Дополнительные сведения см. [в разделе Создание приложения WMI или скрипта](creating-a-wmi-application-or-script.md).</span><span class="sxs-lookup"><span data-stu-id="85da5-200">For more information, see [Creating a WMI Application or Script](creating-a-wmi-application-or-script.md).</span></span>

## <a name="setting-the-default-impersonation-level-using-the-registry"></a><span data-ttu-id="85da5-201">Настройка уровня олицетворения по умолчанию с помощью реестра</span><span class="sxs-lookup"><span data-stu-id="85da5-201">Setting the Default Impersonation Level Using the Registry</span></span>

<span data-ttu-id="85da5-202">Если у вас есть доступ к реестру, можно также задать раздел реестра уровня олицетворения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="85da5-202">If you have access to the registry, you can also set the default impersonation level registry key.</span></span> <span data-ttu-id="85da5-203">Этот ключ указывает, какой уровень олицетворения использует API скриптов для инструментария WMI, если не указано иное.</span><span class="sxs-lookup"><span data-stu-id="85da5-203">This key specifies which impersonation level the Scripting API for WMI uses unless otherwise specified.</span></span> <span data-ttu-id="85da5-204">Следующий путь определяет путь реестра.</span><span class="sxs-lookup"><span data-stu-id="85da5-204">The following path identifies the registry path.</span></span>

<span data-ttu-id="85da5-205">**HKey \_ По локального \_ компьютера** \\ **программное обеспечение** \\ **Microsoft** \\ **WBEM** \\ **Скрипт** \\ **уровень олицетворения по умолчанию**</span><span class="sxs-lookup"><span data-stu-id="85da5-205">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**WBEM**\\**Scripting**\\**Default Impersonation Level**</span></span>

<span data-ttu-id="85da5-206">По умолчанию раздел реестра имеет значение 3, указывая уровень олицетворения IMPERSONATE.</span><span class="sxs-lookup"><span data-stu-id="85da5-206">By default, the registry key is set to 3, specifying the Impersonate impersonation level.</span></span> <span data-ttu-id="85da5-207">Некоторые поставщики могут потребовать более высокого уровня олицетворения.</span><span class="sxs-lookup"><span data-stu-id="85da5-207">Some providers may require a higher level of impersonation.</span></span>

## <a name="accessing-the-swbemsecurity-object-in-vbscript"></a><span data-ttu-id="85da5-208">Доступ к объекту Свбемсекурити в VBScript</span><span class="sxs-lookup"><span data-stu-id="85da5-208">Accessing the SWbemSecurity Object in VBScript</span></span>

<span data-ttu-id="85da5-209">Другим способом установки уровня олицетворения является объект безопасности [**свбемсекурити**](swbemsecurity.md) , который отображается как свойство [**безопасности \_**](swbemservices-security-.md) объектов [**SwbemServices**](swbemservices.md), [**SWbemObject**](swbemobject.md), [**SWbemObjectSet**](swbemobjectset.md), [**свбемевентсаурце**](swbemeventsource.md), [**свбемобжектпас**](swbemobjectpath.md)и [**SwbemLocator**](swbemlocator.md) .</span><span class="sxs-lookup"><span data-stu-id="85da5-209">The other way you can set the impersonation level is from the [**SWbemSecurity**](swbemsecurity.md) security object, which appears as the [**Security\_**](swbemservices-security-.md) property of the [**SWbemServices**](swbemservices.md), [**SWbemObject**](swbemobject.md), [**SWbemObjectSet**](swbemobjectset.md), [**SWbemEventSource**](swbemeventsource.md), [**SWbemObjectPath**](swbemobjectpath.md), and [**SwbemLocator**](swbemlocator.md) objects.</span></span>

<span data-ttu-id="85da5-210">Инструментарий WMI передает параметр безопасности родительского объекта потомкам исходного объекта.</span><span class="sxs-lookup"><span data-stu-id="85da5-210">WMI passes the security setting of a parent object to the descendants of the original object.</span></span> <span data-ttu-id="85da5-211">Таким образом, можно задать уровень олицетворения объекта [**SwbemServices**](swbemservices.md) после входа в WMI и вызовов API, используя этот объект или созданные из него объекты, такие как объекты типа [**SWbemObject**](swbemobject.md).</span><span class="sxs-lookup"><span data-stu-id="85da5-211">Therefore, you can set the impersonation level of an [**SWbemServices**](swbemservices.md) object after logging on to WMI and API calls using this object or objects created from it, such as objects of type [**SWbemObject**](swbemobject.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="85da5-212">См. также</span><span class="sxs-lookup"><span data-stu-id="85da5-212">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="85da5-213">Подключение к инструментарию WMI на удаленном компьютере</span><span class="sxs-lookup"><span data-stu-id="85da5-213">Connecting to WMI on a Remote Computer</span></span>](connecting-to-wmi-on-a-remote-computer.md)
</dt> <dt>

[<span data-ttu-id="85da5-214">Защита клиентов скриптов</span><span class="sxs-lookup"><span data-stu-id="85da5-214">Securing Scripting Clients</span></span>](securing-scripting-clients.md)
</dt> </dl>

 

