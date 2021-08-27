---
description: IShellDispatch4. експлорерполици, метод возвращает значение для указанной Windows политики Internet Explorer.
ms.assetid: 490c3e18-b606-456a-9016-dc4f7bad2bc3
title: IShellDispatch4. Експлорерполици, метод (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch4.ExplorerPolicy
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 16187fedde4a454ffaa5415ade08e61f5d0abca145caa7b5c8e29fa9f3b00cdd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120111504"
---
# <a name="ishelldispatch4explorerpolicy-method"></a>IShellDispatch4. Експлорерполици, метод

возвращает значение для указанной Windows политики Internet Explorer.

## <a name="syntax"></a>Синтаксис


```JScript
retVal = IShellDispatch4.ExplorerPolicy(
  bstrPolicyName
)
```


```VB

IShellDispatch4.ExplorerPolicy( _
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
        
        vReturn = objshell.ExplorerPolicy("ValueName");
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
            vReturn = objshell.ExplorerPolicy("ValueName")
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
        vReturn = objshell.ExplorerPolicy("ValueName")
        Debug.Print vReturn
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения XP\]<br/>                                                                   |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                                          |
| Заголовок<br/>                   | <dl> <dt>Шлдисп. h</dt> </dl>                          |
| IDL<br/>                      | <dl> <dt>Шлдисп. idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (версия 6,0 или более поздняя)</dt> </dl> |



 

 
