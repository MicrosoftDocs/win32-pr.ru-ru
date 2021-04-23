---
description: Вы можете создать удаленное подключение к инструментарию WMI с помощью VBScript, создав объект соединения. Этот объект содержит имя компьютера, пространство имен WMI, к которому необходимо подключиться, а также соответствующие учетные данные и уровни проверки подлинности.
ms.assetid: b2ad262b-148d-47cc-8be7-6df99245aa7f
ms.tgt_platform: multiple
title: Удаленное подключение к инструментарию WMI с помощью VBScript
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 07cff2f0cd0ca06de059d9b39e36d715b5555eaa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711754"
---
# <a name="connecting-to-wmi-remotely-with-vbscript"></a><span data-ttu-id="80794-104">Удаленное подключение к инструментарию WMI с помощью VBScript</span><span class="sxs-lookup"><span data-stu-id="80794-104">Connecting to WMI Remotely with VBScript</span></span>

<span data-ttu-id="80794-105">Вы можете создать удаленное подключение к инструментарию WMI с помощью VBScript, создав объект соединения.</span><span class="sxs-lookup"><span data-stu-id="80794-105">You can create a remote connection to WMI with VBScript by creating a connection object.</span></span> <span data-ttu-id="80794-106">Этот объект содержит имя компьютера, пространство имен WMI, к которому необходимо подключиться, а также соответствующие учетные данные и уровни проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="80794-106">This object contains the name of the computer, the WMI namespace you want to connect to, as well as any relevant credentials and authentication levels.</span></span>

<span data-ttu-id="80794-107">**Подключение к удаленной системе с помощью VBScript**</span><span class="sxs-lookup"><span data-stu-id="80794-107">**To connect to a remote system using VBScript**</span></span>

1.  <span data-ttu-id="80794-108">Укажите сведения о соединении, такие как имя удаленного компьютера, учетные данные и уровень проверки подлинности для подключения.</span><span class="sxs-lookup"><span data-stu-id="80794-108">Specify the connection information such as the remote computer name, credentials, and the authentication level for the connection.</span></span>

    <span data-ttu-id="80794-109">При подключении к удаленному компьютеру с использованием тех же учетных данных (домен и имя пользователя), которые вошли в систему, можно указать сведения о соединении в [моникере](constructing-a-moniker-string.md) [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject), как описано в следующем примере кода.</span><span class="sxs-lookup"><span data-stu-id="80794-109">If you are connecting to a remote computer using the same credentials (domain and user name) you are logged on with, then you can specify the connection information in a [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject)[moniker](constructing-a-moniker-string.md), as described in the following code sample.</span></span>

    ```VB
    strComputer = "Computer_B"
    Set objWMIService = GetObject("winmgmts:{impersonationLevel=Impersonate}!\\" & strComputer & "\Root\CIMv2")
    ```

    

    <span data-ttu-id="80794-110">В общем случае следует указать пространство имен WMI для подключения к удаленному компьютеру.</span><span class="sxs-lookup"><span data-stu-id="80794-110">Generally speaking, you should specify the WMI namespace to connect to on the remote computer.</span></span> <span data-ttu-id="80794-111">Это связано с тем, что пространство имен по умолчанию может не совпадать на разных компьютерах.</span><span class="sxs-lookup"><span data-stu-id="80794-111">This is because it is possible that the default namespace is not the same on different computers.</span></span> <span data-ttu-id="80794-112">Указание пространства имен гарантирует подключение к одному и тому же пространству имен на всех компьютерах.</span><span class="sxs-lookup"><span data-stu-id="80794-112">Specifying the namespace ensures that you connect to the same namespace on all computers.</span></span>

    <span data-ttu-id="80794-113">Дополнительные сведения о константах VBScript и строках сценариев для использования моникера Connection см. в разделе [Задание уровня безопасности процесса по умолчанию с помощью VBScript](setting-the-default-process-security-level-using-vbscript.md).</span><span class="sxs-lookup"><span data-stu-id="80794-113">For more information on VBScript constants and scripting strings for using the moniker connection, see [Setting the Default Process Security Level Using VBScript](setting-the-default-process-security-level-using-vbscript.md).</span></span>

2.  <span data-ttu-id="80794-114">Если вы подключаетесь к удаленному компьютеру в другом домене или используете другое имя пользователя и пароль, необходимо использовать метод [**SWbemLocator. коннектсервер**](swbemlocator-connectserver.md) .</span><span class="sxs-lookup"><span data-stu-id="80794-114">If you connect to a remote computer in a different domain or using a different user name and password, then you must use the [**SWbemLocator.ConnectServer**](swbemlocator-connectserver.md) method.</span></span>

    <span data-ttu-id="80794-115">Как и в случае с моникером, вы используете **коннектсервер** для указания учетных данных, уровня проверки подлинности и пространства имен для удаленного подключения.</span><span class="sxs-lookup"><span data-stu-id="80794-115">As with a moniker, you use **ConnectServer** to specify the credentials, authentication level, and namespace for the remote connection.</span></span> <span data-ttu-id="80794-116">В следующем примере кода описывается использование Коннектсервер для доступа к удаленному компьютеру с использованием учетной записи администратора и пароля.</span><span class="sxs-lookup"><span data-stu-id="80794-116">The following code sample describes using ConnectServer to access a remote computer using an administrator account and password.</span></span>

    ```VB
    strComputer = "Computer_B"
    Set objSWbemLocator = CreateObject("WbemScripting.SWbemLocator")
    Set objSWbemServices = objSWbemLocator.ConnectServer(strComputer, _
                                                         "Root\CIMv2", _
                                                         "fabrikam\administrator", _
                                                         "password")
    ```

    

3.  <span data-ttu-id="80794-117">При использовании функции [**коннектсервер**](swbemlocator-connectserver.md) для удаленных соединений настройте олицетворение и проверку подлинности для объекта безопасности, полученного при вызове [**SwbemServices. Security**](swbemservices-security-.md).</span><span class="sxs-lookup"><span data-stu-id="80794-117">When using the [**ConnectServer**](swbemlocator-connectserver.md) function for remote connections, set impersonation and authentication on the security object obtained by a call to [**SWbemServices.Security**](swbemservices-security-.md).</span></span> <span data-ttu-id="80794-118">Для указания уровня олицетворения можно использовать перечисление [вбемимперсонатионлевеленум](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemimpersonationlevelenum) .</span><span class="sxs-lookup"><span data-stu-id="80794-118">You can use the enumeration [WbemImpersonationLevelEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemimpersonationlevelenum) to specify impersonation level.</span></span>

    <span data-ttu-id="80794-119">В следующем примере кода задается уровень олицетворения для предыдущего примера кода VBScript.</span><span class="sxs-lookup"><span data-stu-id="80794-119">The following code sample sets the impersonation level for the previous VBScript code sample.</span></span>

    ```VB
    objSWbemServices.Security_.ImpersonationLevel = 3
    ```

    

    <span data-ttu-id="80794-120">Обратите внимание, что для некоторых подключений требуется определенный уровень проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="80794-120">Note that some connections require a specific authentication level.</span></span> <span data-ttu-id="80794-121">Дополнительные сведения см. в разделе [Установка клиентских приложений безопасность](setting-client-application-process-security.md) и [Защита клиентов скриптов](securing-scripting-clients.md).</span><span class="sxs-lookup"><span data-stu-id="80794-121">For more information, see [Setting Client Application Process Security](setting-client-application-process-security.md) and [Securing Scripting Clients](securing-scripting-clients.md).</span></span>

    <span data-ttu-id="80794-122">В частности, следует задать уровень проверки подлинности **RPC \_ C \_ AUTHN \_ уровня " \_ PKT \_** " или 6, если для пространства имен, к которому выполняется подключение на удаленном компьютере, требуется зашифрованное соединение, прежде чем оно вернет данные.</span><span class="sxs-lookup"><span data-stu-id="80794-122">In particular, you should set the authentication level to **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY** or 6 if the namespace to which you are connecting on the remote computer requires an encrypted connection before it will return data.</span></span> <span data-ttu-id="80794-123">Этот уровень проверки подлинности также можно использовать, даже если пространство имен не требуется.</span><span class="sxs-lookup"><span data-stu-id="80794-123">You can also use this authentication level, even if the namespace does not require it.</span></span> <span data-ttu-id="80794-124">Это гарантирует, что данные шифруются по мере пересечения сети.</span><span class="sxs-lookup"><span data-stu-id="80794-124">This ensures that data is encrypted as it crosses the network.</span></span> <span data-ttu-id="80794-125">Если попытаться задать более низкий уровень проверки подлинности, чем разрешено, будет возвращено сообщение об отказе в доступе.</span><span class="sxs-lookup"><span data-stu-id="80794-125">If you attempt to set a lower authentication level than is allowed, an access denied message will be returned.</span></span> <span data-ttu-id="80794-126">Дополнительные сведения см. в разделе [требуется зашифрованное соединение с пространством имен](requiring-an-encrypted-connection-to-a-namespace.md).</span><span class="sxs-lookup"><span data-stu-id="80794-126">For more information, see [Requiring an Encrypted Connection to a Namespace](requiring-an-encrypted-connection-to-a-namespace.md).</span></span>

<span data-ttu-id="80794-127">После установки соединения можно продолжить доступ к данным WMI.</span><span class="sxs-lookup"><span data-stu-id="80794-127">Once you have made your connection, you can continue to access WMI data.</span></span> <span data-ttu-id="80794-128">Дополнительные сведения см. в разделе [задачи WMI для скриптов и приложений](wmi-tasks-for-scripts-and-applications.md).</span><span class="sxs-lookup"><span data-stu-id="80794-128">For more information, see [WMI Tasks for Scripts and Applications](wmi-tasks-for-scripts-and-applications.md).</span></span>

## <a name="examples"></a><span data-ttu-id="80794-129">Примеры</span><span class="sxs-lookup"><span data-stu-id="80794-129">Examples</span></span>

<span data-ttu-id="80794-130">Более крупный пример на языке VBScript см. в разделе "примеры" на странице справочника по [**SWbemLocator. коннектсервер**](swbemlocator-connectserver.md) .</span><span class="sxs-lookup"><span data-stu-id="80794-130">For a larger VBScript sample, see the Examples section in the [**SWbemLocator.ConnectServer**](swbemlocator-connectserver.md) reference page.</span></span>

<span data-ttu-id="80794-131">Следующий пример кода VBScript подключается к группе удаленных компьютеров в том же домене, создавая массив имен удаленных компьютеров, а затем отображая имена самонастраивающийся устройств — экземпляры [**Win32 \_ пнпентити**](/windows/desktop/CIMWin32Prov/win32-pnpentity)— на каждом компьютере.</span><span class="sxs-lookup"><span data-stu-id="80794-131">The following VBScript code example connects to a group of remote computers in the same domain by creating an array of remote computer names and then displaying names of the Plug and Play devices—instances of [**Win32\_PnPEntity**](/windows/desktop/CIMWin32Prov/win32-pnpentity)—on each computer.</span></span> <span data-ttu-id="80794-132">Для выполнения приведенного ниже сценария необходимы права администратора на удаленных компьютерах.</span><span class="sxs-lookup"><span data-stu-id="80794-132">To run the script below, you must be an administrator on the remote computers.</span></span> <span data-ttu-id="80794-133">Обратите внимание, что параметр " \\ \\ ", необходимый перед именем удаленного компьютера, добавляется скриптом после настройки уровня олицетворения.</span><span class="sxs-lookup"><span data-stu-id="80794-133">Note that the "\\\\" required before the remote computer name is added by the script following the impersonation level setting.</span></span> <span data-ttu-id="80794-134">Дополнительные сведения о путях WMI см. [в разделе Описание расположения объекта WMI](describing-the-location-of-a-wmi-object.md).</span><span class="sxs-lookup"><span data-stu-id="80794-134">For more information about WMI paths, see [Describing the Location of a WMI Object](describing-the-location-of-a-wmi-object.md).</span></span>


```VB
On Error Resume Next 
arrComputers = Array("Computer1","Computer2","Computer3")
For Each strComputer In arrComputers
    WScript.Echo
    WScript.Echo "===================================="
    WScript.Echo "Computer: "& strComputer
    WScript.Echo "===================================="

    Set objWMIService = GetObject("winmgmts:\\" & strComputer& "\Root\CIMv2") 
    Set colItems = objWMIService.ExecQuery("SELECT * FROM Win32_PnPEntity",,48) 
    For Each objItem in colItems 
        Wscript.Echo "-----------------------------------"
        Wscript.Echo "Win32_PnPEntity instance"
        Wscript.Echo "-----------------------------------"
        Wscript.Echo "Name: "& objItem.Name
        Wscript.Echo "Status: "& objItem.Status
    Next
Next
```



<span data-ttu-id="80794-135">Следующий пример кода VBScript позволяет подключиться к удаленному компьютеру с использованием других учетных данных.</span><span class="sxs-lookup"><span data-stu-id="80794-135">The following VBScript code example enables you to connect to a remote computer using different credentials.</span></span> <span data-ttu-id="80794-136">Например, удаленный компьютер в другом домене или подключение к удаленному компьютеру, для которого требуется другое имя пользователя и пароль.</span><span class="sxs-lookup"><span data-stu-id="80794-136">For example, a remote computer in a different domain or connecting to a remote computer requiring a different user name and password.</span></span> <span data-ttu-id="80794-137">В этом случае используйте подключение [**SwbemServices. коннектсервер**](swbemlocator-connectserver.md) .</span><span class="sxs-lookup"><span data-stu-id="80794-137">In this case, use the [**SWbemServices.ConnectServer**](swbemlocator-connectserver.md) connection.</span></span>


```VB
' Full Computer Name
' can be found by right-clicking My Computer,
' then click Properties, then click the Computer Name tab)
' or use the computer's IP address
strComputer = "FullComputerName" 
strDomain = "DOMAIN" 
Wscript.StdOut.Write "Please enter your user name:"
strUser = Wscript.StdIn.ReadLine 
Set objPassword = CreateObject("ScriptPW.Password")
Wscript.StdOut.Write "Please enter your password:"
strPassword = objPassword.GetPassword()
 
Set objSWbemLocator = CreateObject("WbemScripting.SWbemLocator")
Set objSWbemServices = objSWbemLocator.ConnectServer(strComputer, _
                                                     "Root\CIMv2", _
                                                     strUser, _
                                                     strPassword, _
                                                     "MS_409", _
                                                     "ntlmdomain:" + strDomain)
Set colSwbemObjectSet = objSWbemServices.ExecQuery("Select * From Win32_Process")
For Each objProcess in colSWbemObjectSet
    Wscript.Echo "Process Name: " & objProcess.Name 
Next
```



## <a name="related-topics"></a><span data-ttu-id="80794-138">См. также</span><span class="sxs-lookup"><span data-stu-id="80794-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="80794-139">Подключение к инструментарию WMI на удаленном компьютере</span><span class="sxs-lookup"><span data-stu-id="80794-139">Connecting to WMI on a Remote Computer</span></span>](connecting-to-wmi-on-a-remote-computer.md)
</dt> </dl>

 

 
