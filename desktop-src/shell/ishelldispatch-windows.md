---
description: Ишеллдиспатч. метод Windows — создает и возвращает объект шеллвиндовс. Этот объект представляет коллекцию всех открытых окон, принадлежащих оболочке.
ms.assetid: 788E2106-3534-4e22-801F-677FD02BDFE0
title: Ишеллдиспатч. метод Windows (шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.Windows
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: f17e6f9ff4a8118043cf452af0647b78c7d2c4365f83a497481ee97236edb21c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118221639"
---
# <a name="ishelldispatchwindows-method"></a>Ишеллдиспатч. метод Windows

Создает и возвращает объект [**шеллвиндовс**](shellwindows.md) . Этот объект представляет коллекцию всех открытых окон, принадлежащих оболочке.

## <a name="syntax"></a>Синтаксис


```JScript
retVal = IShellDispatch.Windows()
```


```VB

IShellDispatch.Windows() As IDispatch
```





## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

### <a name="jscript"></a>Язык JScript

Тип: **[ **IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)\*\***

Ссылка на объект [**шеллвиндовс**](shellwindows.md) .

### <a name="vb"></a>VB

Тип: **[ **IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)\*\***

Ссылка на объект [**шеллвиндовс**](shellwindows.md) .

## <a name="remarks"></a>Remarks

этот метод реализован и доступен через метод [**Shell. Windows**](shell-windows.md) .

## <a name="examples"></a>Примеры

в следующих примерах используется **Windows** для получения объекта [**шеллвиндовс**](shellwindows.md) и отображается количество содержащихся в нем элементов. сведения об использовании отображаются для JScript, VBScript и Visual Basic.

JScript:


```JScript
<script language="JScript">
    function fnShellWindowsJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objShellWindows;
        
        objShellWindows = objshell.Windows();

        if (objShellWindows != null)
        {
            alert(objShellWindows.Count);
        }
    }
</script>
```



Сценариев


```VB
<script language="VBScript">
    function fnShellWindowsVB()
        dim objShell
        dim objShellWindows
        
        set objShell = CreateObject("shell.application")
        set objShellWindows = objshell.Windows

        if (not objShellWindows is nothing) then
            alert(objShellWindows.Count)
        end if

        set objShellWindows = nothing
        set objShell = nothing
    end function
 </script>
```



Visual Basic:


```VB
Private Sub fnShellWindowsVB()
    Dim objShell        As Shell
    Dim objShellWindows As ShellWindows
    
    Set objShell = New Shell
    Set objShellWindows = objshell.Windows

    If (Not objShellWindows Is Nothing) Then
        Debug.Print objShellWindows.Count
    End If

    Set objShellWindows = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional, только для \[ настольных приложений Windows XP\]<br/>                                         |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                           |
| Заголовок<br/>                   | <dl> <dt>Шлдисп. h</dt> </dl>                           |
| IDL<br/>                      | <dl> <dt>Шлдисп. idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (версия 4,71 или более поздняя)</dt> </dl> |



 

 
