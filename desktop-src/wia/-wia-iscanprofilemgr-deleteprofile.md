---
description: Удаляет указанный профиль сканирования.
ms.assetid: 31020528-3a96-492f-a3a1-e9075d4ffd14
title: 'Исканпрофилемгр: метод:D Елетепрофиле (Сканпрофилемгр. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileMgr.DeleteProfile
api_type:
- COM
api_location:
- Scanprofilemgr.h
ms.openlocfilehash: 52a4f2fc11e2a2cac1c3b3c547ee1b7a967a5441fc44cd2bb213bdbf681df8f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117670257"
---
# <a name="iscanprofilemgrdeleteprofile-method"></a>Исканпрофилемгр: метод:D Елетепрофиле

Удаляет указанный профиль сканирования.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT DeleteProfile(
  [in] IScanProfile *pScanProfile
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*псканпрофиле* \[ окне\]
</dt> <dd>

Тип: **[ **исканпрофиле**](-wia-iscanprofile.md)\***

Указатель на профиль.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **HRESULT**

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="remarks"></a>Remarks

**Исканпрофилемгр::D елетепрофиле** удаляет профиль с диска и уничтожает объект профиля в памяти.

Используйте метод [**исканпрофилемгр:: Refresh**](-wia-iscanprofilemgr-refresh.md) , если несколько объектов [**исканпрофилемгр**](-wia-iscanprofilemgr.md) могут создавать или удалять профили одновременно.

## <a name="requirements"></a>Требования



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

 

 




