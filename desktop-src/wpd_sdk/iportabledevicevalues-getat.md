---
description: Метод GetAt извлекает значение из коллекции, используя указанный индекс, начинающийся с нуля.
ms.assetid: d52675f0-55b4-43ef-bb1d-ff6aa8a70647
title: 'Метод Ипортабледевицевалуес:: GetAt (Портабледевицетипес. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetAt
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 4e234d0fe24eec947b388b5da798c55e7478ffa6bda69a9b9fe57c279af6d96e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117843027"
---
# <a name="iportabledevicevaluesgetat-method"></a>Метод Ипортабледевицевалуес:: GetAt

Метод **GetAt** извлекает значение из коллекции, используя указанный индекс, начинающийся с нуля.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetAt(
  [in]      const DWORD       index,
  [in, out]       PROPERTYKEY *pKey,
  [in, out]       PROPVARIANT *pValue
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*индекс* \[ окне\]
</dt> <dd>

Значение **типа DWORD** , указывающее Отсчитываемый от нуля индекс в коллекции.

</dd> <dt>

*pKey* \[ в, out\]
</dt> <dd>

Необязательный указатель **PROPERTYKEY** , извлекающий ключ указанного элемента.

</dd> <dt>

*pValue* \[ в, out\]
</dt> <dd>

Необязательный **пропвариант** , который получает значение указанного элемента. Вызывающий объект должен освободить память, вызвав **пропвариантклеар** , когда завершится с ней.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Метод возвращает **значение HRESULT**. Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.



| Код возврата                                                                                  | Описание                                       |
|----------------------------------------------------------------------------------------------|---------------------------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl>         | Метод выполнен успешно.<br/>                  |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Указан недопустимый номер индекса.<br/> |



 

## <a name="remarks"></a>Remarks

если свойство указывает значение типа VT \_ UNKNOWN, свойство будет одним из Windows портативных устройств ([**ипортабледевицекэйколлектион**](iportabledevicekeycollection.md), [**ипортабледевицевалуесколлектион**](iportabledevicevaluescollection.md), [**ипортабледевицевалуес**](iportabledevicevalues.md) или [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md)). Windows переносные устройства не могут возвращать другие интерфейсы.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>Портабледевицетипес. h</dt> </dl>   |
| Библиотека<br/> | <dl> <dt>Портабледевицегуидс. lib</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Интерфейс Ипортабледевицевалуес**](iportabledevicevalues.md)
</dt> <dt>

[**Ипортабледевицевалуес:: GetStringValue**](iportabledevicevalues-getstringvalue.md)
</dt> </dl>

 

 




