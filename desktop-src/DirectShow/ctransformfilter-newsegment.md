---
description: Метод Невсегмент уведомляет фильтр о том, что примеры носителей, полученные после этого вызова, группируются в виде сегмента.
ms.assetid: 78ddaac7-9c1f-47b6-835d-dd16b1f5b01f
title: Ктрансформфилтер. Невсегмент, метод (Трансфрм. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.NewSegment
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a2cb83c376b012ae3474f87b0f8d26c7fb5560812c1d8ddcbb3ea62293797bb9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118953553"
---
# <a name="ctransformfilternewsegment-method"></a>Ктрансформфилтер. Невсегмент, метод

`NewSegment`Метод уведомляет фильтр о том, что примеры носителей, полученные после этого вызова, группируются в виде сегмента.

## <a name="syntax"></a>Синтаксис


```C++
virtual HRESULT NewSegment(
   REFERENCE_TIME tStart,
   REFERENCE_TIME tStop,
   double         dRate
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*тстарт* 
</dt> <dd>

Время начала сегмента относительно исходного источника.

</dd> <dt>

*тстоп* 
</dt> <dd>

Время окончания сегмента относительно исходного источника.

</dd> <dt>

*драте* 
</dt> <dd>

Скорость обработки сегмента.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение S \_ ОК.

## <a name="remarks"></a>Remarks

Метод [**ктрансформинпутпин:: невсегмент**](ctransforminputpin-newsegment.md) входного контакта вызывает этот метод. Этот метод доставляет `NewSegment` вызов нисходящего входного ПИН-кода.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>трансфрм. h (включает Потоки. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Ктрансформфилтер**](ctransformfilter.md)
</dt> </dl>

 

 




