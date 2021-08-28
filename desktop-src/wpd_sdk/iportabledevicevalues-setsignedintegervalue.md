---
description: Метод Сетсигнединтежервалуе добавляет новое ДЛИННое значение (тип VT \_ i4) или перезаписывает существующий.
ms.assetid: b0bb2992-2906-446c-be9a-20bff13f8e1d
title: 'Метод Ипортабледевицевалуес:: Сетсигнединтежервалуе (Портабледевицетипес. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.SetSignedIntegerValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 71e5354c730671a4be5f344bb2503683f497003ddccecbd250490304f607e9ad
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119704734"
---
# <a name="iportabledevicevaluessetsignedintegervalue-method"></a>Метод Ипортабледевицевалуес:: Сетсигнединтежервалуе

Метод **сетсигнединтежервалуе** добавляет новое **длинное** значение (тип VT \_ i4) или перезаписывает существующий.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT SetSignedIntegerValue(
  [in]       REFPROPERTYKEY key,
  [in] const LONG           Value
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

**Целое** число, указывающее новое значение.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Метод возвращает **значение HRESULT**. Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.



| Код возврата                                                                          | Описание                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl> | Метод выполнен успешно.<br/> |



 

## <a name="remarks"></a>Remarks

Если существующее значение имеет тот же ключ, что и параметр *Key* , он перезаписывает существующее значение без предупреждения.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>Портабледевицетипес. h</dt> </dl>   |
| Библиотека<br/> | <dl> <dt>Портабледевицегуидс. lib</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Интерфейс Ипортабледевицевалуес**](iportabledevicevalues.md)
</dt> <dt>

[**Ипортабледевицевалуес:: Жетсигнединтежервалуе**](iportabledevicevalues-getsignedintegervalue.md)
</dt> </dl>

 

 




