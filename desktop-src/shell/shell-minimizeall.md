---
description: Свертывает все окна на рабочем столе.
ms.assetid: 3af98a16-27d1-4c93-ac72-7c9e24e68c23
title: Метод Shell. Минимизеалл (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.MinimizeAll
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 55b615cfed8813f5567b13d58648fef36aaedda3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985972"
---
# <a name="shellminimizeall-method"></a>Shell. Минимизеалл, метод

Свертывает все окна на рабочем столе. Этот метод действует аналогично щелчку правой кнопкой мыши панели задач и выбора пункта **Свернуть все окна** в старых системах или нажатия значка **Показывать Рабочий стол** в области Быстрый запуск панели задач в Windows 2000 или Windows XP.

## <a name="syntax"></a>Синтаксис


```JScript
iRetVal = Shell.MinimizeAll()
```


```VB

Shell.MinimizeAll() As Integer
```





## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="examples"></a>Примеры

В следующем примере показано использование **минимизеалл** . Правильное использование показано в JScript, VBScript и Visual Basic.

Присутствовал


```JScript
<script language="JScript">
    function fnShellMinimizeAllJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.MinimizeAll();
    }
</script>
```



Сценариев


```VB
<script language="VBScript">
    function fnShellMinimizeAllVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objShell.MinimizeAll

        set objShell = nothing
    end function
 </script>
```



Visual Basic:


```VB
Private Sub fnShellMinimizeAllVB()
    Dim objShell As Shell

    Set objShell = New Shell
    objShell.MinimizeAll

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



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Shell**](shell.md)
</dt> <dt>

[**ундоминимизеалл**](shell-undominimizeall.md)
</dt> </dl>

 

 




