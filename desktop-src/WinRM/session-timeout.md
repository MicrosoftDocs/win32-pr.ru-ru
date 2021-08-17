---
title: Свойство Session. timeout (Всмандисп. h)
description: задает и возвращает максимальное время (в миллисекундах), в течение которого клиентское приложение ожидает служба удаленного управления Windows завершения операций.
ms.assetid: ca35722a-1fd3-48bf-a11b-4624cb81aae3
ms.tgt_platform: multiple
keywords:
- служба удаленного управления Windows свойства времени ожидания
- служба удаленного управления Windows свойства времени ожидания, объект сеанса
- служба удаленного управления Windows объекта сеанса, свойство Timeout
topic_type:
- apiref
api_name:
- Session.Timeout
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4731e4f76ee890bc925a14b69c8ffb3d50e47406939b76183359021242a5fadc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117743245"
---
# <a name="sessiontimeout-property"></a>Свойство Session. timeout

задает и возвращает максимальное время (в миллисекундах), в течение которого клиентское приложение ожидает служба удаленного управления Windows завершения операций.

Это свойство доступно для чтения и записи.

## <a name="syntax"></a>Синтаксис


```VB
Session.Timeout As long
```



## <a name="property-value"></a>Значение свойства

Значение времени ожидания в миллисекундах. При превышении значения времени ожидания возникает ошибка времени выполнения.

## <a name="remarks"></a>Remarks

Значение времени ожидания можно задать до каждой операции, выполняемой агентом. Если значение времени ожидания не указано, агент устанавливает значение времени ожидания.

Во время операции перечисления значение времени ожидания не может быть сброшено во время перечисления ресурса.

## <a name="examples"></a>Примеры

Следующий пример кода VBScript запускает Calc.exe процесс с помощью метода [**CREATE**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process) класса [**\_ процесса Win32**](/windows/desktop/CIMWin32Prov/win32-process) WMI. Параметр *стринпутпараметерс* содержит входные параметры в формате XML. Скрипт задает время ожидания для сеанса.


```VB
Set objWsman = CreateObject( "WSMan.Automation" )
If objWsman is Nothing Then
    WScript.Echo "Failed to create WSMAN Automation object"
    WScript.Quit
End If 

Set objSession = objWsman.CreateSession
If objSession is Nothing Then
    WScript.Echo "Failed to create WSMAN Session object"
    WScript.Quit
End If 

strResource = "http://schemas.microsoft.com/wbem/wsman/1/" & _
    "wmi/root/cimv2/Win32_Process"

'Reset timeout to 10,000 milliseconds
objSession.Timeout = 10000     

strInputParameters = "<p:Create_INPUT " & _
    "xmlns:p=""http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_Process"">" & _
    "<p:CommandLine>" & "calc.exe" & _
    "</p:CommandLine>" & _
    "</p:Create_INPUT>"

strOutputParameters = objSession.Invoke( "Create", _
    strResource, strInputParameters )

DisplayOutput( strOutputParameters )

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



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                 |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                           |
| Заголовок<br/>                   | <dl> <dt>Всмандисп. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Всмандисп. idl</dt> </dl> |
| Библиотека<br/>                  | <dl> <dt>Всмандисп. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Сеанс**](session.md)
</dt> </dl>

 

