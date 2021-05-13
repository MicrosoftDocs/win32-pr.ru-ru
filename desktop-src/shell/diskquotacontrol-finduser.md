---
description: Поиск записи пользователя по имени в файле квоты тома.
title: Дисккуотаконтрол. Финдусер, метод
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.FindUser
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: e5767d28-4c0a-49bc-a1d3-ba809411456d
ms.openlocfilehash: eab539a5ec5a360ae28fc87d5ffbb9dd4f9f1cc8
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841525"
---
# <a name="diskquotacontrolfinduser-method"></a>Дисккуотаконтрол. Финдусер, метод

Поиск записи пользователя по имени в файле квоты тома.

## <a name="syntax"></a>Синтаксис


```JScript
DiskQuotaControl.FindUser(
  sLogonName
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*слогоннаме* 
</dt> <dd>

Тип: **строка**

Строковое значение, содержащее имя входа пользователя.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает выражение объекта, результатом которого является объект пользователя [**дидисккуотаусер**](didiskquotauser-object.md) .

## <a name="remarks"></a>Remarks

Этот метод возвращает объект [**дидисккуотаусер**](didiskquotauser-object.md) , даже если в файле квоты нет записи для пользователя. Возвращенный объект пользователя имеет порог предупреждения, а ограничения жестких квот установлены на значения по умолчанию для тома.

Строка, возвращаемая из [**транслателогоннаметосид**](diskquotacontrol-translatelogonnametosid.md) , может передаваться вместо параметра *слогоннаме* . Когда **финдусер** получает строку идентификатора безопасности, она использует соответствующий идентификатор безопасности для прямого поиска записи квот пользователя на томе. Это обходит кэш имен SID. В случаях, когда **финдусер** завершается сбоем из-за несоответствия в формате (например, с SAM-совместимым и UPN) имени входа и кэшированного имени входа, имя входа может быть преобразовано в строку идентификатора SID с помощью **транслателогоннаметосид** , затем снова передается в **финдусер**. Этот метод показан в следующем коде VBScript.


```
Function Find(dqc, name)
    On Error Resume Next
    SET Find = dqc.FindUser(name)

    If Err.Number <> 0 Then
        Err.Clear
        SET Find = dqc.FindUser(dqc.TranslateLogonNameToSID(name))
    End If    

End Function
```



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                                                    |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shell32.dll (версия 5,0 или более поздняя)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Объект Дисккуотаконтрол**](diskquotacontrol-object.md)
</dt> </dl>

 

 




