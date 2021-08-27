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
ms.openlocfilehash: 6bcaa5ac4f7dff4be80763b0aa411b7f104ff786b21e422044bdc7198697d54c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120111824"
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

Возвращает идентификатор безопасности пользователя (SID) в строковом формате, соответствующий указанному имени входа. Возвращаемая строка включает стандартные заключенные в фигурные скобки. Например:

"{S-1-5-21-2127521184-1604012920-1887927527-19009}"

## <a name="remarks"></a>Remarks

Возвращенная строка идентификатора безопасности может быть передана в метод [**финдусер**](diskquotacontrol-finduser.md) вместо имени для входа.

При сбое вызова метода [**финдусер**](diskquotacontrol-finduser.md)( *логоннаме*) это может быть вызвано несоответствием между формой (например, совместимым с Security Account Manager \[ SAM \] и именем участника \[ -пользователя UPN \] ) имени входа и формы, хранящейся в кэше имен SID. В таких случаях имя входа может быть преобразовано в идентификатор безопасности, а вызов **финдусер** повторяется. **Финдусер** распознает строку идентификатора безопасности и обходит Поиск в КЭШЕ имен SID. этот прием показан на следующем коде VBScript (Microsoft Visual Basic scripting Edition).


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

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional, только для \[ настольных приложений Windows XP\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shell32.dll (версия 5,0 или более поздняя)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Объект Дисккуотаконтрол**](diskquotacontrol-object.md)
</dt> </dl>

 

 




