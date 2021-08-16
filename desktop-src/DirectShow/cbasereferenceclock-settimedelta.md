---
description: Метод Сеттимеделта корректирует время внутренних часов.
ms.assetid: 51534c92-5573-4e2a-baeb-b1a82ccf88de
title: Кбасереференцеклокк. Сеттимеделта, метод (Рефклокк. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseReferenceClock.SetTimeDelta
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ac9eba5337fa43e43e3b7a45a7a92263fd4e6d69388185a2096c1a270590e482
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118403443"
---
# <a name="cbasereferenceclocksettimedelta-method"></a>Кбасереференцеклокк. Сеттимеделта, метод

`SetTimeDelta`Метод корректирует время внутренних часов.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT SetTimeDelta(
  [ref] const REFERENCE_TIME &TimeDelta
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Тимеделта* \[ ЗНАЧ\]
</dt> <dd>

Сумма для корректировки времени в 100-наносекундных единицах. Положительное значение перемещает часы вперед, а отрицательное значение перемещает часы назад.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение S \_ ОК.

## <a name="remarks"></a>Remarks

Производный класс может использовать этот метод для корректировки внутренних часов, если он отклоняется от устройства, предоставляющего сведения о времени.

Метод [**кбасереференцеклокк:: OnTime**](cbasereferenceclock-gettime.md) никогда не возвращает значения по убыванию. Если настроить часы назад, функция @ **time** возвращает предыдущее значение до тех пор, пока часы не достигнет этого значения.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>рефклокк. h (включает Потоки. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасереференцеклокк**](cbasereferenceclock.md)
</dt> </dl>

 

 




