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
ms.openlocfilehash: c522755fe898717f0c06af9698be07ab2ebca491666982d6ff62756ef48ae08f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119907424"
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

## <a name="remarks"></a>Remarks

Этот метод переопределяет метод [**кбасепин:: невсегмент**](cbasepin-newsegment.md) . Он вызывает метод [**ктрансформфилтер:: невсегмент**](ctransformfilter-newsegment.md) фильтра для предоставления вызова в нисходящем направлении.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>трансфрм. h (включает Потоки. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



 

 




