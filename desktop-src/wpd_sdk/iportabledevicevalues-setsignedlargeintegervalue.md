---
description: Метод Сетсигнедларжеинтежервалуе добавляет новое значение ЛОНГЛОНГ (Type VT \_ I8) или перезаписывает существующий.
ms.assetid: 604b48ed-3e3f-4a06-91dd-7ece9f146824
title: 'Метод Ипортабледевицевалуес:: Сетсигнедларжеинтежервалуе (Портабледевицетипес. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.SetSignedLargeIntegerValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 5ac0ec7e7dce817565ea8b260501879ca8423b090ff357b30f177ff828c8ff9d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119026772"
---
# <a name="iportabledevicevaluessetsignedlargeintegervalue-method"></a>Метод Ипортабледевицевалуес:: Сетсигнедларжеинтежервалуе

Метод **сетсигнедларжеинтежервалуе** добавляет новое значение **ЛОНГЛОНГ** (Type VT \_ I8) или перезаписывает существующий.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT SetSignedLargeIntegerValue(
  [in]       REFPROPERTYKEY key,
  [in] const LONGLONG       Value
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

Объект **лонглонг** , указывающий новое значение.

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

[**Ипортабледевицевалуес:: Жетсигнедларжеинтежервалуе**](iportabledevicevalues-getsignedlargeintegervalue.md)
</dt> </dl>

 

 




