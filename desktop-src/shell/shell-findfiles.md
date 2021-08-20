---
description: 'Отображает диалоговое окно Поиск: все файлы. это то же самое, что щелчок меню, а затем выбор поиска (или его эквивалент в системах, предшествующих Windows XP.'
ms.assetid: cccdd3ea-b52a-4fbe-b4c5-1efc1dd6d770
title: Метод Shell. Финдфилес (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.FindFiles
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 8c7295857509c19b06bed342508e0f0c5ee5aae42136edbe6035c6e256cdfb2f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118968583"
---
# <a name="shellfindfiles-method"></a>Shell. Финдфилес, метод

Отображает диалоговое окно **Поиск: все файлы** . это то же самое, что и при нажатии кнопки " **пуск** ", а затем выборе **поиска** (или его эквивалента в системах, предшествующих Windows XP.

## <a name="syntax"></a>Синтаксис


```JScript
Shell.FindFiles()
```


```VB

Shell.FindFiles()
```





## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

### <a name="jscript"></a>Язык JScript

Этот метод не возвращает значение.

### <a name="vb"></a>VB

Этот метод не возвращает значение.

## <a name="examples"></a>Примеры

В следующем примере показано использование **финдфилес** . правильное использование отображается для JScript, VBScript и Visual Basic.

JScript:


```JScript
<script language="JScript">
    function fnShellFindFilesJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.Shell_FindFiles();
    }
</script>
```



Сценариев


```VB
<script language="VBScript">
    function fnShellFindFilesVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objShell.FindFiles

        set objShell = nothing
    end function
 </script>
```



Visual Basic:


```VB
Private Sub fnShellFindFilesVB()
    Dim objShell As Shell

    Set objShell = New Shell
    objShell.FindFiles

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



 

 




