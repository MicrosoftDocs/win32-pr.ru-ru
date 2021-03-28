---
description: 'Отображает диалоговое окно Результаты поиска: компьютеры. В диалоговом окне отображается результат поиска указанного компьютера.'
ms.assetid: 9B687A8A-BB29-49a0-8AE3-11A75FAF3257
title: Ишеллдиспатч. Финдкомпутер, метод (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.FindComputer
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 3ad928b6860a85126a714a08f3bc3df9d4aff67c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984716"
---
# <a name="ishelldispatchfindcomputer-method"></a>Ишеллдиспатч. Финдкомпутер, метод

Отображает диалоговое окно **Результаты поиска: компьютеры** . В диалоговом окне отображается результат поиска указанного компьютера.

## <a name="syntax"></a>Синтаксис


```JScript
IShellDispatch.FindComputer()
```


```VB

IShellDispatch.FindComputer()
```





## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

### <a name="jscript"></a>Язык JScript

Этот метод не возвращает значение.

### <a name="vb"></a>VB

Этот метод не возвращает значение.

## <a name="remarks"></a>Примечания

Этот метод реализован и доступен через метод [**Shell. финдкомпутер**](shell-findcomputer.md) .

## <a name="examples"></a>Примеры

В следующих примерах показано использование **финдкомпутер** в JScript, VBScript и Visual Basic.

Присутствовал


```JScript
<script language="JScript">
    function fnShellFindComputerJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.FindComputer();
    }
</script>
```



Сценариев


```VB
 <script language="VBScript">
    function fnShellFindComputerVB()
        dim objShell
        dim ssfWINDOWS
        ssfWINDOWS = 36

        set objShell = CreateObject("shell.application")
        objshell.FindComputer

        set objShell = nothing
    end function
 </script>
```



Visual Basic:


```VB
Private Sub fnShellFindComputerVB()
    Dim objShell As Shell

    Set objShell = New Shell
    objshell.FindComputer

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional, только для \[ классических приложений Windows XP\]<br/>                                         |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                           |
| Заголовок<br/>                   | <dl> <dt>Шлдисп. h</dt> </dl>                           |
| IDL<br/>                      | <dl> <dt>Шлдисп. idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (версия 4,71 или более поздняя)</dt> </dl> |



 

 




