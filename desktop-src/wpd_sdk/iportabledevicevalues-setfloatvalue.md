---
description: Метод Сетфлоатвалуе добавляет новое значение FLOAT (Type VT \_ R4) или перезаписывает существующий.
ms.assetid: 1e0c9d19-47bf-4d93-a0c0-27e2c4897012
title: 'Метод Ипортабледевицевалуес:: Сетфлоатвалуе (Портабледевицетипес. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.SetFloatValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 347cf93fe68e989eebb921472d1e81e4d0aa650e92d2c535dfdd93a6d823ed1d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119657814"
---
# <a name="iportabledevicevaluessetfloatvalue-method"></a>Метод Ипортабледевицевалуес:: Сетфлоатвалуе

Метод **сетфлоатвалуе** добавляет новое значение **float** (Type VT \_ R4) или перезаписывает существующий.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT SetFloatValue(
  [in]       REFPROPERTYKEY key,
  [in] const FLOAT          Value
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ключ* \[ окне\]
</dt> <dd>

Объект **рефпропертикэй** , указывающий элемент для создания или перезаписи.

</dd> <dt>

*Значение* \[ окне\]
</dt> <dd>

**Число с плавающей запятой** , содержащее новое значение.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Метод возвращает **значение HRESULT**. Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.



| Код возврата                                                                          | Описание                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl> | Метод выполнен успешно.<br/> |



 

## <a name="remarks"></a>Remarks

Если существующее значение имеет тот же ключ, что и параметр *Key* , он перезаписывает существующее значение без предупреждения.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>Портабледевицетипес. h</dt> </dl>   |
| Библиотека<br/> | <dl> <dt>Портабледевицегуидс. lib</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Интерфейс Ипортабледевицевалуес**](iportabledevicevalues.md)
</dt> <dt>

[**Ипортабледевицевалуес:: Жетфлоатвалуе**](iportabledevicevalues-getfloatvalue.md)
</dt> </dl>

 

 




