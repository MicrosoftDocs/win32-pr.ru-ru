---
description: IShellDispatch2. Иссервицеруннинг, метод возвращает значение, указывающее, запущена ли определенная служба.
ms.assetid: 91f3fba1-7aa5-423a-bc37-49db230c79db
title: IShellDispatch2. Иссервицеруннинг, метод (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch2.IsServiceRunning
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: e8ad792f1669a8ebcfa411c58b34da214ccf69a7
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117092"
---
# <a name="ishelldispatch2isservicerunning-method"></a>IShellDispatch2. Иссервицеруннинг, метод

Возвращает значение, указывающее, запущена ли определенная служба.

## <a name="syntax"></a>Синтаксис


```JScript
retVal = IShellDispatch2.IsServiceRunning(
  sServiceName
)
```


```VB

IShellDispatch2.IsServiceRunning( _
  ByVal sServiceName As BSTR _
) As Variant
```





## <a name="parameters"></a>Параметры

<dl> <dt>

*ссервиценаме* \[ окне\]
</dt> <dd>

Тип: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

**Строка** , содержащая имя службы.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

### <a name="jscript"></a>Язык JScript

Тип: **Variant \***

Возвращает **значение true** , если служба, указанная параметром *ссервиценаме* , запущена. в противном случае — **значение false**.

### <a name="vb"></a>VB

Тип: **Variant \***

Возвращает **значение true** , если служба, указанная параметром *ссервиценаме* , запущена. в противном случае — **значение false**.

## <a name="remarks"></a>Remarks

Этот метод реализован и доступен через метод [**Shell. иссервицеруннинг**](./shell-isservicerunning.md) .

Этот метод в настоящее время недоступен в Microsoft Visual Basic.

## <a name="examples"></a>Примеры

В следующих примерах показано использование **иссервицеруннинг** для определения того, запущена ли служба "темы" для приложения. Для JScript и VBScript отображается использование.

Присутствовал


```JScript
<script language="JScript">
    function fnIsServiceRunningJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var bReturn;
    
        bReturn = objShell.IsServiceRunning("Themes");
    }
</script>
```



Сценариев


```VB
<script language="VBScript">
    function fnIsServiceRunningVB()
        dim objShell
        dim bReturn
    
        set objShell = CreateObject("shell.application")
    
        bReturn = objShell.IsServiceRunning("Themes")
    
        set objShell = nothing
    end function
</script>
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional, только для \[ классических приложений Windows XP\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                                          |
| Header<br/>                   | <dl> <dt>Шлдисп. h</dt> </dl>                          |
| IDL<br/>                      | <dl> <dt>Шлдисп. idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (версия 5,0 или более поздняя)</dt> </dl> |



 

 
