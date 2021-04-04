---
description: Получает все профили сканирования, доступные для пользователя в системе, в которой выполняется приложение.
ms.assetid: 9787079e-283c-4f6d-b97c-cfc1349ada30
title: 'Метод Исканпрофилемгр:: (Сканпрофилемгр. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileMgr.GetProfiles
api_type:
- COM
api_location:
- Scanprofilemgr.h
ms.openlocfilehash: 13949fe08dd547ecb5319e18ecc84139ccd310bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103813881"
---
# <a name="iscanprofilemgrgetprofiles-method"></a>Метод Исканпрофилемгр::

Получает все профили сканирования, доступные для пользователя в системе, в которой выполняется приложение.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetProfiles(
  [in, out] ULONG        *pulNumProfiles,
  [out]     IScanProfile **ppScanProfile
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пулнумпрофилес* \[ в, out\]
</dt> <dd>

Тип: **ulong \** _

При передаче указатель на максимальное число возвращаемых профилей. При возвращении — указатель на число возвращенных профилей.

</dd> <dt>

_ppScanProfile * \[ out\]
</dt> <dd>

Тип: **[ **исканпрофиле**](-wia-iscanprofile.md)\*\***

Адрес массива указателей на профили.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **HRESULT**

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="remarks"></a>Комментарии

Если общее число профилей, доступных для пользователя, меньше значения, переданного в *пулнумпрофилес*, то *пулнумпрофилес* возвращает этот итог. В противном случае возвращается то же значение, которое было передано в него.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                              |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                        |
| Header<br/>                   | <dl> <dt>Сканпрофилемгр. h</dt> </dl> |
| IDL<br/>                      | <dl> <dt>Сканпрофилес. idl</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**исканпрофилемгр**](-wia-iscanprofilemgr.md)
</dt> <dt>

[Схема профиля сканирования](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




