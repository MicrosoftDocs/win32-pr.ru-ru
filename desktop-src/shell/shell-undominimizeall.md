---
description: Восстанавливает все настольные компьютеры в том же состоянии, в котором они находились до последней команды Минимизеалл.
ms.assetid: dcedfa18-6dde-4fb8-9679-4d6ff80249e4
title: Метод Shell. Ундоминимизеалл (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.UndoMinimizeALL
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 5e2342bda1059e2bcb00893afb182e415840a4e650392fc3e1d3df4756cb2d03
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119941574"
---
# <a name="shellundominimizeall-method"></a>Shell. Ундоминимизеалл, метод

Восстанавливает все настольные компьютеры в том же состоянии, в котором они находились до последней команды [**минимизеалл**](shell-minimizeall.md) . этот метод действует аналогично щелчку правой кнопкой мыши панели задач и выбора команды **отменить свернуть все Windows** в старых системах или второй щелчок значка " **свернуть рабочий стол** " в области быстрого запуска на панели задач в Windows 2000 или Windows XP.

## <a name="syntax"></a>Синтаксис


```JScript
iRetVal = Shell.UndoMinimizeALL()
```


```VB

Shell.UndoMinimizeALL() As Integer
```





## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="examples"></a>Примеры

В следующем примере показано использование **ундоминимизеалл** . правильное использование отображается для JScript, VBScript и Visual Basic.

JScript:


```JScript
<script language="JScript">
    function fnShellUndoMinimizeALLJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.UndoMinimizeALL();
    }
</script>
```



Сценариев


```VB
<script language="VBScript">
    function fnShellUndoMinimizeALLVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objShell.UndoMinimizeALL

        set objShell = nothing
    end function
 </script>
```



Visual Basic:


```VB
Private Sub fnShellUndoMinimizeAllVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objShell.UndoMinimizeALL

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



 

 




