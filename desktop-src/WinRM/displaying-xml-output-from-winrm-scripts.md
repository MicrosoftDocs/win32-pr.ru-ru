---
title: Отображение выходных данных XML из скриптов WinRM
description: Служба удаленного управления Windows скрипты возвращают XML, а не объекты. Формат XML не предназначен для восприятия. Для преобразования данных в удобочитаемый формат можно использовать методы API MSXML и предварительно установленный XSL-файл.
ms.assetid: a2c9401b-bc1e-4f8e-aabf-b6ade1a849ba
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c70dd0a61181f6fc61e685641ff0ed5e3d43ffe8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104070397"
---
# <a name="displaying-xml-output-from-winrm-scripts"></a>Отображение выходных данных XML из скриптов WinRM

Служба удаленного управления Windows скрипты возвращают XML, а не объекты. Формат XML не предназначен для восприятия. Для преобразования данных в удобочитаемый формат можно использовать методы API [MSXML](/previous-versions/windows/desktop/ms763742(v=vs.85)) и предварительно установленный XSL-файл.

Дополнительные сведения об XML-выходных данных и примерах XML в формате RAW см. [в разделе сценарии в Служба удаленного управления Windows](scripting-in-windows-remote-management.md).

Программа командной строки **WinRM** поставляется с файлом преобразования с именем всмткст. xsl, который отображает выходные данные в табличной форме. Если скрипт передает этот файл методам MSXML, выполняющим преобразует данные, выходные данные отображаются так же, как и выходные данные средства **WinRM** .

**Форматирование необработанных выходных данных XML**

1.  Создайте объект [**WSMan**](wsman.md) и создайте сеанс.

    ```VB
    Set Wsman = CreateObject("Wsman.Automation")
    Set Session = Wsman.CreateSession
    ```

    

2.  Создание объектов MSXML, представляющих выходные данные XML-ответа и преобразования XSL.

    ```VB
    Set xmlFile = CreateObject( "MSXml.DOMDocument" )
    Set xslFile = CreateObject( "MSXml.DOMDocument" )
    ```

    

3.  Получение данных с помощью методов объекта [**сеанса**](session.md) .

    ```VB
    xmlResponse = Session.Get("http://schemas.microsoft.com/" & _
        "wbem/wsman/1/wmi/root/cimv2/Win32_Service?Name=Spooler")
    ```

    

4.  Укажите ответ на метод MSXML [LoadXml](/previous-versions/windows/desktop/ms754585(v=vs.85)) и метод [Load](/previous-versions/windows/desktop/ms762722(v=vs.85)) для хранения файла преобразования.

    ```VB
    xmlFile.LoadXml(xmlResponse)
    xslFile.Load("WsmTxt.xsl")
    
    ```

    

5.  Используйте метод [TRANSFORMNODE](/previous-versions/windows/desktop/ms761399(v=vs.85)) MSXML и отобразите или сохраните выходные данные.

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

Следующая подпрограммы использует вызовы методов создания скриптов MSXML для предоставления выходных данных в Всмткст. xsl.


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



## <a name="related-topics"></a>См. также

<dl> <dt>

[О служба удаленного управления Windows](about-windows-remote-management.md)
</dt> <dt>

[Использование служба удаленного управления Windows](using-windows-remote-management.md)
</dt> <dt>

[Справочник по служба удаленного управления Windows](windows-remote-management-reference.md)
</dt> </dl>

 

 