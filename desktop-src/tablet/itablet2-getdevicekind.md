---
description: Возвращает тип аппаратного устройства, которое представляет объект планшета, например мышь, перо или сенсорный ввод.
ms.assetid: 693cb45f-958d-42e2-a3ee-a7cfcc72e5c3
title: 'Метод ITablet2:: Жетдевицекинд'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITablet2.GetDeviceKind
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: f20b1fe6a5a48196f6b3adc5982f2596d93f0863
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105719563"
---
# <a name="itablet2getdevicekind-method"></a>Метод ITablet2:: Жетдевицекинд

Возвращает тип аппаратного устройства, которое представляет объект планшета, например мышь, перо или сенсорный ввод.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetDeviceKind(
  [out] TABLET_DEVICE_KIND *pKind
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пкинд* \[ заполняет\]
</dt> <dd>

Значение перечисления, указывающее тип планшета, например мышь, перо или сенсорный ввод.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод может возвращать одно из этих значений.



| Код возврата                                                                            | Описание                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl>   | Успешно.<br/>                       |
| <dl> <dt>**\_Ошибка E**</dt> </dl> | Произошла неизвестная ошибка.<br/> |



 

## <a name="remarks"></a>Комментарии

Этот интерфейс и метод появились в Windows Vista.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только классические приложения Windows XP Tablet PC Edition \[\]<br/>                          |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                              |
| Библиотека<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Интерфейс ITablet2**](itablet2.md)
</dt> <dt>

[**\_Перечисление типов планшетных устройств \_**](tablet-device-kind.md)
</dt> <dt>

[**Интерфейс Итаблет**](itablet.md)
</dt> </dl>

 

 




