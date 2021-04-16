---
description: Метод TimerCallback является методом обратного вызова для события таймера конца потока.
ms.assetid: ed43d07a-1ece-43ab-8753-ab14fa388946
title: Кбасерендерер. TimerCallback, метод (Ренбасе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.TimerCallback
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cfa59ca6bed0539caa7eb650458c168999b0de5a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657987"
---
# <a name="cbaserenderertimercallback-method"></a>Кбасерендерер. TimerCallback, метод

`TimerCallback`Метод является методом обратного вызова для события конца потока.

## <a name="syntax"></a>Синтаксис


```C++
void TimerCallback();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Комментарии

Метод [**кбасерендерер:: сендендофстреам**](cbaserenderer-sendendofstream.md) использует событие Timer для планирования \_ уведомлений о завершении EC. Метод **кбасерендерер:: TimerCallback** является функцией обратного вызова для события таймера. `TimerCallback`Метод вызывает **сендендофстреам** еще раз, и **сендендофстреам** определяет, следует ли отправить \_ уведомление о завершении EC или задать другой таймер.

Метод [**кбасерендерер:: ресетендофстреамтимер**](cbaserenderer-resetendofstreamtimer.md) отменяет событие таймера.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ренбасе. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасерендерер**](cbaserenderer.md)
</dt> </dl>

 

 




