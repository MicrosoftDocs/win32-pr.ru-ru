---
description: Метод Stopped определяет, остановлен ли фильтр, содержащий этот ПИН-код.
ms.assetid: ffeac352-2f9b-44be-a8e8-7e9238d0b18e
title: Метод Кбасепин. Stopped (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.IsStopped
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 64e833ef495ace41a9dcd1614b69e4a081befce0e429fa7aad800a73ce490439
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119916394"
---
# <a name="cbasepinisstopped-method"></a>Кбасепин. метод Stopped

`IsStopped`Метод определяет, остановлен ли фильтр, содержащий этот ПИН-код.

## <a name="syntax"></a>Синтаксис


```C++
BOOL IsStopped();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение true** , если фильтр остановлен. В противном случае возвращает **значение false**.

## <a name="remarks"></a>Remarks

Не вызывайте этот метод из в методе конструктора **кбасепин** , так как фильтр, возможно, еще не инициализирован.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>амфилтер. h (включает Потоки. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Кбасепин**](cbasepin.md)
</dt> </dl>

 

 




