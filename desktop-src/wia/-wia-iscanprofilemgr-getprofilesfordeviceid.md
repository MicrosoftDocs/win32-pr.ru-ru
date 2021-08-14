---
description: Возвращает все профили сканирования, связанные с устройством.
ms.assetid: 2e509f01-9c5e-4d17-8888-b08b6b4b9fa9
title: 'Метод Исканпрофилемгр:: Жетпрофилесфордевицеид (Сканпрофилемгр. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileMgr.GetProfilesforDeviceID
api_type:
- COM
api_location:
- Scanprofilemgr.h
ms.openlocfilehash: 8ca150d02aff2f84becf8b36aca87e2da24b2b83c9ccd85c0cf5a1c5ced0d664
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118209060"
---
# <a name="iscanprofilemgrgetprofilesfordeviceid-method"></a>Метод Исканпрофилемгр:: Жетпрофилесфордевицеид

Возвращает все профили сканирования, связанные с устройством.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetProfilesforDeviceID(
  [in]      BSTR         bstrDeviceID,
  [in, out] ULONG        *pulNumProfiles,
  [out]     IScanProfile **ppScanProfile
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*бстрдевицеид* \[ окне\]
</dt> <dd>

Тип: **BSTR**

ИДЕНТИФИКАТОР устройства.

</dd> <dt>

*пулнумпрофилес* \[ в, out\]
</dt> <dd>

Тип: **ulong \***

При передаче указатель на максимальное число возвращаемых профилей. При возвращении возвращается указатель на число возвращаемых профилей.

</dd> <dt>

*ппсканпрофиле* \[ заполняет\]
</dt> <dd>

Тип: **[ **исканпрофиле**](-wia-iscanprofile.md)\*\***

Адрес указателя на массив профилей.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **HRESULT**

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="remarks"></a>Remarks

Если общее число профилей, связанных с устройством, меньше значения, переданного в *пулнумпрофилес*, то *пулнумпрофилес* возвращает этот итог. В противном случае возвращается то же значение, которое было передано в него.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                              |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                        |
| Header<br/>                   | <dl> <dt>Сканпрофилемгр. h</dt> </dl> |
| IDL<br/>                      | <dl> <dt>Сканпрофилес. idl</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**исканпрофилемгр**](-wia-iscanprofilemgr.md)
</dt> <dt>

[Схема профиля сканирования](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




