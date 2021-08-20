---
title: Получение данных с удаленного компьютера
description: Можно получить данные или управлять ресурсами на удаленных компьютерах, а также на локальном компьютере. подключение к удаленному компьютеру в служба удаленного управления Windows сценария очень похоже на создание локального соединения.
ms.assetid: 578eee80-a6c1-4456-9683-14e0a3386248
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: cf3531e19c0848691ededa0c3b6b2fad642de33c2a5f2d465ac899716970a512
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118823411"
---
# <a name="obtaining-data-from-a-remote-computer"></a>Получение данных с удаленного компьютера

Можно получить данные или управлять ресурсами на удаленных компьютерах, а также на локальном компьютере. подключение к удаленному компьютеру в служба удаленного управления Windows сценария очень похоже на создание локального соединения. Данные экземпляра WMI доступны, и, если на удаленном компьютере установлено оборудование BMC, которое может обмениваться данными по протоколу WS-Management, то доступны также данные [интеллектуального управления платформой (IPMI)](/previous-versions/windows/desktop/ipmiprv/ipmi-provider) . дополнительные сведения см. в разделе [служба удаленного управления Windows и инструментарий WMI](windows-remote-management-and-wmi.md) и [удаленное управление оборудованием](remote-hardware-management.md).

Может потребоваться создать объект [**ConnectionOptions**](connectionoptions.md) , чтобы указать сведения о типе проверки подлинности, запрашиваемом для входа в систему.

Если учетная запись на удаленном компьютере имеет одинаковое имя пользователя и пароль для входа, необходимы только дополнительные сведения: транспорт, имя домена и имя компьютера. Из-за [контроля учетных записей пользователей](https://support.microsoft.com/help/922708/how-to-use-user-account-control-uac-in-windows-vista)удаленная учетная запись должна быть учетной записью домена и членом группы администраторов удаленного компьютера. Если учетная запись является членом локальной группы "Администраторы", то UAC не разрешает доступ к службе WinRM. чтобы получить доступ к удаленной службе удаленного управления windows в рабочей группе, необходимо отключить фильтрацию контроля учетных записей для локальных учетных записей, создав следующую запись реестра DWORD и установив для нее значение 1: **\[ HKEY \_ local \_ MACHINE \\ SOFTWARE \\ Microsoft \\ Windows \\ CurrentVersion \\ политики \\ System \] LocalAccountTokenFilterPolicy**.

**Подключение к удаленному компьютеру с использованием имени пользователя и пароля для входа**

1.  Укажите конечный компьютер с полным доменным именем или IP-адресом и назначьте его константе. Если указан IPv6-адрес, адрес должен быть заключен в квадратные скобки.

    ```VB
    Const RemoteComputer = "ComputerName.domain.com"
    ```

    

2.  Создайте объект [**WSMan**](wsman.md) .

    ```VB
    Set objWsman = CreateObject("WSMan.Automation")
    ```

    

3.  Создайте сеанс, указав транспорт, HTTP или HTTPS, и объедините его с константой, представляющей целевой компьютер.

    ```VB
    
    Set objSession = objWsman.CreateSession("https://" & RemoteComputer)
    ```

    

В следующем примере кода VBScript показан полный скрипт. Скрипт включает подпрограммы для преобразования данных из необработанного XML в удобочитаемую форму. Дополнительные сведения см. [в разделе вывод XML-данных из скриптов WinRM](displaying-xml-output-from-winrm-scripts.md).


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



**Подключение к удаленному компьютеру с помощью другой учетной записи**

1.  Укажите конечный компьютер с полным доменным именем или IP-адресом и назначьте его константе. Если указан IPv6-адрес, адрес должен быть заключен в квадратные скобки.

    ```VB
    Const RemoteComputer = "ComputerName.domain.com"
    ```

    

2.  Создайте объект [**WSMan**](wsman.md) .

    ```VB
    Set objWsman = CreateObject("Wsman.Automation")
    
    ```

    

3.  Вызовите метод [**WSMan. креатеконнектионоптионс**](wsman-createconnectionoptions.md) , чтобы создать объект [**ConnectionOptions**](connectionoptions.md) . Учетная запись на удаленном компьютере должна быть членом группы администраторов локального компьютера.

    ```VB
    Set objConnectionOptions = objWsman.CreateConnectionOptions
    objConnectionOptions.UserName = "Username"
    objConnectionOptions.Password = "Password"
    ```

    

4.  В вызове [**WSman. CreateSession**](wsman-createsession.md) укажите соответствующие флаги подключения сеанса в параметре *flags* . Дополнительные сведения см. в разделе [константы сеанса](session-constants.md). Укажите конечный компьютер с полным именем компьютера или IP-адресом, а также транспортом — HTTP или HTTPS. Этот сценарий запрашивает проверку подлинности [*Kerberos*](windows-remote-management-glossary.md) из удаленной службы WinRM.

    В отличие от сценариев WMI, в сценариях WinRM можно использовать несколько методов проверки подлинности. Дополнительные сведения см. в разделе [Проверка подлинности удаленных подключений](authentication-for-remote-connections.md).

    ```VB
    iFlags = objWsman.SessionFlagUseKerberos Or _
      objWsman.SessionFlagCredUserNamePassword
    Set objSession = objWsman.CreateSession("https://" & RemoteComputer, _
      iFlags, objConnectionOptions)
    ```

    

5.  После того как объект сеанса будет доступен, можно вызвать любой из методов объекта [**Session**](session.md) для получения данных для ресурса. Можно получить данные для любого ресурса, доступного на компьютере, на котором выполняется сеанс. Дополнительные сведения см. [в разделе Получение данных с локального компьютера](obtaining-data-from-the-local-computer.md).

В следующем примере кода VBScript показан полный скрипт. Скрипт включает подпрограммы для преобразования данных из необработанного XML в удобочитаемую форму. Дополнительные сведения см. [в разделе вывод XML-данных из скриптов WinRM](displaying-xml-output-from-winrm-scripts.md). В скрипте указывается проверка подлинности Kerberos, но если удаленный компьютер находится в Рабочей группе, а не в домене, то при указании протокола Kerberos возникает ошибка.


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



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[о служба удаленного управления Windows](about-windows-remote-management.md)
</dt> <dt>

[использование служба удаленного управления Windows](using-windows-remote-management.md)
</dt> <dt>

[Windows Справочник по удаленному управлению](windows-remote-management-reference.md)
</dt> </dl>

 

 