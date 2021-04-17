---
description: 'Метод Невсегмент уведомляет ПИН-код о том, что примеры носителей, полученные после этого вызова, группируются как сегмент. Реализует метод Ипин:: Невсегмент.'
ms.assetid: e334d5a7-0398-496c-882c-bf73e6545867
title: Кбасепин. Невсегмент, метод (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.NewSegment
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1f128ce8cb2fee5479efeddd5932d0392b92a6fc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657367"
---
# <a name="cbasepinnewsegment-method"></a>Кбасепин. Невсегмент, метод

`NewSegment`Метод уведомляет ПИН-код о том, что примеры носителей, полученные после этого вызова, группируются как сегмент. Реализует метод [**Ипин:: невсегмент**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT NewSegment(
   REFERENCE_TIME tStart,
   REFERENCE_TIME tStop,
   double         dRate
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*тстарт* 
</dt> <dd>

Начальная координата носителя сегмента, в единицах 100-наносекундных.

</dd> <dt>

*тстоп* 
</dt> <dd>

Конечное расположение носителя сегмента в единицах 100-наносекундных.

</dd> <dt>

*драте* 
</dt> <dd>

Скорость обработки этого сегмента в процентах от исходной ставки.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение S \_ ОК.

## <a name="remarks"></a>Комментарии

Этот метод задает переменные члена [**кбасепин:: m \_ тстарт**](cbasepin-m-tstart.md), [**кбасепин:: m \_ тстоп**](cbasepin-m-tstop.md)и [**кбасепин:: m \_ драте**](cbasepin-m-drate.md) . В производном классе Переопределите этот метод, чтобы передать уведомление в нисходящее.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Амфилтер. h (включение Streams. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасепин**](cbasepin.md)
</dt> </dl>

 

 




