---
description: Метод Жетиункновнвалуе извлекает значение интерфейса IUnknown (тип VT \_ Unknown), заданный ключом.
ms.assetid: 2197fa1f-639d-4ac1-9d5b-c6534f3ecf1c
title: 'Метод Ипортабледевицевалуес:: Жетиункновнвалуе (Портабледевицетипес. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetIUnknownValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: bc7ecfdc699cfe5f572c303d2c8a9e71bafc026b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718155"
---
# <a name="iportabledevicevaluesgetiunknownvalue-method"></a>Метод Ипортабледевицевалуес:: Жетиункновнвалуе

Метод **жетиункновнвалуе** извлекает значение интерфейса **IUnknown** (тип VT \_ Unknown), заданный ключом.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetIUnknownValue(
  [in]  REFPROPERTYKEY key,
  [out] IUnknown       **ppValue
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

Адрес переменной, которая получает указатель на полученный интерфейс **IUnknown** . Вызывающий объект отвечает за вызов метода **Release** на полученном интерфейсе.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Метод возвращает **значение HRESULT**. Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.



| Код возврата                                                                                                            | Описание                                                                  |
|------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl>                                   | Метод выполнен успешно.<br/>                                             |
| <dl> <dt>**\_вытипемисматч E \_**</dt> </dl>                   | Свойство, заданное *ключом* , не является интерфейсом **IUnknown** .<br/> |
| <dl> <dt>**HRESULT \_ из \_ Win32 (ошибка \_ не \_ найдена)**</dt> </dl> | Свойство, указанное *ключом* , отсутствует в коллекции.<br/>         |



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Портабледевицетипес. h</dt> </dl>   |
| Библиотека<br/> | <dl> <dt>Портабледевицегуидс. lib</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Интерфейс Ипортабледевицевалуес**](iportabledevicevalues.md)
</dt> <dt>

[**Ипортабледевицевалуес:: Сетиункновнвалуе**](iportabledevicevalues-setiunknownvalue.md)
</dt> </dl>

 

 




