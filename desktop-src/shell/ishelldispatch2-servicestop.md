---
description: IShellDispatch2. Сервицестоп, метод — останавливает именованную службу.
ms.assetid: f4cd0e2c-4ecc-4e9f-a0b5-d2a8a739f0e2
title: IShellDispatch2. Сервицестоп, метод (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch2.ServiceStop
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 71bc0502d45e4092decfe1b712ed11f75a02bf50d112436ad1d21f9e02c17e72
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118221029"
---
# <a name="ishelldispatch2servicestop-method"></a>IShellDispatch2. Сервицестоп, метод

Останавливает именованную службу.

## <a name="syntax"></a>Синтаксис


```JScript
retVal = IShellDispatch2.ServiceStop(
  sServiceName,
  vPersistent
)
```


```VB

IShellDispatch2.ServiceStop( _
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

Задайте значение **true** , чтобы служба была запущена диспетчером управления службами при вызове [**сервицестарт**](ishelldispatch2-servicestart.md) . Чтобы оставить конфигурацию службы без изменений, установите для *вперсистент* значение **false**.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

### <a name="jscript"></a>Язык JScript

Тип: **Variant \***

Возвращает **значение true** в случае успешного выполнения. в противном случае — **значение false**.

### <a name="vb"></a>VB

Тип: **Variant \***

Возвращает **значение true** в случае успешного выполнения. в противном случае — **значение false**.

## <a name="remarks"></a>Remarks

Этот метод реализован и доступен через метод [**Shell. сервицестоп**](./shell-servicestop.md) .

Метод возвращает **значение false** , если служба уже остановлена. Перед вызовом этого метода можно вызвать [**Shell. иссервицеруннинг**](./shell-isservicerunning.md) для определения состояния службы.

Этот метод в настоящее время недоступен в Microsoft Visual Basic.

## <a name="examples"></a>Примеры

В следующих примерах показано использование **сервицестоп** для завершения работы службы сообщений. для JScript и VBScript отображается использование.

JScript:


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



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional, только для \[ настольных приложений Windows XP\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                                          |
| Header<br/>                   | <dl> <dt>Шлдисп. h</dt> </dl>                          |
| IDL<br/>                      | <dl> <dt>Шлдисп. idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (версия 5,0 или более поздняя)</dt> </dl> |



 

 
