---
description: Располагает все окна на рабочем столе по вертикали. Этот метод оказывает тот же результат, что и щелчок правой кнопкой мыши панели задач и выбора параметра Показывать окна рядом.
ms.assetid: 63CB7E20-48E6-4cfe-B0BA-0D28A7B151BD
title: Ишеллдиспатч. Тилевертикалли, метод (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.TileVertically
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 42f98ae99814495029c67d41b05e86182c6b8b34
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984700"
---
# <a name="ishelldispatchtilevertically-method"></a>Ишеллдиспатч. Тилевертикалли, метод

Располагает все окна на рабочем столе по вертикали. Этот метод оказывает тот же результат, что и щелчок правой кнопкой мыши панели задач и выбора параметра **Показывать окна рядом**.

## <a name="syntax"></a>Синтаксис


```JScript
IShellDispatch.TileVertically()
```


```VB

IShellDispatch.TileVertically()
```





## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

### <a name="jscript"></a>Язык JScript

Этот метод не возвращает значение.

### <a name="vb"></a>VB

Этот метод не возвращает значение.

## <a name="remarks"></a>Примечания

Этот метод реализован и доступен через метод [**Shell. тилевертикалли**](shell-tilevertically.md) .

## <a name="examples"></a>Примеры

В следующих примерах показано использование **тилевертикалли** в JScript, VBScript и Visual Basic.

Присутствовал


```JScript
<script language="JScript">
    function fnShellTileVerticallyJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.TileVertically();
    }
</script>
```



Сценариев


```VB
<script language="VBScript">
    function fnShellTileVerticallyVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objshell.TileVertically

        set objShell = nothing
    end function
 </script>
```



Visual Basic:


```VB
Private Sub fnShellTileVerticallyVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objshell.TileVertically

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



 

 




