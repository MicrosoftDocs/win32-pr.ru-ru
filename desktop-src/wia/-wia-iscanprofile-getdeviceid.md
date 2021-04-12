---
description: Возвращает идентификатор устройства.
ms.assetid: 72a0843d-36f2-463f-8269-0e91233f1931
title: 'Метод Исканпрофиле:: GetDeviceID (Сканпрофиле. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile.GetDeviceID
api_type:
- COM
api_location:
- Scanprofile.h
ms.openlocfilehash: fb0e2597164cb0a82c15cecf394ce7a9e0bec16d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344015"
---
# <a name="iscanprofilegetdeviceid-method"></a>Метод Исканпрофиле:: GetDeviceID

Возвращает идентификатор устройства.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetDeviceID(
  [out] BSTR *pbstrDeviceID
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пбстрдевицеид* \[ заполняет\]
</dt> <dd>

Тип: **BSTR \** _

Указатель на идентификатор устройства.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: _ *HRESULT**

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                              |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                        |
| Header<br/>                   | <dl> <dt>Сканпрофиле. h</dt> </dl>    |
| IDL<br/>                      | <dl> <dt>Сканпрофилес. idl</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**исканпрофиле**](-wia-iscanprofile.md)
</dt> <dt>

[Схема профиля сканирования](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




