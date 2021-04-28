---
description: Метод Shell. Strict — получает параметр ограничения группы из реестра.
ms.assetid: C4B3B5C0-7445-483a-885F-5283BD4D4B39
title: Метод Shell. Unrestricted (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.IsRestricted
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 3e428c914cf95d282fd721071009efc70fcb3a4d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108104262"
---
# <a name="shellisrestricted-method"></a>Shell. Strict, метод

Извлекает из реестра параметр ограничений группы.

## <a name="syntax"></a>Синтаксис


```JScript
iRetVal = Shell.IsRestricted(
  sGroup,
  sRestriction
)
```


```VB

Shell.IsRestricted( _
  ByVal sGroup As BSTR, _
  ByVal sRestriction As BSTR _
) As Integer
```





## <a name="parameters"></a>Параметры

<dl> <dt>

*сграуп* \[ окне\]
</dt> <dd>

Тип: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

**Строка** , содержащая имя группы. Это значение представляет собой имя подраздела реестра, в котором будет проверяться ограничение.

</dd> <dt>

*срестриктион* \[ окне\]
</dt> <dd>

Тип: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

**Строка** , содержащая ограничение, значение которого необходимо получить.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

### <a name="jscript"></a>Язык JScript

Тип: **Integer \***

Значение ограничения. Если указанное ограничение не найдено, возвращается значение 0.

### <a name="vb"></a>VB

Тип: **Integer \***

Значение ограничения. Если указанное ограничение не найдено, возвращается значение 0.

## <a name="remarks"></a>Remarks

**Ограничение** сначала ищет имя подраздела, которое соответствует *сграуп* в следующем разделе.

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Policies
```

Ограничения объявляются в виде значений отдельных подразделов политики. Если ограничение с именем в *срестриктион* находится в подразделе с именем в *сграуп*, то функция **Unrestricted** возвращает текущее значение ограничения. Если ограничение не найдено в разделе **hKey \_ локальный \_ компьютер**, то этот же подраздел проверяется в разделе **hKey \_ текущий \_ пользователь**.

Этот метод в настоящее время недоступен в Microsoft Visual Basic.

## <a name="examples"></a>Примеры

В приведенных ниже примерах показано использование параметра **ундокквисаутлогон** **для получения** значения данных из ограничения для подраздела **System** . Для JScript и VBScript отображается использование.

Присутствовал


```JScript
<script language="JScript">
    function fnIsRestricedJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var lReturn;
        
        lReturn = objShell.IsRestricted("system", "undockwithoutlogon");
        document.write(lReturn);
    }
</script>
```



Сценариев


```VB
<script language="VBScript">
    function fnIsRestricedVB()
        dim objShell
        dim lReturn

        set objShell = CreateObject("shell.application")

        lReturn = objShell.IsRestricted("system", "undockwithoutlogon")
        document.write(lReturn)

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



 

 
