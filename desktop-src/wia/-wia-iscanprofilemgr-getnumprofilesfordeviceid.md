---
description: Возвращает число профилей сканирования для устройства.
ms.assetid: fb1f8884-28ef-460e-a8c4-b9608cc89dc6
title: 'Метод Исканпрофилемгр:: Жетнумпрофилесфордевицеид (Сканпрофилемгр. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileMgr.GetNumProfilesforDeviceID
api_type:
- COM
api_location:
- Scanprofilemgr.h
ms.openlocfilehash: 1a65e1f6571f4ec12a9bd91749c7419f9f9641c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263309"
---
# <a name="iscanprofilemgrgetnumprofilesfordeviceid-method"></a>Метод Исканпрофилемгр:: Жетнумпрофилесфордевицеид

Возвращает число профилей сканирования для устройства.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetNumProfilesforDeviceID(
  [in]  BSTR  bstrDeviceID,
  [out] ULONG *pulNumProfiles
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*бстрдевицеид* \[ окне\]
</dt> <dd>

Тип: **BSTR**

ИДЕНТИФИКАТОР устройства.

</dd> <dt>

*пулнумпрофилес* \[ заполняет\]
</dt> <dd>

Тип: **ulong \** _

Указатель на количество профилей, доступных для устройства.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: _ *HRESULT**

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

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

 

 




