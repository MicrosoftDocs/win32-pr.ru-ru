---
description: 'Отображает диалоговое окно Поиск: все файлы. это то же самое, что и при щелчке меню и выборе поиска.'
ms.assetid: 6F588D5E-5B6E-4000-BAD5-B557FB975FCA
title: Ишеллдиспатч. Финдфилес, метод (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.FindFiles
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 6cc390ea0ff4ba328bd0061ed03d973bff9e32054713a793ebe29ef9be2650ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119942384"
---
# <a name="ishelldispatchfindfiles-method"></a>Ишеллдиспатч. Финдфилес, метод

Отображает диалоговое окно **Поиск: все файлы** . Это то же самое, что и при щелчке в меню **Пуск** , а затем выбрав **Поиск**.

## <a name="syntax"></a>Синтаксис


```JScript
IShellDispatch.FindFiles()
```


```VB

IShellDispatch.FindFiles()
```





## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

### <a name="jscript"></a>Язык JScript

Этот метод не возвращает значение.

### <a name="vb"></a>VB

Этот метод не возвращает значение.

## <a name="remarks"></a>Remarks

Этот метод реализован и доступен через метод [**Shell. финдфилес**](shell-findfiles.md) .

## <a name="examples"></a>Примеры

в следующих примерах показано использование **финдфилес** в JScript, VBScript и Visual Basic.

JScript:


```JScript
<script language="JScript">
    function fnShellFindFilesJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.FindFiles();
    }
</script>
```



Сценариев


```VB
<script language="VBScript">
   function fnShellFindFilesVB()
       dim objShell
       
       set objShell = CreateObject("shell.application")
       objshell.FindFiles

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



 

 




