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
ms.openlocfilehash: e1db540b1097428e20104d95a8a7a6726566c7cd8939a11ec4041c1aa9475afd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118450531"
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



 

## <a name="remarks"></a>Remarks

этот интерфейс и метод появились в Windows Vista.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows XP Tablet PC Edition \[ только классические приложения\]<br/>                          |
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

 

 




