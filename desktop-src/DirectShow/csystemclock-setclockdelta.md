---
description: 'Метод Сетклоккделта корректирует время в часах. Этот метод реализует метод Иамклоккаджуст:: Сетклоккделта.'
ms.assetid: 2bb9266f-3866-4b2e-92a8-cde31a501047
title: Ксистемклокк. Сетклоккделта, метод (Сисклокк. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSystemClock.SetClockDelta
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cc1027081cc8713cffd2979e20627c037d0799f9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105656889"
---
# <a name="csystemclocksetclockdelta-method"></a>Ксистемклокк. Сетклоккделта, метод

`SetClockDelta`Метод корректирует время. Этот метод реализует метод [**иамклоккаджуст:: сетклоккделта**](/windows/desktop/api/Strmif/nf-strmif-iamclockadjust-setclockdelta) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT SetClockDelta(
   REFERENCE_TIME rtDelta
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ртделта* 
</dt> <dd>

Указывает величину, на которую следует отрегулировать часы, как [**значение \_ времени ссылки**](reference-time.md) . Положительное значение перемещает часы вперед, а отрицательное значение перемещает часы назад.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение S \_ ОК или код ошибки **HRESULT** .

## <a name="remarks"></a>Комментарии

Этот метод просто вызывает [**кбасереференцеклокк:: сеттимеделта**](cbasereferenceclock-settimedelta.md).

Значения времени, возвращаемые функцией [**иреференцеклокк:: OnTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-gettime) , монотонно увеличиваются. Если вы установили часы обратно, **время** будет продолжать сообщать о старом времени до тех пор, пока внутренняя синхронизация не завершится.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Версия<br/> | Класс Ксистемклокк<br/>                                                                                                                                                              |
| Header<br/>  | <dl> <dt>Сисклокк. h (включение Streams. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



 

 




