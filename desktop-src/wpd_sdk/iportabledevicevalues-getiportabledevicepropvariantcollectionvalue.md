---
description: Метод Жетипортабледевицепропвариантколлектионвалуе извлекает значение Ипортабледевицепропвариантколлектион (тип VT \_ Unknown), заданный ключом.
ms.assetid: a7b5ba64-c28e-42ae-9f04-2bdb67e93328
title: 'Метод Ипортабледевицевалуес:: Жетипортабледевицепропвариантколлектионвалуе (Портабледевицетипес. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetIPortableDevicePropVariantCollectionValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: d0ca7f2350fee8ba5d7cea85eb19c874eb5893f86f0e17fa1b4f0e97087e7c34
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120055194"
---
# <a name="iportabledevicevaluesgetiportabledevicepropvariantcollectionvalue-method"></a>Метод Ипортабледевицевалуес:: Жетипортабледевицепропвариантколлектионвалуе

Метод **жетипортабледевицепропвариантколлектионвалуе** извлекает значение **ИПОРТАБЛЕДЕВИЦЕПРОПВАРИАНТКОЛЛЕКТИОН** (тип VT \_ Unknown), заданный ключом.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetIPortableDevicePropVariantCollectionValue(
  [in]  REFPROPERTYKEY                       key,
  [out] IPortableDevicePropVariantCollection **ppValue
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ключ* \[ окне\]
</dt> <dd>

Ключ **рефпропертикэй** , указывающий извлекаемый элемент.

</dd> <dt>

*ппвалуе* \[ заполняет\]
</dt> <dd>

Адрес переменной, которая получает указатель на полученный интерфейс [**ипортабледевицепропвариантколлектион**](iportabledevicepropvariantcollection.md) . Вызывающий объект отвечает за вызов метода **Release** на полученном интерфейсе.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Метод возвращает **значение HRESULT**. Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.



| Код возврата                                                                                                            | Описание                                                                                              |
|------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl>                                   | Метод выполнен успешно.<br/>                                                                         |
| <dl> <dt>**\_вытипемисматч E \_**</dt> </dl>                   | Свойство, заданное *ключом* , не является интерфейсом **ипортабледевицепропвариантколлектион** .<br/> |
| <dl> <dt>**HRESULT \_ из \_ Win32 (ошибка \_ не \_ найдена)**</dt> </dl> | Свойство, указанное *ключом* , отсутствует в коллекции.<br/>                                     |



 

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>Портабледевицетипес. h</dt> </dl>   |
| Библиотека<br/> | <dl> <dt>Портабледевицегуидс. lib</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Интерфейс Ипортабледевицевалуес**](iportabledevicevalues.md)
</dt> <dt>

[**Ипортабледевицевалуес:: Сетипортабледевицепропвариантколлектионвалуе**](iportabledevicevalues-setiportabledevicepropvariantcollectionvalue.md)
</dt> </dl>

 

 




