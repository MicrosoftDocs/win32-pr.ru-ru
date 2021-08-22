---
description: Свертывает все окна на рабочем столе. этот метод действует аналогично щелчку правой кнопкой мыши панели задач и выбора пункта свернуть все Windows в старых системах или щелчка значка свернуть рабочий стол на панели задач.
ms.assetid: 25DD56B0-221E-44a2-9FAD-FB358ADD7FF1
title: Ишеллдиспатч. Минимизеалл, метод (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.MinimizeAll
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 18f1256f93c9cd18d0c904f090716641b466e91319dbef323ee5107b802f82ff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118452989"
---
# <a name="ishelldispatchminimizeall-method"></a>Ишеллдиспатч. Минимизеалл, метод

Свертывает все окна на рабочем столе. этот метод действует аналогично щелчку правой кнопкой мыши панели задач и выбора пункта **свернуть все Windows** в старых системах или щелчка значка свернуть **рабочий стол** на панели задач.

## <a name="syntax"></a>Синтаксис


```JScript
IShellDispatch.MinimizeAll()
```


```VB

IShellDispatch.MinimizeAll()
```





## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

### <a name="jscript"></a>Язык JScript

Этот метод не возвращает значение.

### <a name="vb"></a>VB

Этот метод не возвращает значение.

## <a name="remarks"></a>Remarks

Этот метод реализован и доступен через метод [**Shell. минимизеалл**](shell-minimizeall.md) .

## <a name="examples"></a>Примеры

в следующих примерах показано использование **минимизеалл** для JScript, VBScript и Visual Basic.

JScript:


```JScript
<script language="JScript">
    function fnShellMinimizeAllJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.MinimizeAll();
    }
</script>
```



Сценариев


```VB
<script language="VBScript">
    function fnShellMinimizeAllVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objshell.MinimizeAll

        set objShell = nothing
    end function
 </script>
```



Visual Basic:


```VB
Private Sub fnShellMinimizeAllVB()
    Dim objShell As Shell

    Set objShell = New Shell
    objshell.MinimizeAll

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional, только для \[ настольных приложений Windows XP\]<br/>                                         |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                           |
| Заголовок<br/>                   | <dl> <dt>Шлдисп. h</dt> </dl>                           |
| IDL<br/>                      | <dl> <dt>Шлдисп. idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (версия 4,71 или более поздняя)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ишеллдиспатч**](ishelldispatch.md)
</dt> <dt>

[**ундоминимизеалл**](shell-undominimizeall.md)
</dt> </dl>

 

 




