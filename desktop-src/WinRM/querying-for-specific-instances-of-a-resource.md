---
title: Запрос конкретных экземпляров ресурса
description: Вызов Session. Enumerate имеет необязательные параметры, которые позволяют уменьшить перечисление в запрос.
ms.assetid: 69d2fe79-9aad-4c8c-a65e-c6bb0e51c063
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 30ae068c712dd04ba892220657ad64820a890040
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105700869"
---
# <a name="querying-for-specific-instances-of-a-resource"></a>Запрос конкретных экземпляров ресурса

Вызов [**Session. Enumerate**](session-enumerate.md) имеет необязательные параметры, которые позволяют уменьшить перечисление в запрос. Так как [API-интерфейсы WinRM](winrm-scripting-api.md) и [API для WinRM](winrm-c---api.md) в тесно моделируются по базовому протоколу WS-Management, параметры используют одну и ту же терминологию для запросов в качестве *диалекта* протокола —*фильтра* и фильтра.

Можно использовать параметры Filter и диалекта [**Session. Enumerate**](session-enumerate.md) , либо можно создать и предоставить объект [**ResourceLocator**](resourcelocator.md) и метод [**аддселектор**](resourcelocator-addselector.md) , но нельзя выполнить оба действия.

Эта процедура выполняет запрос для сетевых адаптеров, которые привязаны к TCP/IP и включены. Запрос запрашивает все экземпляры [**Win32 \_ NetworkAdapterConfiguration**](/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration) , для которых свойство **IpEnabled** имеет значение **true**. За исключением добавления *фильтра* и *диалекта*, запрос обрабатывается как простое перечисление.

В этом примере имя ресурса для константы ресурса представлено звездочкой " \* ", поскольку имя класса [**Win32 \_ NetworkAdapterConfiguration**](/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration)уже упоминается в строке *стрфилтер* .

**Запрос конкретных экземпляров ресурса**

1.  Для простоты чтения определите URI как константы.

    ```VB
    Const RemoteComputer = "servername.domain.com"
    Const Resource = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/*"
    Const Dialect = "http://schemas.microsoft.com/wbem/wsman/1/WQL"
    ```

    

2.  Создание сеанса.

    ```VB
    Set objWsman = CreateObject("Wsman.Automation")
    Set objSession = objWsman.CreateSession("https://" & RemoteComputer)
    ```

    

3.  Создайте строку фильтра. Служба удаленного управления Windows поддерживает [WQL](/windows/desktop/WmiSdk/wql-sql-for-wmi) в качестве диалекта фильтра.

    ```VB
    strFilter = "SELECT * FROM Win32_NetworkAdapterConfiguration WHERE IpEnabled=TRUE"
    ```

    

4.  Задайте необходимые [**константы перечисления**](enumeration-constants.md) в параметре *flags* .

    Имейте в виду, что если флаги включают в себя [**константы перечисления**](enumeration-constants.md) **всманфлагхиерарчидипбасепропсонли** или **всманфлагхиерарчишаллов** , служба WinRM возвращает код ошибки **Error, \_ \_ \_ \_ не поддерживаемый режимом полиморфизма WSMan**.

5.  Вызовите метод [**Session. Enumerate**](session-enumerate.md) . Этот вызов запускает перечисление. Метод **Session. Enumerate** устанавливает WS-Management контекст перечисления протокола, который сохраняется в объекте [**перечислителя**](enumerator.md) .

    ```VB
    Set objResultSet = objSession.Enumerate(Resource, strFilter, Dialect)
    ```

    

6.  Вызовите метод [**Enumerator. ReadItem**](enumerator-readitem.md) , чтобы получить следующий элемент результатов. В WS-Management Protocol это соответствует операции извлечения. Используйте метод [**Enumerator. атендофстреам**](enumerator-atendofstream.md) в качестве элемента управления, чтобы выяснить, когда следует прерывать чтение.

    ```VB
    While Not objResultSet.AtEndOfStream
        DisplayOutput(objResultSet.ReadItem)
    Wend
    ```

    

В следующем примере кода VBScript показан полный скрипт.


```VB
Const RemoteComputer = "servername.domain.com"
Const Resource = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/*"
Const Dialect = "http://schemas.microsoft.com/wbem/wsman/1/WQL"

Set objWsman = CreateObject("Wsman.Automation")
Set objSession = objWsman.CreateSession("https://" & RemoteComputer)

strFilter = "SELECT * FROM Win32_NetworkAdapterConfiguration WHERE IpEnabled=TRUE"

Set objResultSet = objSession.Enumerate(Resource, strFilter, Dialect)

While Not objResultSet.AtEndOfStream
    DisplayOutput(objResultSet.ReadItem)
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



## <a name="related-topics"></a>См. также

<dl> <dt>

[Использование служба удаленного управления Windows](using-windows-remote-management.md)
</dt> <dt>

[Перечисление или вывод всех экземпляров ресурса](enumerating-or-listing-all-instances-of-a-resource.md)
</dt> <dt>

[**ResourceLocator**](resourcelocator.md)
</dt> </dl>

 

 