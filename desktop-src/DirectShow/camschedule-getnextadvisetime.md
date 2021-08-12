---
description: Метод Жетнекстадвисетиме извлекает время следующего запроса Advise.
ms.assetid: 2a376250-fb39-46d7-a5a8-e3a3143cd209
title: Камсчедуле. Жетнекстадвисетиме, метод (Дссчедуле. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMSchedule.GetNextAdviseTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6c7fd04622a5cdab8bade32f41b090d8f480db292209d284804b5180134954f4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118662350"
---
# <a name="camschedulegetnextadvisetime-method"></a>Камсчедуле. Жетнекстадвисетиме, метод

`GetNextAdviseTime`Метод извлекает время следующего запроса на выadvise.

## <a name="syntax"></a>Синтаксис


```C++
REFERENCE_TIME GetNextAdviseTime();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Возвращает время ссылки следующего запроса на выходе или максимальное время, в \_ течение которого запросы не планируются.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>дссчедуле. h (включает Потоки. h)</dt> </dl>                                                                                |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Камсчедуле**](camschedule.md)
</dt> </dl>

 

 




