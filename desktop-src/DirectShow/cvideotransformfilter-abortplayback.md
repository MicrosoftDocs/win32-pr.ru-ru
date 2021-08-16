---
description: Метод Абортплайбакк используется для сигнализации об ошибке потоковой передачи. он отправляет событие EC \_ еррораборт в фильтр Graph Manager и отправляет уведомление о завершении потока.
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
ms.openlocfilehash: 6560e7ce704423bfecc519c709c2c08733fe90a2346324f9e1282571530293ac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117821939"
---
# <a name="cvideotransformfilterabortplayback-method"></a>Квидеотрансформфилтер. Абортплайбакк, метод

`AbortPlayback`Метод используется для сигнализации об ошибке потоковой передачи. он отправляет событие [**EC \_ еррораборт**](ec-errorabort.md) в фильтр Graph Manager и отправляет уведомление о завершении потока.

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
| Заголовок<br/>  | <dl> <dt>втранс. h (включает Потоки. h)</dt> </dl>                                                                                    |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Квидеотрансформфилтер**](cvideotransformfilter.md)
</dt> </dl>

 

 




