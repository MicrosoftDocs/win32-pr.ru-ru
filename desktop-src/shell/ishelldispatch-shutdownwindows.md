---
description: ишеллдиспатч. шутдовнвиндовс-метод — отображает диалоговое окно завершение работы Windows. это то же самое, что и щелчок меню и выбор команды завершение работы.
ms.assetid: 3C4F6579-6398-4af4-8911-FE22555B0ABC
title: Ишеллдиспатч. Шутдовнвиндовс, метод (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.ShutdownWindows
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 2ba63602dd2603ea2bf4ff2b14346d640800a74082cd89e154ee98a0a0431bd3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119661214"
---
# <a name="ishelldispatchshutdownwindows-method"></a>Ишеллдиспатч. Шутдовнвиндовс, метод

отображает диалоговое окно **завершение работы Windows** . Это то же самое, что и при нажатии кнопки « **Пуск** », и при выборе « **Завершение работы**».

## <a name="syntax"></a>Синтаксис


```JScript
IShellDispatch.ShutdownWindows()
```


```VB

IShellDispatch.ShutdownWindows()
```





## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

### <a name="jscript"></a>Язык JScript

Этот метод не возвращает значение.

### <a name="vb"></a>VB

Этот метод не возвращает значение.

## <a name="remarks"></a>Remarks

Этот метод реализован и доступен через метод [**Shell. шутдовнвиндовс**](shell-shutdownwindows.md) .

## <a name="examples"></a>Примеры

в следующем примере показано использование **шутдовнвиндовс** в JScript, VBScript и Visual Basic.

JScript:


```JScript
<script language="JScript">
    function fnShellShutdownWindowsJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.ShutdownWindows();
    }
</script>
```



Сценариев


```VB
<script language="VBScript">
    function fnShellShutdownWindowsVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objshell.ShutdownWindows

        set objShell = nothing
    end function
 </script>
```



Visual Basic:


```VB
Private Sub fnShellShutdownWindowsVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objshell.ShutdownWindows

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



 

 




