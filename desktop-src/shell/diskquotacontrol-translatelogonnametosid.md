---
description: Преобразует имя входа в соответствующий идентификатор безопасности пользователя в строковом формате.
title: Дисккуотаконтрол. Транслателогоннаметосид, метод
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.TranslateLogonNameToSID
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 3b6b0d03-e9ef-4575-bb67-f7b7b39d2a16
ms.openlocfilehash: 5f0a2591b0f5df6bc0f50994fcbf101b7bfbb36d
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841565"
---
# <a name="diskquotacontroltranslatelogonnametosid-method"></a>Дисккуотаконтрол. Транслателогоннаметосид, метод

Преобразует имя входа в соответствующий идентификатор безопасности пользователя в строковом формате.

## <a name="syntax"></a>Синтаксис


```JScript
DiskQuotaControl.TranslateLogonNameToSID(
  logonname
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*логоннаме* 
</dt> <dd>

Тип: **строка**

Строковое значение, указывающее имя пользователя для входа.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает идентификатор безопасности пользователя (SID) в строковом формате, соответствующий указанному имени входа. Возвращаемая строка включает стандартные заключенные в фигурные скобки. Пример:

"{S-1-5-21-2127521184-1604012920-1887927527-19009}"

## <a name="remarks"></a>Remarks

Возвращенная строка идентификатора безопасности может быть передана в метод [**финдусер**](diskquotacontrol-finduser.md) вместо имени для входа.

При сбое вызова метода [**финдусер**](diskquotacontrol-finduser.md)( *логоннаме*) это может быть вызвано несоответствием между формой (например, совместимым с Security Account Manager \[ SAM \] и именем участника \[ -пользователя UPN \] ) имени входа и формы, хранящейся в кэше имен SID. В таких случаях имя входа может быть преобразовано в идентификатор безопасности, а вызов **финдусер** повторяется. **Финдусер** распознает строку идентификатора безопасности и обходит Поиск в КЭШЕ имен SID. Этот прием показан на следующем коде VBScript (Microsoft Visual Basic Scripting Edition).


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



При сравнении уточняющих запросов в кэше имен SID процесс преобразования имени в идентификатор SID может оказаться очень длительным. Таким образом, рекомендуется сначала вызвать [**финдусер**](diskquotacontrol-finduser.md) с именем для входа. В приведенном выше примере используется этот метод.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional, только для \[ классических приложений Windows XP\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shell32.dll (версия 5,0 или более поздняя)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Объект Дисккуотаконтрол**](diskquotacontrol-object.md)
</dt> </dl>

 

 




