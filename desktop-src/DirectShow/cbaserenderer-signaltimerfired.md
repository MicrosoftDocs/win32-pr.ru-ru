---
description: Метод Сигналтимерфиред очищает идентификатор таймера, используемый для планирования подготовки к просмотру.
ms.assetid: b8ae362e-fcda-4888-be32-8fb910d0f0db
title: Кбасерендерер. Сигналтимерфиред, метод (Ренбасе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.SignalTimerFired
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f08ed0e8348648d5d1af1127159b414b0ddbc40cfd470ff0834b7bc2b0723e9b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120052364"
---
# <a name="cbaserenderersignaltimerfired-method"></a>Кбасерендерер. Сигналтимерфиред, метод

`SignalTimerFired`Метод очищает идентификатор таймера, используемый для планирования подготовки к просмотру.

## <a name="syntax"></a>Синтаксис


```C++
virtual void SignalTimerFired();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Remarks

Фильтр вызывает этот метод, когда таймер отрисовки активирует (см [**. кбасерендерер:: ваитфоррендертиме**](cbaserenderer-waitforrendertime.md)) или при отмене таймера (см. [**Кбасерендерер:: канцелнотификатион**](cbaserenderer-cancelnotification.md)). Метод сбрасывает переменную члена [**кбасерендерер:: m \_ двадвисе**](cbaserenderer-m-dwadvise.md) в нулевое значение.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>ренбасе. h (включает Потоки. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасерендерер**](cbaserenderer.md)
</dt> </dl>

 

 




