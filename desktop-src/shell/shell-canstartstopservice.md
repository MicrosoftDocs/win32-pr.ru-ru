---
description: Определяет, может ли текущий пользователь запускать и прекращать работу именованной службы.
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
ms.openlocfilehash: 1d92fa076141bdebc8a2f24059a65e842e5a3d6c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103998754"
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

Тип: **Variant \** _

Возвращает *значение _ true**, если пользователь может запускать и прекращать работу службы. в противном случае — **значение false**.

### <a name="vb"></a>VB

Тип: **Variant \** _

Возвращает *значение _ true**, если пользователь может запускать и прекращать работу службы. в противном случае — **значение false**.

## <a name="remarks"></a>Примечания

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



 

 




