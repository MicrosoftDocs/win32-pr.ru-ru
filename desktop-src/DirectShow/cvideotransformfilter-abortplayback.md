---
description: Метод Абортплайбакк используется для сигнализации об ошибке потоковой передачи. Он отправляет событие EC \_ еррораборт в Диспетчер графа фильтров и отправляет уведомление о завершении потока.
ms.assetid: b48ec72f-d220-4b27-98fc-88eaa4f663eb
title: Квидеотрансформфилтер. Абортплайбакк, метод (Втранс. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CVideoTransformFilter.AbortPlayback
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 952987dec315408920e92d79003480a01640d14e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105674835"
---
# <a name="cvideotransformfilterabortplayback-method"></a>Квидеотрансформфилтер. Абортплайбакк, метод

`AbortPlayback`Метод используется для сигнализации об ошибке потоковой передачи. Он отправляет событие [**EC \_ Еррораборт**](ec-errorabort.md) в Диспетчер графа фильтров и отправляет уведомление о завершении потока.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT AbortPlayback(
   HRESULT hr
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ч* 
</dt> <dd>

Значение **HRESULT** операции, которая завершилась ошибкой. Это значение используется в качестве первого параметра события для \_ события EC еррораборт.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение параметра *HR* .

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Втранс. h (включение Streams. h)</dt> </dl>                                                                                    |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Квидеотрансформфилтер**](cvideotransformfilter.md)
</dt> </dl>

 

 




