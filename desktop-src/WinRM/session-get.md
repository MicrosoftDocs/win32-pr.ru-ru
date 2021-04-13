---
title: Метод Session. Get (Всмандисп. h)
description: Извлекает ресурс, указанный с помощью URI, и возвращает XML-представление текущего экземпляра ресурса.
ms.assetid: 873242fd-9da3-42f4-a18e-258fedba77ec
ms.tgt_platform: multiple
keywords:
- Получение метода служба удаленного управления Windows
- Получение метода служба удаленного управления Windows, объект Session
- Объект Session служба удаленного управления Windows, метод Get
topic_type:
- apiref
api_name:
- Session.Get
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e4ee84cc711db312389151d1dd95fb890474dcd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104341020"
---
# <a name="sessionget-method"></a>Session. Get, метод

Извлекает ресурс, указанный с помощью [*URI*](windows-remote-management-glossary.md) , и возвращает XML-представление текущего экземпляра ресурса.

## <a name="syntax"></a>Синтаксис


```VB
Session.Get( _
  ByVal resourceUri, _
  [ ByVal flags ] _
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*resourceUri* \[ окне\]
</dt> <dd>

Идентификатор извлекаемого ресурса.

Этот параметр может содержать одно из следующих:

-   Универсальный код ресурса (URI) с [*селекторами*](windows-remote-management-glossary.md)или без них. При вызове метода **Get** с селектором для получения ресурса WMI используйте ключевое свойство или свойства объекта. Например, в Visual Basic приведенном ниже примере кода сценария VBScript ключ задается с помощью `Win32_Service?Name=winmgmt` . Для одноэлементных классов, таких как [**Win32 \_ localtime**](/previous-versions/windows/desktop/wmitimepprov/win32-localtime), нельзя использовать селектор.

    ```VB
    strResourceUri = "http://schemas.microsoft.com/" _ 
        & "wbem/wsman/1/wmi/root/cimv2/Win32_Service?Name=winmgmt"

    strResourceUri = "http://schemas.microsoft.com/" _ 
        & "wbem/wsman/1/wmi/root/cimv2/Win32_LocalTime"
    ```

    

-   Объект [**ResourceLocator**](resourcelocator.md) , который может содержать селекторы, [*фрагменты*](windows-remote-management-glossary.md)или [*Параметры*](windows-remote-management-glossary.md).
-   Ссылка на конечную точку [*WS-Addressing*](windows-remote-management-glossary.md) , как описано в стандарте протокола WS-Management. Дополнительные сведения о общедоступной спецификации для [протокол WS-Management](ws-management-protocol.md)см. на [странице индекс спецификаций управления](/previous-versions/dotnet/articles/ms951267(v=msdn.10)).

</dd> <dt>

*Флаги* \[ в необязательное\]
</dt> <dd>

Зарезервировано. Должен иметь значение 0.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

XML-представление ресурса.

## <a name="examples"></a>Примеры

В следующем примере кода VBScript извлекается XML-представление экземпляра [**\_ службы Win32**](/windows/desktop/CIMWin32Prov/win32-service) , представляющего службу WMI Winmgmt на локальном компьютере.


```VB

'Create a WSMan object.
Set objWsman = CreateObject( "WSMAN.Automation" )
If objWsman is Nothing Then
    WScript.Echo "Failed to create WSMAN Automation object"
    WScript.Quit
End If 

'Create a Session object.
Set objSession = objWsman.CreateSession
If objSession is Nothing Then
    WScript.Echo "Failed to create WSMAN Session object"
    WScript.Quit
End If 


strResourceUri = "http://schemas.microsoft.com/" _ 
    & "wbem/wsman/1/wmi/root/cimv2/Win32_Service?Name=winmgmt"

On Error Resume Next
xmlResource = objSession.Get( strResourceUri )
WScript.Echo "Response message: " & Chr(10) & xmlResource
If Err.Number <> 0 Then
    DisplayErrorInfo
End If
On Error Goto 0

Sub DisplayErrorInfo()
    WScript.Echo "An error has occurred."     
    WScript.Echo
    WScript.Echo "Error Info"
    WScript.Echo "-----------"
    WScript.Echo "Number      : 0x" & hex(Err.number)
    WScript.Echo "Description : " & Err.Description
    WScript.Echo "Source      : " & Err.Source
    WScript.Echo "HelpFile    : " & Err.helpfile
    WScript.Echo "HelpContext : " & Err.HelpContext    
    WScript.Echo Err.Clear    
End Sub

```



Следующий пример кода VBScript извлекает экземпляр службы WMI Winmgmt с удаленного компьютера. Удаленный компьютер определяется полным доменным именем (servername.domain.com). Единственное различие между локальной и удаленной версиями — спецификация удаленного компьютера в вызове [**WSMan. CreateSession**](wsman-createsession.md).


```VB
Const RemoteComputer = "servername.domain.com"

'Create a WSMan object.
Set objWsman = CreateObject( "WSMAN.Automation" )
If objWsman is Nothing Then
    WScript.Echo "Failed to create WSMAN Automation object"
    WScript.Quit
End If 

'Create a Session object.
Dim objSession
Set objSession = objWsman.CreateSession( "https://" & RemoteComputer )
If objSession is Nothing Then
    WScript.Echo "Failed to create WSMAN Session object"
    WScript.Quit
End If 


strResourceUri = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/" _ 
    & "Win32_Service?Name=winmgmt"


On Error Resume Next
xmlResource = objSession.Get( strResourceUri )
WScript.Echo "Response message: " & Chr(10) & xmlResource
If Err.Number <> 0 Then
    DisplayErrorInfo
End If
On Error Goto 0

Sub DisplayErrorInfo()
    WScript.Echo "An error has occurred."     
    WScript.Echo
    WScript.Echo "Error Info"
    WScript.Echo "-----------"
    WScript.Echo "Number      : 0x" & hex(Err.number)
    WScript.Echo "Description : " & Err.Description
    WScript.Echo "Source      : " & Err.Source
    WScript.Echo "HelpFile    : " & Err.helpfile
    WScript.Echo "HelpContext : " & Err.HelpContext    
    WScript.Echo Err.Clear    
End Sub
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                 |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                           |
| Header<br/>                   | <dl> <dt>Всмандисп. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Всмандисп. idl</dt> </dl> |
| Библиотека<br/>                  | <dl> <dt>Всмандисп. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Session**](session.md)
</dt> </dl>

 

