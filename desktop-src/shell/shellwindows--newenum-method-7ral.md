---
description: Создает и возвращает новый объект Шеллвиндовс, являющийся копией этого объекта Шеллвиндовс.
title: Метод ShellWindows._NewEnum (Ексдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellWindows._NewEnum
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 85e84c13-62aa-4502-b642-ca55273a800d
ms.openlocfilehash: 696767844e2cc5dbe17aa44c2f76a8b0550b86115437e0d5f3e1f1f2543dbb2d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117857103"
---
# <a name="shellwindows_newenum-method"></a>Шеллвиндовс. \_ Метод NewEnum

Создает и возвращает новый объект [**шеллвиндовс**](shellwindows.md) , являющийся копией этого объекта **шеллвиндовс** .

## <a name="syntax"></a>Синтаксис


```JScript
retVal = ShellWindows._NewEnum()
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)\*\***

Ссылка на объект для копирования объекта [**шеллвиндовс**](shellwindows.md) .

## <a name="examples"></a>Примеры

В следующем примере показано использование **\_ NewEnum** . Для VBScript и Visual Basic отображается правильное использование. Этот метод не может использоваться с JScript.

Сценариев


```VB
<script language="VBScript">
    function fnShellWindowsNewEnumVB()
        dim objShell
        dim objShellWindows
        
        set objShell = CreateObject("shell.application")
        set objShellWindows = objshell.Shell_Windows

        if (not objShellWindows is nothing) then
            dim objEnumItems
            
            for each objEnumItems in objShellWindows
                alert(objEnumItems.Type)
            next
        end if

        set objShellWindows = nothing
        set objShell = nothing
    end function
 </script>
```



Visual Basic:


```VB
Private Sub fnShellWindowsNewEnumVB()
    Dim objShell        As Shell
    Dim objShellWindows As ShellWindows
    
    Set objShell = New Shell
    Set objShellWindows = objshell.Shell_Windows

    If (Not objShellWindows Is Nothing) Then
        Dim vEnumItem As Variant
        
        For Each vEnumItem In objShellWindows
            Debug.Print vEnumItem.Type
        Next vEnumItem
    End If

    Set objShellWindows = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional, только для \[ настольных приложений Windows XP\]<br/>                                         |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                           |
| Заголовок<br/>                   | <dl> <dt>Ексдисп. h</dt> </dl>                            |
| DLL<br/>                      | <dl> <dt>Shell32.dll (версия 4,71 или более поздняя)</dt> </dl> |



 

 
