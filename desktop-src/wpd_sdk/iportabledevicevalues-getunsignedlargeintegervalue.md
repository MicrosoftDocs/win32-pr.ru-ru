---
description: Метод Жетунсигнедларжеинтежервалуе извлекает значение УЛОНГЛОНГ (Type VT \_ UI8), заданное ключом.
ms.assetid: de37c49b-a5f4-424d-8320-1de2d5a624aa
title: 'Метод Ипортабледевицевалуес:: Жетунсигнедларжеинтежервалуе (Портабледевицетипес. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetUnsignedLargeIntegerValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 48f6093f32d43737b1999c3474f74569ecd3f8cd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648040"
---
# <a name="iportabledevicevaluesgetunsignedlargeintegervalue-method"></a>Метод Ипортабледевицевалуес:: Жетунсигнедларжеинтежервалуе

Метод **жетунсигнедларжеинтежервалуе** извлекает значение **УЛОНГЛОНГ** (Type VT \_ UI8), заданное ключом.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetUnsignedLargeIntegerValue(
  [in]  REFPROPERTYKEY key,
  [out] ULONGLONG      *pValue
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ключ* \[ окне\]
</dt> <dd>

Ключ **рефпропертикэй** , указывающий извлекаемый элемент.

</dd> <dt>

*pValue* \[ заполняет\]
</dt> <dd>

Указатель на полученное значение **улонглонг** .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Метод возвращает **значение HRESULT**. Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.



| Код возврата                                                                                                            | Описание                                                             |
|------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl>                                   | Метод выполнен успешно.<br/>                                        |
| <dl> <dt>**\_вытипемисматч E \_**</dt> </dl>                   | Свойство, указанное *ключом* , не является типом **улонглонг** .<br/> |
| <dl> <dt>**HRESULT \_ из \_ Win32 (ошибка \_ не \_ найдена)**</dt> </dl> | Свойство, указанное *ключом* , отсутствует в коллекции.<br/>    |



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Портабледевицетипес. h</dt> </dl>   |
| Библиотека<br/> | <dl> <dt>Портабледевицегуидс. lib</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Интерфейс Ипортабледевицевалуес**](iportabledevicevalues.md)
</dt> <dt>

[**Ипортабледевицевалуес:: Сетунсигнедларжеинтежервалуе**](iportabledevicevalues-setunsignedlargeintegervalue.md)
</dt> </dl>

 

 




