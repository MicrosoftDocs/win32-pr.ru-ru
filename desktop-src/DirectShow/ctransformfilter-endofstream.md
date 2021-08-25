---
description: Метод EndOfStream уведомляет фильтр о том, что из входного ПИН-кода не ожидается дополнительных данных.
ms.assetid: b8fc3976-e3d4-4f16-82b0-3900ad6a740c
title: Ктрансформфилтер. EndOfStream, метод (Трансфрм. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.EndOfStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ade419666b1df36e851d5d945e14d9035c1377145cecd472244c9178758f45f1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119907634"
---
# <a name="ctransformfilterendofstream-method"></a>Ктрансформфилтер. EndOfStream, метод

`EndOfStream`Метод уведомляет фильтр о том, что из входного ПИН-кода не ожидается дополнительных данных.

## <a name="syntax"></a>Синтаксис


```C++
virtual HRESULT EndOfStream();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Возвращает \_ значение, равное ОК или другому значению **HRESULT** .

## <a name="remarks"></a>Remarks

Метод [**ктрансформинпутпин:: EndOfStream**](ctransforminputpin-endofstream.md) входного контакта вызывает этот метод. Этот метод доставляет уведомление о завершении потока. Если производный класс использует рабочий поток для доставки образцов мультимедиа, он должен переопределить этот метод и поставить в очередь уведомление о завершении потока.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>трансфрм. h (включает Потоки. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Ктрансформфилтер**](ctransformfilter.md)
</dt> </dl>

 

 




