---
description: Мозаичное отображение всех окон на рабочем столе по горизонтали. Этот метод действует так же, как и щелчок правой кнопкой мыши панели задач и выбора пункта Показывать окна с накоплением.
ms.assetid: 85785510-6B75-450a-A9BB-6C3B4F6194E2
title: Ишеллдиспатч. Тилехоризонталли, метод (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.TileHorizontally
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 06491f797de4a9fcb5c431d85cff71fbc78d605c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154938"
---
# <a name="ishelldispatchtilehorizontally-method"></a>Ишеллдиспатч. Тилехоризонталли, метод

Мозаичное отображение всех окон на рабочем столе по горизонтали. Этот метод действует так же, как и щелчок правой кнопкой мыши панели задач и выбора пункта **Показывать окна с накоплением**.

## <a name="syntax"></a>Синтаксис


```JScript
IShellDispatch.TileHorizontally()
```


```VB

IShellDispatch.TileHorizontally()
```





## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

### <a name="jscript"></a>Язык JScript

Этот метод не возвращает значение.

### <a name="vb"></a>VB

Этот метод не возвращает значение.

## <a name="remarks"></a>Примечания

Этот метод реализован и доступен через метод [**Shell. тилехоризонталли**](shell-tilehorizontally.md) .

## <a name="examples"></a>Примеры

В следующем примере показано использование **тилехоризонталли** в JScript, VBScript и Visual Basic.

Присутствовал


```JScript
<script language="JScript">
    function fnShellTileHorizontallyJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.TileHorizontally();
    }
</script>
```



Сценариев


```VB
<script language="VBScript">
    function fnShellTileHorizontallyVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objshell.TileHorizontally

        set objShell = nothing
    end function
 </script>
```



Visual Basic:


```VB
Private Sub fnShellTileHorizontallyVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objshell.TileHorizontally

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



 

 




