---
description: Возвращает профиль сканирования по умолчанию.
ms.assetid: 0e5ca06a-78ca-4d24-8dda-26babc3124b5
title: 'Метод Исканпрофилемгр:: Жетдефаултпрофиле (Сканпрофилемгр. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileMgr.GetDefaultProfile
api_type:
- COM
api_location:
- Scanprofilemgr.h
ms.openlocfilehash: a496a2e606e389f8b2e1dfd7808d56e4360108a27ef66fbc0937ef1040514e44
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119549765"
---
# <a name="iscanprofilemgrgetdefaultprofile-method"></a>Метод Исканпрофилемгр:: Жетдефаултпрофиле

Возвращает профиль сканирования по умолчанию.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetDefaultProfile(
  [in]  BSTR         bstrDeviceID,
  [out] IScanProfile **ppScanProfile
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*бстрдевицеид* \[ окне\]
</dt> <dd>

Тип: **BSTR**

ИДЕНТИФИКАТОР устройства.

</dd> <dt>

*ппсканпрофиле* \[ заполняет\]
</dt> <dd>

Тип: **[ **исканпрофиле**](-wia-iscanprofile.md)\*\***

Адрес указателя на профиль по умолчанию для устройства.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **HRESULT**

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="remarks"></a>Remarks

Профиль по умолчанию содержит `<Default>` элемент.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                              |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                        |
| Заголовок<br/>                   | <dl> <dt>Сканпрофилемгр. h</dt> </dl> |
| IDL<br/>                      | <dl> <dt>Сканпрофилес. idl</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**исканпрофилемгр**](-wia-iscanprofilemgr.md)
</dt> <dt>

[Схема профиля сканирования](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




