---
description: Возвращает значение, указывающее, является ли профиль профилем сканирования по умолчанию для связанного устройства IWiaItem2.
ms.assetid: 32ca3b9f-6235-4eec-aa94-bf20f15a9a16
title: 'Метод Исканпрофиле:: Default (Сканпрофиле. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile.IsDefault
api_type:
- COM
api_location:
- Scanprofile.h
ms.openlocfilehash: 3f763286a6db8430514cd70bc05eb160935e0fdc7ae8b5c452e8c09a113c0af5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119882414"
---
# <a name="iscanprofileisdefault-method"></a>Метод Исканпрофиле:: Default

Возвращает значение, указывающее, является ли профиль профилем сканирования по умолчанию для связанного устройства [**IWiaItem2**](-wia-iwiaitem2.md) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT IsDefault(
  [out] BOOL *pbDefault
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пбдефаулт* \[ заполняет\]
</dt> <dd>

Тип: **bool \*** .

Указатель на **логическое** значение.

<dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**УСЛОВИЯ**


</dt> <dd>

По умолчанию используется профиль.

</dd> <dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**ISFALSE**


</dt> <dd>

Профиль не является значением по умолчанию.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **HRESULT**

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="remarks"></a>Remarks

*пбдефаулт* имеет **значение true** , если профиль содержит `<Default>` элемент. **Значение false** , если такой элемент отсутствует. Элемент не имеет значения.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                              |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                        |
| Заголовок<br/>                   | <dl> <dt>Сканпрофиле. h</dt> </dl>    |
| IDL<br/>                      | <dl> <dt>Сканпрофилес. idl</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**исканпрофиле**](-wia-iscanprofile.md)
</dt> <dt>

[Схема профиля сканирования](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




