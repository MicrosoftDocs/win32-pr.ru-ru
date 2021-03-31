---
title: Получение данных с локального компьютера
description: Хотя протокол служба удаленного управления Windows и WS-Management специально разработан для удаленного подключения, в самом простом случае устанавливается сеанс на локальном компьютере.
ms.assetid: 7f08b557-bbd4-4f67-b5e5-b84e8af58657
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ccb71fd176bf3faf425ea57d06beb27788f41a62
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103791706"
---
# <a name="obtaining-data-from-the-local-computer"></a>Получение данных с локального компьютера

Хотя протокол служба удаленного управления Windows и WS-Management специально разработан для удаленного подключения, в самом простом случае устанавливается сеанс на локальном компьютере. Для некоторых сценариев может потребоваться доступ к данным на локальном компьютере, а также к удаленным компьютерам.

**WinRM версии 2,0:  **

Все операции считаются удаленными, и служба WinRM должна быть запущена до выполнения любой операции. Если удаленное назначение не указано, по умолчанию используется localhost, и все операции будут отправляться в локальную службу WinRM. Дополнительные сведения о запуске службы WinRM см. в разделе [Установка и настройка для служба удаленного управления Windows](installation-and-configuration-for-windows-remote-management.md).

При использовании службы WinRM для локальных операций следует учитывать следующие факторы.

-   Локальная конфигурация WinRM может быть прочитана только администраторами.
-   Пространства имен WMI должны иметь набор разрешений Remote Enable. Дополнительные сведения см. [в разделе Защита удаленного WMI-подключения](../wmisdk/securing-a-remote-wmi-connection.md).
-   Если [*прослушиватель*](windows-remote-management-glossary.md) WinRM не создан, служба WinRM прослушивает локальные запросы через порт 47001.

Каждый сценарий WinRM должен начаться с установления сеанса или соединения с компьютером путем создания объекта [**сеанса**](session.md) . После создания сеанса можно использовать методы объекта **сеанса** , такие как [**Session. Enumerate**](session-enumerate.md) или [**Session. Invoke**](session-invoke.md) , для получения данных или для выполнения методов.

Создание сеанса в некоторой степени похоже на [Подключение](/windows/desktop/WmiSdk/wmi-tasks--connecting-to-the-wmi-service) к пространству имен инструментарий управления Windows (WMI) ([WMI](/windows/desktop/WmiSdk/wmi-start-page)). Сеанс по сути является слоем, который позволяет отправлять и получать данные через сообщения [*SOAP*](windows-remote-management-glossary.md) и протокол WS-Management. Дополнительные сведения см. в разделе [протокол WS-Management](ws-management-protocol.md).

Вызов метода [**WSMan. CreateSession**](wsman-createsession.md) для создания объекта [**сеанса**](session.md) приведет к запуску [*сеанса*](windows-remote-management-glossary.md) , который подключается к локальному WinRM.

**Создание сеанса WSMan и получение данных**

1.  Создайте объект [**WSMan**](wsman.md) .

    ```VB
    Set objWsman = CreateObject("Wsman.Automation")
    ```

    

2.  Создайте сеанс, вызвав метод [**WSMan. CreateSession**](wsman-createsession.md) . Этот сеанс выполняется с именем пользователя и паролем для входа и может получать данные через локальный WinRM.

    ```VB
    Set objSession = objWsman.CreateSession()
    ```

    

3.  Создайте [*URI*](windows-remote-management-glossary.md) ресурса для определения [*ресурса*](windows-remote-management-glossary.md) , которым требуется управлять или для которого требуется получить данные. Дополнительные сведения о форматировании URI см. в разделе [URI ресурсов](resource-uris.md). Этот URI ресурса предназначен для конкретного экземпляра класса [**\_ службы Win32**](/windows/desktop/CIMWin32Prov/win32-service) WMI, службы Winmgmt. Дополнительные сведения см. в разделе [Служба удаленного управления Windows и инструментарий WMI](windows-remote-management-and-wmi.md).

    ```VB
    strResource = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_Service?Name=Winmgmt"
    ```

    

4.  Вызывайте методы [**сеанса**](session.md) , которые получают или перечисляют данные с помощью URI ресурса. Дополнительные сведения см. в разделе [API сценариев WinRM](winrm-scripting-api.md).

    ```VB
    strResponse = objSession.Get(strResource)
    Wscript.Echo strResponse
    ```

    

5.  Сведения о получении или управлении данными с другого компьютера или использовании различных методов проверки подлинности см. в разделе [Получение данных с удаленного компьютера](obtaining-data-from-a-remote-computer.md).

В следующем примере кода VBScript показан полный скрипт, который получает конкретный экземпляр [**\_ службы Win32**](/windows/desktop/CIMWin32Prov/win32-service) инструментария WMI с именем Winmgmt.


```VB
Set objWsman = CreateObject("Wsman.Automation")
Set objSession = objWsman.CreateSession()
strResource = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_Service?Name=Winmgmt"
strResponse = objSession.Get(strResource)
Wscript.Echo strResponse
```



В следующем примере кода VBScript показан полный скрипт с преобразованием данных. Дополнительные сведения см. [в разделе вывод XML-данных из скриптов WinRM](displaying-xml-output-from-winrm-scripts.md).


```VB
Set objWsman = CreateObject("Wsman.Automation")
Set objSession = objWsman.CreateSession()
strResource = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_Service?Name=Winmgmt"
strResponse = objSession.Get(strResource)
Set xmlFile = CreateObject("MSXml.DOMDocument")
Set xslFile = CreateObject("MSXml.DOMDocument")
xmlFile.LoadXml(strResponse)
xslFile.Load("WsmTxt.xsl")
Wscript.Echo xmlFile.TransformNode(xslFile)

```



## <a name="related-topics"></a>См. также

<dl> <dt>

[О служба удаленного управления Windows](about-windows-remote-management.md)
</dt> <dt>

[Использование служба удаленного управления Windows](using-windows-remote-management.md)
</dt> <dt>

[Справочник по служба удаленного управления Windows](windows-remote-management-reference.md)
</dt> </dl>

 

 