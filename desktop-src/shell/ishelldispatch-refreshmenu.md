---
description: сведения о методе ишеллдиспатч. рефрешмену, который обновляет содержимое меню. используется только с системами, предшествующими Windows XP.
ms.assetid: D36FA5A0-AF03-4627-86E0-869BF1440958
title: Ишеллдиспатч. Рефрешмену, метод (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.RefreshMenu
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: ac5bb37f5880011fcabcfcc0e923196857694012a547b0391326a9fe5d8424f0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118969063"
---
# <a name="ishelldispatchrefreshmenu-method"></a>Ишеллдиспатч. Рефрешмену, метод

Обновляет содержимое меню " **Пуск** ". используется только с системами, предшествующими Windows XP.

## <a name="syntax"></a>Синтаксис


```JScript
IShellDispatch.RefreshMenu()
```


```VB

IShellDispatch.RefreshMenu()
```





## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

### <a name="jscript"></a>Язык JScript

Этот метод не возвращает значение.

### <a name="vb"></a>VB

Этот метод не возвращает значение.

## <a name="remarks"></a>Remarks

Этот метод реализован и доступен через метод [**Shell. трайпропертиес**](shell-trayproperties.md) .

функциональные возможности, предоставляемые **рефрешмену** , автоматически обрабатываются в Windows XP и более поздних версиях. не вызывайте этот метод в Windows XP или более поздней версии.

## <a name="examples"></a>Примеры

в следующих примерах показано использование **рефрешмену** в JScript, VBScript и Visual Basic.

JScript:


```JScript
<script language="JScript">
    function fnShellRefreshMenuJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.RefreshMenu();
    }
</script>
```



Сценариев


```VB
<script language="VBScript">
    function fnShellRefreshMenuVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objshell.RefreshMenu

        set objShell = nothing
    end function
 </script>
```



Visual Basic:


```VB
Private Sub fnShellRefreshMenuVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objshell.RefreshMenu

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



 

 




