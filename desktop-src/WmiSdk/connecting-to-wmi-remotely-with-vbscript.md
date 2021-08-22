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
ms.openlocfilehash: 9ccdd4466273cdc3b49399abf30915a975418433183d821482a8fa92920d52d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118819692"
---
# <a name="connecting-to-wmi-remotely-with-vbscript"></a>Удаленное подключение к инструментарию WMI с помощью VBScript

Вы можете создать удаленное подключение к инструментарию WMI с помощью VBScript, создав объект соединения. Этот объект содержит имя компьютера, пространство имен WMI, к которому необходимо подключиться, а также соответствующие учетные данные и уровни проверки подлинности.

**Подключение к удаленной системе с помощью VBScript**

1.  Укажите сведения о соединении, такие как имя удаленного компьютера, учетные данные и уровень проверки подлинности для подключения.

    При подключении к удаленному компьютеру с использованием тех же учетных данных (домен и имя пользователя), которые вошли в систему, можно указать сведения о соединении в [моникере](constructing-a-moniker-string.md) [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject), как описано в следующем примере кода.

    ```VB
    strComputer = "Computer_B"
    Set objWMIService = GetObject("winmgmts:{impersonationLevel=Impersonate}!\\" & strComputer & "\Root\CIMv2")
    ```

    

    В общем случае следует указать пространство имен WMI для подключения к удаленному компьютеру. Это связано с тем, что пространство имен по умолчанию может не совпадать на разных компьютерах. Указание пространства имен гарантирует подключение к одному и тому же пространству имен на всех компьютерах.

    Дополнительные сведения о константах VBScript и строках сценариев для использования моникера Connection см. в разделе [Задание уровня безопасности процесса по умолчанию с помощью VBScript](setting-the-default-process-security-level-using-vbscript.md).

2.  Если вы подключаетесь к удаленному компьютеру в другом домене или используете другое имя пользователя и пароль, необходимо использовать метод [**SWbemLocator. коннектсервер**](swbemlocator-connectserver.md) .

    Как и в случае с моникером, вы используете **коннектсервер** для указания учетных данных, уровня проверки подлинности и пространства имен для удаленного подключения. В следующем примере кода описывается использование Коннектсервер для доступа к удаленному компьютеру с использованием учетной записи администратора и пароля.

    ```VB
    strComputer = "Computer_B"
    Set objSWbemLocator = CreateObject("WbemScripting.SWbemLocator")
    Set objSWbemServices = objSWbemLocator.ConnectServer(strComputer, _
                                                         "Root\CIMv2", _
                                                         "fabrikam\administrator", _
                                                         "password")
    ```

    

3.  При использовании функции [**коннектсервер**](swbemlocator-connectserver.md) для удаленных соединений настройте олицетворение и проверку подлинности для объекта безопасности, полученного при вызове [**SwbemServices. Security**](swbemservices-security-.md). Для указания уровня олицетворения можно использовать перечисление [вбемимперсонатионлевеленум](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemimpersonationlevelenum) .

    В следующем примере кода задается уровень олицетворения для предыдущего примера кода VBScript.

    ```VB
    objSWbemServices.Security_.ImpersonationLevel = 3
    ```

    

    Обратите внимание, что для некоторых подключений требуется определенный уровень проверки подлинности. Дополнительные сведения см. в разделе [Установка клиентских приложений безопасность](setting-client-application-process-security.md) и [Защита клиентов скриптов](securing-scripting-clients.md).

    В частности, следует задать уровень проверки подлинности **RPC \_ C \_ AUTHN \_ уровня " \_ PKT \_** " или 6, если для пространства имен, к которому выполняется подключение на удаленном компьютере, требуется зашифрованное соединение, прежде чем оно вернет данные. Этот уровень проверки подлинности также можно использовать, даже если пространство имен не требуется. Это гарантирует, что данные шифруются по мере пересечения сети. Если попытаться задать более низкий уровень проверки подлинности, чем разрешено, будет возвращено сообщение об отказе в доступе. Дополнительные сведения см. в разделе [требуется зашифрованное соединение с пространством имен](requiring-an-encrypted-connection-to-a-namespace.md).

После установки соединения можно продолжить доступ к данным WMI. Дополнительные сведения см. в разделе [задачи WMI для скриптов и приложений](wmi-tasks-for-scripts-and-applications.md).

## <a name="examples"></a>Примеры

Более крупный пример на языке VBScript см. в разделе "примеры" на странице справочника по [**SWbemLocator. коннектсервер**](swbemlocator-connectserver.md) .

Следующий пример кода VBScript подключается к группе удаленных компьютеров в том же домене, создавая массив имен удаленных компьютеров, а затем отображая имена самонастраивающийся устройств — экземпляры [**Win32 \_ пнпентити**](/windows/desktop/CIMWin32Prov/win32-pnpentity)— на каждом компьютере. Для выполнения приведенного ниже сценария необходимы права администратора на удаленных компьютерах. Обратите внимание, что параметр " \\ \\ ", необходимый перед именем удаленного компьютера, добавляется скриптом после настройки уровня олицетворения. Дополнительные сведения о путях WMI см. [в разделе Описание расположения объекта WMI](describing-the-location-of-a-wmi-object.md).


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



Следующий пример кода VBScript позволяет подключиться к удаленному компьютеру с использованием других учетных данных. Например, удаленный компьютер в другом домене или подключение к удаленному компьютеру, для которого требуется другое имя пользователя и пароль. В этом случае используйте подключение [**SwbemServices. коннектсервер**](swbemlocator-connectserver.md) .


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



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Подключение к инструментарию WMI на удаленном компьютере](connecting-to-wmi-on-a-remote-computer.md)
</dt> </dl>

 

 
