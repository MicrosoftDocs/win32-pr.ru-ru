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
ms.openlocfilehash: de58363119dc08c21d2cab0070b438ad6b4331e0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669196"
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

## <a name="remarks"></a>Комментарии

Производный класс может использовать этот метод для корректировки внутренних часов, если он отклоняется от устройства, предоставляющего сведения о времени.

Метод [**кбасереференцеклокк:: OnTime**](cbasereferenceclock-gettime.md) никогда не возвращает значения по убыванию. Если настроить часы назад, функция @ **time** возвращает предыдущее значение до тех пор, пока часы не достигнет этого значения.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Рефклокк. h (включение Streams. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасереференцеклокк**](cbasereferenceclock.md)
</dt> </dl>

 

 




