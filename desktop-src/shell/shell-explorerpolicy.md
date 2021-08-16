---
description: Shell. експлорерполици — получает значение для указанного Windows политики Internet Explorer.
ms.assetid: 47E17F6A-ED43-44cd-AF77-A6E49865E1B5
title: Метод Shell. Експлорерполици (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.ExplorerPolicy
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 78a0e601e8093358ef05f259586726e840982d1a97d428b8453f26ecb878a4c6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117857936"
---
# <a name="shellexplorerpolicy-method"></a>Shell. Експлорерполици, метод

возвращает значение для указанной Windows политики Internet Explorer.

## <a name="syntax"></a>Синтаксис


```JScript
retVal = Shell.ExplorerPolicy(
  bstrPolicyName
)
```


```VB

Shell.ExplorerPolicy( _
  ByVal bstrPolicyName As BSTR _
) As Variant
```





## <a name="parameters"></a>Параметры

<dl> <dt>

*бстрполицинаме* \[ окне\]
</dt> <dd>

Тип: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

**Строка** , указывающая имя политики.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

### <a name="jscript"></a>Язык JScript

Тип: **Variant \***

Значение, связанное с указанным именем политики.

### <a name="vb"></a>VB

Тип: **Variant \***

Значение, связанное с указанным именем политики.

## <a name="remarks"></a>Remarks

Сетевые администраторы могут управлять вычислительной средой пользователей и управлять ею, настроив политики.

указанное имя значения должно находиться в разделе реестра **HKEY \_ CURRENT \_ USER** \\ **Software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **политики** \\ **обозревателя** . Если имя параметра не существует, метод возвращает **значение NULL**.

## <a name="examples"></a>Примеры

в следующих примерах показано правильное использование **експлорерполици** для JScript, VBScript и Visual Basic.

JScript:


```JScript
<script language="JScript">
    function fnIShellDispatch4ExplorerPolicyJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var vReturn;
        
        vReturn = objShell.ExplorerPolicy("ValueName");
        alert(vReturn);
    }
</script>
```



Сценариев


```VB
<script language="VBScript">
     function fnIShellDispatch4ExplorerPolicyVB()
        dim objShell
        dim vReturn
        
        set objShell = CreateObject("shell.application")
            vReturn = objShell.ExplorerPolicy("ValueName")
            alert(vReturn)
        set objShell = nothing
    end function
 </script>
```



Visual Basic:


```VB
Private Sub fnIShellDispatch4ExplorerPolicyVB()
    Dim objShell As Shell
    Dim vReturn  As Variant
    
    Set objShell = New Shell
        vReturn = objShell.ExplorerPolicy("ValueName")
        Debug.Print vReturn
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения XP\]<br/>                                                                   |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                                          |
| Header<br/>                   | <dl> <dt>Шлдисп. h</dt> </dl>                          |
| IDL<br/>                      | <dl> <dt>Шлдисп. idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (версия 6,0 или более поздняя)</dt> </dl> |



 

 
