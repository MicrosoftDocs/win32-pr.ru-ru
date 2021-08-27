---
description: IShellDispatch2. Сервицестарт-метод — запускает именованную службу.
ms.assetid: 3af57cdc-f449-433d-a9e1-119038045e4c
title: IShellDispatch2. Сервицестарт, метод (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch2.ServiceStart
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: f48d13e593898b7b4f91fc9246745b183b928ffaa0a799100990a327a3f670ba
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120090344"
---
# <a name="ishelldispatch2servicestart-method"></a>IShellDispatch2. Сервицестарт, метод

Запускает именованную службу.

## <a name="syntax"></a>Синтаксис


```JScript
retVal = IShellDispatch2.ServiceStart(
  sServiceName,
  vPersistent
)
```


```VB

IShellDispatch2.ServiceStart( _
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

Задайте значение **true** , чтобы служба автоматически запускалась диспетчером управления службами во время запуска системы. Задайте значение **false** , чтобы оставить конфигурацию службы без изменений.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

### <a name="jscript"></a>Язык JScript

Тип: **Variant \***

Возвращает **значение true** в случае успешного выполнения. в противном случае — **значение false**.

### <a name="vb"></a>VB

Тип: **Variant \***

Возвращает **значение true** в случае успешного выполнения. в противном случае — **значение false**.

## <a name="remarks"></a>Remarks

Этот метод реализован и доступен через метод [**Shell. сервицестарт**](./shell-servicestart.md) .

Метод возвращает **значение false** , если служба уже запущена. Перед вызовом этого метода можно вызвать [**Shell. иссервицеруннинг**](./shell-isservicerunning.md) для определения состояния службы.

Этот метод в настоящее время недоступен в Microsoft Visual Basic.

## <a name="examples"></a>Примеры

В следующих примерах показано использование **сервицестарт** для запуска службы сообщений. для JScript и VBScript отображается использование.

JScript:


```JScript
<script language="JScript">
    function fnServiceStartJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var bReturn;
        
        bReturn = objShell.ServiceStart("Messenger", true);
    }
</script>
```



Сценариев


```VB
<script language="VBScript">
    function fnServiceStartVB()
        dim objShell
        dim bReturn

        set objShell = CreateObject("shell.application")

        bReturn = objShell.ServiceStart("Messenger", true)

        set objShell = nothing
    end function
</script>
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional, только для \[ настольных приложений Windows XP\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                                          |
| Header<br/>                   | <dl> <dt>Шлдисп. h</dt> </dl>                          |
| IDL<br/>                      | <dl> <dt>Шлдисп. idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (версия 5,0 или более поздняя)</dt> </dl> |



 

 
