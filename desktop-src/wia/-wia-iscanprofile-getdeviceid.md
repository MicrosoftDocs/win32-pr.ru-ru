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
ms.openlocfilehash: 484c9a53542b0f7b62c00ca030b4bee9276914dce28bd3034865f308ba80705e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120007614"
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

Тип: **BSTR \***

Указатель на идентификатор устройства.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **HRESULT**

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                              |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                        |
| Заголовок<br/>                   | <dl> <dt>Сканпрофиле. h</dt> </dl>    |
| IDL<br/>                      | <dl> <dt>Сканпрофилес. idl</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**исканпрофиле**](-wia-iscanprofile.md)
</dt> <dt>

[Схема профиля сканирования](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




