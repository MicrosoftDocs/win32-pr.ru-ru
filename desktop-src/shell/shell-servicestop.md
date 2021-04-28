---
description: Shell. Сервицестоп метод — останавливает именованную службу.
ms.assetid: AC22C91E-BBC6-4a2e-8D39-F9D7C0AC0947
title: Метод Shell. Сервицестоп (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.ServiceStop
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 5307fabe79ab9e634ca1e2815c0b90d59b13b1f6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108104162"
---
# <a name="shellservicestop-method"></a>Shell. Сервицестоп, метод

Останавливает именованную службу.

## <a name="syntax"></a>Синтаксис


```JScript
retVal = Shell.ServiceStop(
  sServiceName,
  vPersistent
)
```


```VB

Shell.ServiceStop( _
  ByVal sServiceName As BSTR, _
  ByVal vPersistent As Variant _
) As Variant
```





## <a name="parameters"></a>Параметры

<dl> <dt>

*ссервиценаме* \[ окне\]
</dt> <dd>

Тип: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

**Строка** , содержащая имя службы.

</dd> <dt>

*вперсистент* \[ окне\]
</dt> <dd>

Тип: **Variant**

Задайте значение **true** , чтобы служба была запущена диспетчером управления службами при вызове [**сервицестарт**](./shell-servicestart.md) . Чтобы оставить конфигурацию службы без изменений, установите для *вперсистент* значение **false**.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

### <a name="jscript"></a>Язык JScript

Тип: **Variant \***

Возвращает **значение true** в случае успешного выполнения. в противном случае — **значение false**.

### <a name="vb"></a>VB

Тип: **Variant \***

Возвращает **значение true** в случае успешного выполнения. в противном случае — **значение false**.

## <a name="remarks"></a>Remarks

Метод возвращает **значение false** , если служба уже остановлена. Перед вызовом этого метода можно вызвать [**Shell. иссервицеруннинг**](./shell-isservicerunning.md) для определения состояния службы.

Этот метод в настоящее время недоступен в Microsoft Visual Basic.

## <a name="examples"></a>Примеры

В следующих примерах показано использование **сервицестоп** для завершения работы службы сообщений. Для JScript и VBScript отображается использование.

Присутствовал


```JScript
<script language="JScript">
    function fnServiceStopJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var bReturn;
        
        bReturn = objShell.ServiceStop("Messenger", true);
    }
</script>
```



Сценариев


```VB
<script language="VBScript">
    function fnServiceStopVB()
        dim objShell
        dim bReturn

        set objShell = CreateObject("shell.application")

        bReturn = objShell.ServiceStop("Messenger", true)

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



 

 
