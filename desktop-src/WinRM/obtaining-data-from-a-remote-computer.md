---
title: Получение данных с удаленного компьютера
description: Можно получить данные или управлять ресурсами на удаленных компьютерах, а также на локальном компьютере. Подключение к удаленному компьютеру в служба удаленного управления Windows сценария очень похоже на создание локального соединения.
ms.assetid: 578eee80-a6c1-4456-9683-14e0a3386248
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8cfc95a73dab4c9a0f19481b7ba41f3c40a3862d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103890668"
---
# <a name="obtaining-data-from-a-remote-computer"></a><span data-ttu-id="9777c-104">Получение данных с удаленного компьютера</span><span class="sxs-lookup"><span data-stu-id="9777c-104">Obtaining Data from a Remote Computer</span></span>

<span data-ttu-id="9777c-105">Можно получить данные или управлять ресурсами на удаленных компьютерах, а также на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="9777c-105">You can obtain data or manage resources on remote computers as well as the local computer.</span></span> <span data-ttu-id="9777c-106">Подключение к удаленному компьютеру в служба удаленного управления Windows сценария очень похоже на создание локального соединения.</span><span class="sxs-lookup"><span data-stu-id="9777c-106">Connecting to a remote computer in a Windows Remote Management script is very similar to making a local connection.</span></span> <span data-ttu-id="9777c-107">Данные экземпляра WMI доступны, и, если на удаленном компьютере установлено оборудование BMC, которое может обмениваться данными по протоколу WS-Management, то доступны также данные [интеллектуального управления платформой (IPMI)](/previous-versions/windows/desktop/ipmiprv/ipmi-provider) .</span><span class="sxs-lookup"><span data-stu-id="9777c-107">WMI instance data is available and, if the remote computer has BMC hardware that can communicate using the WS-Management protocol, then [Intelligent Platform Management Interface (IPMI)](/previous-versions/windows/desktop/ipmiprv/ipmi-provider) data is also available.</span></span> <span data-ttu-id="9777c-108">Дополнительные сведения см. в разделе [Служба удаленного управления Windows и инструментарий WMI](windows-remote-management-and-wmi.md) и [Удаленное управление оборудованием](remote-hardware-management.md).</span><span class="sxs-lookup"><span data-stu-id="9777c-108">For more information, see [Windows Remote Management and WMI](windows-remote-management-and-wmi.md) and [Remote Hardware Management](remote-hardware-management.md).</span></span>

<span data-ttu-id="9777c-109">Может потребоваться создать объект [**ConnectionOptions**](connectionoptions.md) , чтобы указать сведения о типе проверки подлинности, запрашиваемом для входа в систему.</span><span class="sxs-lookup"><span data-stu-id="9777c-109">You may need to create a [**ConnectionOptions**](connectionoptions.md) object to specify information about the type of authentication requested for the logon.</span></span>

<span data-ttu-id="9777c-110">Если учетная запись на удаленном компьютере имеет одинаковое имя пользователя и пароль для входа, необходимы только дополнительные сведения: транспорт, имя домена и имя компьютера.</span><span class="sxs-lookup"><span data-stu-id="9777c-110">If the account on the remote computer has the same logon username and password, the only extra information you need is the transport, the domain name, and the computer name.</span></span> <span data-ttu-id="9777c-111">Из-за [контроля учетных записей пользователей](https://support.microsoft.com/help/922708/how-to-use-user-account-control-uac-in-windows-vista)удаленная учетная запись должна быть учетной записью домена и членом группы администраторов удаленного компьютера.</span><span class="sxs-lookup"><span data-stu-id="9777c-111">Because of [User Account Control (UAC)](https://support.microsoft.com/help/922708/how-to-use-user-account-control-uac-in-windows-vista), the remote account must be a domain account and a member of the remote computer Administrators group.</span></span> <span data-ttu-id="9777c-112">Если учетная запись является членом локальной группы "Администраторы", то UAC не разрешает доступ к службе WinRM.</span><span class="sxs-lookup"><span data-stu-id="9777c-112">If the account is a local computer member of the Administrators group, then UAC does not allow access to the WinRM service.</span></span> <span data-ttu-id="9777c-113">Чтобы получить доступ к удаленной службе удаленного управления Windows в Рабочей группе, необходимо отключить фильтрацию контроля учетных записей для локальных учетных записей, создав следующую запись реестра DWORD и установив для нее значение 1: **\[ hKey \_ Local \_ Machine \\ Software \\ Microsoft \\ Windows \\ CurrentVersion Services \\ \\ \] LocalAccountTokenFilterPolicy System**.</span><span class="sxs-lookup"><span data-stu-id="9777c-113">To access a remote WinRM service in a workgroup, UAC filtering for local accounts must be disabled by creating the following DWORD registry entry and setting its value to 1: **\[HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Windows\\CurrentVersion\\Policies\\System\] LocalAccountTokenFilterPolicy**.</span></span>

<span data-ttu-id="9777c-114">**Подключение к удаленному компьютеру с использованием имени пользователя и пароля для входа**</span><span class="sxs-lookup"><span data-stu-id="9777c-114">**To connect to a remote computer using your logon username and password**</span></span>

1.  <span data-ttu-id="9777c-115">Укажите конечный компьютер с полным доменным именем или IP-адресом и назначьте его константе.</span><span class="sxs-lookup"><span data-stu-id="9777c-115">Specify the target computer with a fully qualified domain name or an IP address and assign this to a constant.</span></span> <span data-ttu-id="9777c-116">Если указан IPv6-адрес, адрес должен быть заключен в квадратные скобки.</span><span class="sxs-lookup"><span data-stu-id="9777c-116">If an IPv6 address is specified, then the address must be enclosed in square brackets.</span></span>

    ```VB
    Const RemoteComputer = "ComputerName.domain.com"
    ```

    

2.  <span data-ttu-id="9777c-117">Создайте объект [**WSMan**](wsman.md) .</span><span class="sxs-lookup"><span data-stu-id="9777c-117">Create a [**WSMan**](wsman.md) object.</span></span>

    ```VB
    Set objWsman = CreateObject("WSMan.Automation")
    ```

    

3.  <span data-ttu-id="9777c-118">Создайте сеанс, указав транспорт, HTTP или HTTPS, и объедините его с константой, представляющей целевой компьютер.</span><span class="sxs-lookup"><span data-stu-id="9777c-118">Create the session, specifying the transport, HTTP or HTTPS, and concatenating it with the constant representing the target computer.</span></span>

    ```VB
    
    Set objSession = objWsman.CreateSession("https://" & RemoteComputer)
    ```

    

<span data-ttu-id="9777c-119">В следующем примере кода VBScript показан полный скрипт.</span><span class="sxs-lookup"><span data-stu-id="9777c-119">The following VBScript code example shows the complete script.</span></span> <span data-ttu-id="9777c-120">Скрипт включает подпрограммы для преобразования данных из необработанного XML в удобочитаемую форму.</span><span class="sxs-lookup"><span data-stu-id="9777c-120">The script includes a subroutine to transform the data from raw XML to human-readable form.</span></span> <span data-ttu-id="9777c-121">Дополнительные сведения см. [в разделе вывод XML-данных из скриптов WinRM](displaying-xml-output-from-winrm-scripts.md).</span><span class="sxs-lookup"><span data-stu-id="9777c-121">For more information, see [Displaying XML Output from WinRM Scripts](displaying-xml-output-from-winrm-scripts.md).</span></span>


```VB
Const RemoteComputer = "ComputerName.domain.com"

Set objWsman = CreateObject("WSMan.Automation")
Set objSession = objWsman.CreateSession("https://" & RemoteComputer)
strResource = "http://schemas.microsoft.com/wbem/wsman/1/" & _
  "wmi/root/cimv2/Win32_OperatingSystem"
Set objResponse = objSession.Enumerate(strResource)

While Not objResponse.AtEndOfStream
    DisplayOutput(objResponse.ReadItem) 
Wend

'****************************************************
' Displays WinRM XML message using built-in XSL
'****************************************************
Sub DisplayOutput(strWinRMXml)
    Dim xmlFile, xslFile
    Set xmlFile = CreateObject("MSXml.DOMDocument") 
    Set xslFile = CreateObject("MSXml.DOMDocument")
    xmlFile.LoadXml(strWinRMXml)
    xslFile.Load("WsmTxt.xsl")
    Wscript.Echo xmlFile.TransformNode(xslFile) 
End Sub
```



<span data-ttu-id="9777c-122">**Подключение к удаленному компьютеру с помощью другой учетной записи**</span><span class="sxs-lookup"><span data-stu-id="9777c-122">**To connect to a remote computer using a different account**</span></span>

1.  <span data-ttu-id="9777c-123">Укажите конечный компьютер с полным доменным именем или IP-адресом и назначьте его константе.</span><span class="sxs-lookup"><span data-stu-id="9777c-123">Specify the target computer with a fully qualified domain name or an IP address and assign this to a constant.</span></span> <span data-ttu-id="9777c-124">Если указан IPv6-адрес, адрес должен быть заключен в квадратные скобки.</span><span class="sxs-lookup"><span data-stu-id="9777c-124">If an IPv6 address is specified, then the address must be enclosed in square brackets.</span></span>

    ```VB
    Const RemoteComputer = "ComputerName.domain.com"
    ```

    

2.  <span data-ttu-id="9777c-125">Создайте объект [**WSMan**](wsman.md) .</span><span class="sxs-lookup"><span data-stu-id="9777c-125">Create a [**WSMan**](wsman.md) object.</span></span>

    ```VB
    Set objWsman = CreateObject("Wsman.Automation")
    
    ```

    

3.  <span data-ttu-id="9777c-126">Вызовите метод [**WSMan. креатеконнектионоптионс**](wsman-createconnectionoptions.md) , чтобы создать объект [**ConnectionOptions**](connectionoptions.md) .</span><span class="sxs-lookup"><span data-stu-id="9777c-126">Call the [**WSMan.CreateConnectionOptions**](wsman-createconnectionoptions.md) method to create a [**ConnectionOptions**](connectionoptions.md) object.</span></span> <span data-ttu-id="9777c-127">Учетная запись на удаленном компьютере должна быть членом группы администраторов локального компьютера.</span><span class="sxs-lookup"><span data-stu-id="9777c-127">The account on the remote computer must be a member of the local computer administrators group.</span></span>

    ```VB
    Set objConnectionOptions = objWsman.CreateConnectionOptions
    objConnectionOptions.UserName = "Username"
    objConnectionOptions.Password = "Password"
    ```

    

4.  <span data-ttu-id="9777c-128">В вызове [**WSman. CreateSession**](wsman-createsession.md) укажите соответствующие флаги подключения сеанса в параметре *flags* .</span><span class="sxs-lookup"><span data-stu-id="9777c-128">On the [**WSman.CreateSession**](wsman-createsession.md) call, specify the appropriate session connection flags in the *flags* parameter.</span></span> <span data-ttu-id="9777c-129">Дополнительные сведения см. в разделе [константы сеанса](session-constants.md).</span><span class="sxs-lookup"><span data-stu-id="9777c-129">For more information, see [Session Constants](session-constants.md).</span></span> <span data-ttu-id="9777c-130">Укажите конечный компьютер с полным именем компьютера или IP-адресом, а также транспортом — HTTP или HTTPS.</span><span class="sxs-lookup"><span data-stu-id="9777c-130">Specify the target computer with a fully qualified computer name or an IP address and the transport—http or https.</span></span> <span data-ttu-id="9777c-131">Этот сценарий запрашивает проверку подлинности [*Kerberos*](windows-remote-management-glossary.md) из удаленной службы WinRM.</span><span class="sxs-lookup"><span data-stu-id="9777c-131">This script requests [*Kerberos*](windows-remote-management-glossary.md) authentication from the remote WinRM service.</span></span>

    <span data-ttu-id="9777c-132">В отличие от сценариев WMI, в сценариях WinRM можно использовать несколько методов проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="9777c-132">Unlike WMI scripts, you can use several methods of authentication in WinRM scripts.</span></span> <span data-ttu-id="9777c-133">Дополнительные сведения см. в разделе [Проверка подлинности удаленных подключений](authentication-for-remote-connections.md).</span><span class="sxs-lookup"><span data-stu-id="9777c-133">For more information, see [Authentication for Remote Connections](authentication-for-remote-connections.md).</span></span>

    ```VB
    iFlags = objWsman.SessionFlagUseKerberos Or _
      objWsman.SessionFlagCredUserNamePassword
    Set objSession = objWsman.CreateSession("https://" & RemoteComputer, _
      iFlags, objConnectionOptions)
    ```

    

5.  <span data-ttu-id="9777c-134">После того как объект сеанса будет доступен, можно вызвать любой из методов объекта [**Session**](session.md) для получения данных для ресурса.</span><span class="sxs-lookup"><span data-stu-id="9777c-134">After the session object is available, you can call any of the [**Session**](session.md) object methods to obtain data for a resource.</span></span> <span data-ttu-id="9777c-135">Можно получить данные для любого ресурса, доступного на компьютере, на котором выполняется сеанс.</span><span class="sxs-lookup"><span data-stu-id="9777c-135">You can get data for any resource that is available on the computer on which the session is running.</span></span> <span data-ttu-id="9777c-136">Дополнительные сведения см. [в разделе Получение данных с локального компьютера](obtaining-data-from-the-local-computer.md).</span><span class="sxs-lookup"><span data-stu-id="9777c-136">For more information, see [Obtaining Data from the Local Computer](obtaining-data-from-the-local-computer.md).</span></span>

<span data-ttu-id="9777c-137">В следующем примере кода VBScript показан полный скрипт.</span><span class="sxs-lookup"><span data-stu-id="9777c-137">The following VBScript code example shows the complete script.</span></span> <span data-ttu-id="9777c-138">Скрипт включает подпрограммы для преобразования данных из необработанного XML в удобочитаемую форму.</span><span class="sxs-lookup"><span data-stu-id="9777c-138">The script includes a subroutine to transform the data from raw XML to human-readable form.</span></span> <span data-ttu-id="9777c-139">Дополнительные сведения см. [в разделе вывод XML-данных из скриптов WinRM](displaying-xml-output-from-winrm-scripts.md).</span><span class="sxs-lookup"><span data-stu-id="9777c-139">For more information, see [Displaying XML Output from WinRM Scripts](displaying-xml-output-from-winrm-scripts.md).</span></span> <span data-ttu-id="9777c-140">В скрипте указывается проверка подлинности Kerberos, но если удаленный компьютер находится в Рабочей группе, а не в домене, то при указании протокола Kerberos возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="9777c-140">The script specifies Kerberos authentication, but if the remote computer is in a workgroup rather than a domain, specifying Kerberos generates an error.</span></span>


```VB
Const RemoteComputer = "ComputerName.domain.com"

Set objWsman = CreateObject("Wsman.Automation")
Set objConnectionOptions = objWsman.CreateConnectionOptions
objConnectionOptions.UserName = "Username"
objConnectionOptions.Password = "Password"
iFlags = objWsman.SessionFlagUseKerberos Or _
  objWsman.SessionFlagCredUserNamePassword
Set objSession = objWsman.CreateSession("https://" & RemoteComputer, _
  iFlags, objConnectionOptions)
strResource = "http://schemas.microsoft.com/wbem/wsman/1/" & _
  "wmi/root/cimv2/Win32_OperatingSystem"
Set objResponse = objSession.Enumerate(strResource)

While Not objResponse.AtEndOfStream
    DisplayOutput(objResponse.ReadItem) 
Wend

'****************************************************
' Displays WinRM XML message using built-in XSL
'****************************************************
Sub DisplayOutput(strWinRMXml)
    Dim xmlFile, xslFile
    Set xmlFile = CreateObject("MSXml2.DOMDocument.3.0") 
    Set xslFile = CreateObject("MSXml2.DOMDocument.3.0")
    xmlFile.LoadXml(strWinRMXml)
    xslFile.Load("WsmTxt.xsl")
    Wscript.Echo xmlFile.TransformNode(xslFile) 
End Sub
```



## <a name="related-topics"></a><span data-ttu-id="9777c-141">См. также</span><span class="sxs-lookup"><span data-stu-id="9777c-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9777c-142">О служба удаленного управления Windows</span><span class="sxs-lookup"><span data-stu-id="9777c-142">About Windows Remote Management</span></span>](about-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="9777c-143">Использование служба удаленного управления Windows</span><span class="sxs-lookup"><span data-stu-id="9777c-143">Using Windows Remote Management</span></span>](using-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="9777c-144">Справочник по служба удаленного управления Windows</span><span class="sxs-lookup"><span data-stu-id="9777c-144">Windows Remote Management Reference</span></span>](windows-remote-management-reference.md)
</dt> </dl>

 

 