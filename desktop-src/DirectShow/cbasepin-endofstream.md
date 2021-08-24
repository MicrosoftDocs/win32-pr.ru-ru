---
description: 'Метод EndOfStream уведомляет ПИН-код о том, что дополнительные данные не ожидаются. Этот метод реализует метод Ипин:: EndOfStream. Вызывайте этот метод только для входных ПИН-кодов.'
ms.assetid: 52a71c30-bd68-4152-8901-71ef2e65913a
title: Кбасепин. EndOfStream, метод (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.EndOfStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f9e1549000be728da0118323303a60a23a5930ad68d3c7d2d2b6c9c92d54c3d3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119916434"
---
# <a name="cbasepinendofstream-method"></a>Кбасепин. EndOfStream, метод

`EndOfStream`Метод уведомляет ПИН-код о том, что дополнительные данные не ожидаются. Этот метод реализует метод [**Ипин:: EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) . Вызывайте этот метод только для входных ПИН-кодов.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT EndOfStream();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение S \_ ОК.

## <a name="remarks"></a>Remarks

Фильтр должен передавать уведомления о завершении потока в подчиненные входные контакты подключенных фильтров. Если фильтр является модулем подготовки отчетов, он должен опубликовать уведомление о событии [**EC \_ Complete**](ec-complete.md) в диспетчере графов фильтров. дополнительные сведения см. [в разделе Flow данных в фильтре Graph](data-flow-in-the-filter-graph.md).

В базовом классе этот метод не выполняет никаких действий. Производные классы должны переопределять этот метод.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>амфилтер. h (включает Потоки. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Кбасепин**](cbasepin.md)
</dt> </dl>

 

 




