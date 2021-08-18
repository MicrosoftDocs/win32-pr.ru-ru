---
title: Перечисление или составление списка всех экземпляров ресурса
description: метод Session. enumerate является служба удаленного управления Windowsным подходом для получения всех экземпляров указанного ресурса.
ms.assetid: c50c37bf-e19a-473b-8d27-ab3bb4ec86a0
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1f510d0e0cc8115ca4dca7c7e46dd5e987ef0dd15dd4fa7d92e47d737e467d8f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119679994"
---
# <a name="enumerating-or-listing-all-instances-of-a-resource"></a>Перечисление или составление списка всех экземпляров ресурса

метод [**Session. enumerate**](session-enumerate.md) является служба удаленного управления Windowsным подходом для получения всех экземпляров указанного ресурса.

Метод [**Session. Enumerate**](session-enumerate.md) не получает коллекцию в объекте [**SWbemObjectSet**](/windows/desktop/WmiSdk/swbemobjectset) , например [**SWbemService.ExeКкуери**](/windows/desktop/WmiSdk/swbemservices-execquery) Call с [запросом WMI](/windows/desktop/WmiSdk/querying-wmi) в качестве параметра (например, `ExecQuery("SELECT * from Win32_LogicalDisk")` ), или вызов метода, например [**SWbemObject. Instances \_**](/windows/desktop/WmiSdk/swbemobject-instances-). Метод **Session. Enumerate** и объект [**перечислителя**](enumerator.md) гораздо более похож на операцию объекта [TextStream](/previous-versions//312a5kbt(v=vs.85)) скриптов, который используется для чтения файлов в виде потока.

Чтобы считать файлы в виде текстового потока, необходимо создать объект скрипта [TextStream](/previous-versions//312a5kbt(v=vs.85)) и вызвать метод [TextStream. ReadLine](/previous-versions//h7se9d4f(v=vs.85)) для чтения каждой строки файла. Аналогичным образом можно вызвать метод [**Session. Enumerate**](session-enumerate.md) , чтобы получить объект [**перечислителя**](enumerator.md) и вызвать метод [**Enumerator. ReadItem**](enumerator-readitem.md) для получения следующего элемента. Как и при чтении из текстового файла, можно вызвать свойство [**Enumerator. атендофстреам**](enumerator-atendofstream.md) , чтобы проверить, достигли ли вы конца элементов данных.

**Перечисление ресурсов**

1.  Создание сеанса.

    ```VB
    Const RemoteComputer = "servername.domain.com"
    Set objWsman = CreateObject( "WSMan.Automation" )
    Set objSession = objWsman.CreateSession( "https://" _
        & RemoteComputer )
    ```

    

2.  Создайте универсальный код ресурса (URI) для обнаружения ресурса.

    ```VB
    strResource = "http://schemas.microsoft.com/wbem/wsman/1/" &_
                 "wmi/root/cimv2/Win32_ScheduledJob"
    ```

    

3.  Вызовите метод [**Session. Enumerate**](session-enumerate.md) . Этот вызов запускает перечисление. В WinRM операция перечисления не получает коллекцию точно так же, как это делает WMI. Вместо этого метод **Session. Enumerate** устанавливает WS-Management контекст перечисления протокола, который поддерживается в объекте [**перечислителя**](enumerator.md) .

    ```VB
    Set EnumJobs = objSession.Enumerate( strResource )
    ```

    

4.  Вызовите метод [**Enumerator. ReadItem**](enumerator-readitem.md) , чтобы получить следующий элемент результатов. В WS-Management Protocol это соответствует операции извлечения. Используйте метод [**Enumerator. атендофстреам**](enumerator-atendofstream.md) в качестве элемента управления, чтобы выяснить, когда следует прерывать чтение.

    ```VB
    While Not EnumJobs.AtEndOfStream
        NumOfJobs = NumOfJobs + 1
        DisplayOutput( EnumJobs.ReadItem ) 
    Wend
    ```

    

В следующем примере кода VBScript показан полный скрипт.


```VB
Const RemoteComputer = "servername.domain.com"
Set objWsman = CreateObject( "WSMan.Automation" )
Set objSession = objWsman.CreateSession( "https://" & RemoteComputer )
strResource = "http://schemas.microsoft.com/wbem/wsman/1/" &_
              "wmi/root/cimv2/Win32_ScheduledJob"

Set EnumJobs = objSession.Enumerate( strResource )
NumOfJobs = 0
While Not EnumJobs.AtEndOfStream
    NumOfJobs = NumOfJobs + 1
    DisplayOutput( EnumJobs.ReadItem ) 
Wend
Wscript.Echo "There are " & NumOfJobs & " jobs scheduled."

'****************************************************
' Displays WinRM XML message using built-in XSL
'****************************************************
Sub DisplayOutput( strWinRMXml )
    Dim xmlFile, xslFile
    Set xmlFile = CreateObject( "MSXml2.DOMDocument.3.0" ) 
    Set xslFile = CreateObject( "MSXml2.DOMDocument.3.0" )
    xmlFile.LoadXml( strWinRMXml )
    xslFile.Load( "WsmTxt.xsl" )
    Wscript.Echo xmlFile.TransformNode( xslFile ) 
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

 

 