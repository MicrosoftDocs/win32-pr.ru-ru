---
description: 'Метод Невсегмент уведомляет ПИН-код о том, что примеры носителей, полученные после этого вызова, группируются как сегмент. Этот метод реализует метод Ипин:: Невсегмент.'
ms.assetid: 8925b8b5-13dd-4127-82d8-96525bd4d6fc
title: Ктрансформинпутпин. Невсегмент, метод (Трансфрм. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.NewSegment
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 25c455fe5ec6ddf9157e991b70b468ace653daa9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675845"
---
# <a name="ctransforminputpinnewsegment-method"></a>Ктрансформинпутпин. Невсегмент, метод

`NewSegment`Метод уведомляет ПИН-код о том, что примеры носителей, полученные после этого вызова, группируются как сегмент. Этот метод реализует метод [**Ипин:: невсегмент**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment) .

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

Время начала сегмента.

</dd> <dt>

*тстоп* 
</dt> <dd>

Время окончания сегмента.

</dd> <dt>

*драте* 
</dt> <dd>

Интенсивность сегмента.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает \_ значение, равное ОК или другому значению **HRESULT** .

## <a name="remarks"></a>Комментарии

Этот метод переопределяет метод [**кбасепин:: невсегмент**](cbasepin-newsegment.md) . Он вызывает метод [**ктрансформфилтер:: невсегмент**](ctransformfilter-newsegment.md) фильтра для предоставления вызова в нисходящем направлении.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Трансфрм. h (включение Streams. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



 

 




