---
description: Метод Жетприватетиме извлекает значение реального времени из часов.
ms.assetid: ce9832cb-4b5a-49a1-9a69-d2fb90b3ed2e
title: Кбасереференцеклокк. Жетприватетиме, метод (Рефклокк. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseReferenceClock.GetPrivateTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 387df10472e4913d33722492bf07601faf08e3ba
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669202"
---
# <a name="cbasereferenceclockgetprivatetime-method"></a>Кбасереференцеклокк. Жетприватетиме, метод

`GetPrivateTime`Метод получает значение реального времени из часов.

## <a name="syntax"></a>Синтаксис


```C++
virtual REFERENCE_TIME GetPrivateTime();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Возвращает текущее время (в 100-наносекундных единицах).

## <a name="remarks"></a>Комментарии

Этот метод возвращает реальное время, сообщаемое часами. Внешние вызывающие объекты используют метод [**кбасереференцеклокк:: OnTime**](cbasereferenceclock-gettime.md) , который вызывает этот метод. В отличие от метода со **временем** , внутренние часы могут проходить назад. Если это происходит, метод **метода noreturn по** ошибке возвращает время последнего отчета, пока метод не закончится `GetPrivateTime` .

Этот метод возвращает системное время. Переопределите этот метод, если часы получают время из другого источника.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Рефклокк. h (включение Streams. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасереференцеклокк**](cbasereferenceclock.md)
</dt> </dl>

 

 




