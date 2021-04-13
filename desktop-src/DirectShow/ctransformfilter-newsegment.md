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
ms.openlocfilehash: 0fd046288886d3e7619419dd591dd94310f56020
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657747"
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

## <a name="remarks"></a>Комментарии

Метод [**ктрансформинпутпин:: невсегмент**](ctransforminputpin-newsegment.md) входного контакта вызывает этот метод. Этот метод доставляет `NewSegment` вызов нисходящего входного ПИН-кода.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Трансфрм. h (включение Streams. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Ктрансформфилтер**](ctransformfilter.md)
</dt> </dl>

 

 




