---
title: Отображение выходных данных XML из скриптов WinRM
description: Windows Сценарии удаленного управления возвращают XML, а не объекты. Формат XML не предназначен для восприятия. для преобразования данных в удобочитаемый формат можно использовать методы API MSXML и предварительно установленного XSL-файла.
ms.assetid: a2c9401b-bc1e-4f8e-aabf-b6ade1a849ba
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: df5c27c1fe22ae87395357aeefe681af7c041420d32b7bccbf595fab38bb060b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119680024"
---
# <a name="displaying-xml-output-from-winrm-scripts"></a>Отображение выходных данных XML из скриптов WinRM

Windows Сценарии удаленного управления возвращают XML, а не объекты. Формат XML не предназначен для восприятия. для преобразования данных в удобочитаемый формат можно использовать методы API [MSXML](/previous-versions/windows/desktop/ms763742(v=vs.85)) и предварительно установленного XSL-файла.

дополнительные сведения об xml-выходных данных и примерах xml в формате raw см. [в разделе сценарии в служба удаленного управления Windows](scripting-in-windows-remote-management.md).

Программа командной строки **WinRM** поставляется с файлом преобразования с именем всмткст. xsl, который отображает выходные данные в табличной форме. если скрипт передает этот файл в MSXML методы, выполняющие преобразует данные, выходные данные отображаются так же, как и выходные данные средства **Winrm** .

**Форматирование необработанных выходных данных XML**

1.  Создайте объект [**WSMan**](wsman.md) и создайте сеанс.

    ```VB
    Set Wsman = CreateObject("Wsman.Automation")
    Set Session = Wsman.CreateSession
    ```

    

2.  создание MSXML объектов, представляющих выходные данные XML-ответа и преобразования XSL.

    ```VB
    Set xmlFile = CreateObject( "MSXml.DOMDocument" )
    Set xslFile = CreateObject( "MSXml.DOMDocument" )
    ```

    

3.  Получение данных с помощью методов объекта [**сеанса**](session.md) .

    ```VB
    xmlResponse = Session.Get("http://schemas.microsoft.com/" & _
        "wbem/wsman/1/wmi/root/cimv2/Win32_Service?Name=Spooler")
    ```

    

4.  укажите ответ на метод MSXML [loadXML](/previous-versions/windows/desktop/ms754585(v=vs.85)) и метод [load](/previous-versions/windows/desktop/ms762722(v=vs.85)) для хранения файла преобразования.

    ```VB
    xmlFile.LoadXml(xmlResponse)
    xslFile.Load("WsmTxt.xsl")
    
    ```

    

5.  используйте метод MSXML [transformNode](/previous-versions/windows/desktop/ms761399(v=vs.85)) и отобразите или сохраните выходные данные.

    ```VB
    Wscript.Echo xmlFile.TransformNode(xslFile)
    ```

    

В следующем примере кода VBScript показан полный скрипт.


```VB
Set Wsman = CreateObject("Wsman.Automation")
Set Session = Wsman.CreateSession
Set xmlFile = CreateObject( "MSXml.DOMDocument" )
Set xslFile = CreateObject( "MSXml.DOMDocument" )

xmlResponse = Session.Get("http://schemas.microsoft.com/" & _
    "wbem/wsman/1/wmi/root/cimv2/Win32_Service?Name=Spooler")
xmlFile.LoadXml(xmlResponse)
xslFile.Load("WsmTxt.xsl")
Wscript.Echo xmlFile.TransformNode(xslFile)
```



## <a name="adding-a-portable-subroutine-to-transform-xml-to-your-scripts"></a>Добавление переносимой подпрограммы для преобразования XML в скрипты

Можно добавить подпрограммы в скрипты, использующие предустановленный XSL-файл для преобразования необработанных выходных данных из скрипта WinRM в табличную форму.

следующая подпрограммы использует вызовы методов скрипта MSXML для предоставления выходных данных в всмткст. xsl.


```VB
'****************************************************
' Displays WinRM XML message using built-in XSL
'****************************************************
Sub DisplayOutput(strWinRMXml)
    Set xmlFile = CreateObject("MSXml.DOMDocument") 
    Set xslFile = CreateObject("MSXml.DOMDocument")
    xmlFile.LoadXml(strWinRMXml)
    xslFile.Load("WsmTxt.xsl")
    Wscript.Echo xmlFile.TransformNode(xslFile)
End Sub
```



Следующая подпрограммы преобразует каждую строку данных, как показано в следующем примере.


```VB
Const RemoteComputer = "servername.domain.com"
Set objWsman = CreateObject("WSMan.Automation")
Set objSession = objWsman.CreateSession("https://" & RemoteComputer)
strResource = "http://schemas.microsoft.com/" & _
    "wbem/wsman/1/wmi/root/cimv2/Win32_LogicalDisk"
Set objResultSet = objSession.Enumerate(strResource)
While Not objResultSet.AtEndOfStream
    DisplayOutput(objResultSet.ReadItem)
Wend
Sub DisplayOutput(strWinRMXml)
    Set xmlFile = CreateObject("MSXml.DOMDocument") 
    Set xslFile = CreateObject("MSXml.DOMDocument")
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

 

 