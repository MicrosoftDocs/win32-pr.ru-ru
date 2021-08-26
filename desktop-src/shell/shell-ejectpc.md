---
description: Shell. Ежектпк метод — извлекает компьютер из стыковочного узла. это то же самое, что щелчок меню и выбор пункта извлечь компьютер, если компьютер поддерживает эту команду.
ms.assetid: eaba3dce-8fea-453f-90c2-4a9b5cb05ecc
title: Метод Shell. Ежектпк (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.EjectPC
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 3f774b666647ebf8a255950fe8427a87e55ca514db9ed841a5fc7f2e7edb2e69
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119883884"
---
# <a name="shellejectpc-method"></a>Shell. Ежектпк, метод

Извлекает компьютер из стыковочного узла. Это то же самое, что и при нажатии кнопки " **Пуск** " и выборе пункта " **извлечь компьютер**", если компьютер поддерживает эту команду.

## <a name="syntax"></a>Синтаксис


```JScript
Shell.EjectPC()
```


```VB

Shell.EjectPC()
```





## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

### <a name="jscript"></a>Язык JScript

Этот метод не возвращает значение.

### <a name="vb"></a>VB

Этот метод не возвращает значение.

## <a name="examples"></a>Примеры

В следующем примере показано использование **ежектпк** . правильное использование отображается для JScript, VBScript и Visual Basic.

JScript:


```JScript
<script language="JScript">
    function fnShellEjectPCJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.EjectPC();
    }
</script>
```



Сценариев


```VB
<script language="VBScript">
    function fnShellEjectPCVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objShell.EjectPC

        set objShell = nothing
    end function
 </script>
```



Visual Basic:


```VB
Private Sub fnShellEjectPCVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objShell.EjectPC

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



 

 




