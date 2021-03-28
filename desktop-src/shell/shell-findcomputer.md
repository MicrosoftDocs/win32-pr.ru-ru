---
description: 'Отображает диалоговое окно Результаты поиска: компьютеры. В диалоговом окне отображается результат поиска указанного компьютера.'
ms.assetid: 0304b955-afde-4de4-824a-9ec9c9530360
title: Метод Shell. Финдкомпутер (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.FindComputer
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 3824eeb98bfac11e007d1bf7dd9f89153a7b73ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985981"
---
# <a name="shellfindcomputer-method"></a>Shell. Финдкомпутер, метод

Отображает диалоговое окно **Результаты поиска: компьютеры** . В диалоговом окне отображается результат поиска указанного компьютера.

## <a name="syntax"></a>Синтаксис


```JScript
Shell.FindComputer()
```


```VB

Shell.FindComputer()
```





## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

### <a name="jscript"></a>Язык JScript

Этот метод не возвращает значение.

### <a name="vb"></a>VB

Этот метод не возвращает значение.

## <a name="examples"></a>Примеры

В следующем примере показано использование **финдкомпутер** . Результат этого кода аналогичен нажатию кнопки " **Пуск** ", нажатия кнопки " **Поиск**", " **Принтеры", "компьютеры" или "люди** ", а затем выбора **компьютера в сети**. Правильное использование показано в JScript, VBScript и Visual Basic.

Присутствовал


```JScript
<script language="JScript">
    function fnShellFindComputerJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.FindComputer();
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
        objShell.FindComputer

        set objShell = nothing
    end function
 </script>
```



Visual Basic:


```VB
Private Sub fnShellFindComputerVB()
    Dim objShell As Shell

    Set objShell = New Shell
    objShell.FindComputer

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



 

 




