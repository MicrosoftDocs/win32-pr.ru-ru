---
description: Shell. Канстартстопсервице — определяет, может ли текущий пользователь запускать и прекращать работу именованной службы.
ms.assetid: 1428F529-61F6-4113-A553-2C0D617FD859
title: Метод Shell. Канстартстопсервице (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.CanStartStopService
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 29561519b95329093ef1f7bfc64023fd1ac4533d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108083692"
---
# <a name="shellcanstartstopservice-method"></a>Shell. Канстартстопсервице, метод

Определяет, может ли текущий пользователь запускать и прекращать работу именованной службы.

## <a name="syntax"></a>Синтаксис


```JScript
retVal = Shell.CanStartStopService(
  sServiceName
)
```


```VB

Shell.CanStartStopService( _
  ByVal sServiceName As String _
) As Variant
```





## <a name="parameters"></a>Параметры

<dl> <dt>

*ссервиценаме* \[ окне\]
</dt> <dd>

Тип: **строка**

**Строка** , содержащая имя службы.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

### <a name="jscript"></a>Язык JScript

Тип: **Variant \***

Возвращает **значение true** , если пользователь может запускать и прекращать работу службы. в противном случае — **значение false**.

### <a name="vb"></a>VB

Тип: **Variant \***

Возвращает **значение true** , если пользователь может запускать и прекращать работу службы. в противном случае — **значение false**.

## <a name="remarks"></a>Remarks

Этот метод в настоящее время недоступен в Microsoft Visual Basic.

## <a name="examples"></a>Примеры

В следующих примерах показано использование **канстартстопсервице** для JScript и VBScript.

Присутствовал


```JScript
<script language="JScript">
    function fnCanStartStopServiceJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var bReturn;

        bReturn = objShell.CanStartStopService("service name");
    }
</script>
```



Сценариев


```VB
<script language="VBScript">
    function fnCanStartStopServiceVB()
        dim objShell
        dim bReturn

        set objShell = CreateObject("shell.application")

        bReturn = objShell.CanStartStopService("service name")

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



 

 




