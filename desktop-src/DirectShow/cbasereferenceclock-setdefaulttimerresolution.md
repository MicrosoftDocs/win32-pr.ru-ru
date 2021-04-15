---
description: Метод Сетдефаулттимерресолутион задает разрешение таймера ссылочного времени.
ms.assetid: 891b809a-15d3-41f3-853e-aca9ddcd56e8
title: Кбасереференцеклокк. Сетдефаулттимерресолутион, метод (Рефклокк. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseReferenceClock.SetDefaultTimerResolution
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 146162784ad52a7f7930613ec5c648e40d22900f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669199"
---
# <a name="cbasereferenceclocksetdefaulttimerresolution-method"></a>Кбасереференцеклокк. Сетдефаулттимерресолутион, метод

`SetDefaultTimerResolution`Метод задает разрешение таймера ссылочного времени.

## <a name="syntax"></a>Синтаксис


```C++
STDMETHODIMP SetDefaultTimerResolution(
   REFERENCE_TIME timerResolution
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*тимерресолутион* 
</dt> <dd>

Минимальное разрешение таймера (в 100-наносекундных единицах). Если значение равно нулю, то контрольный таймер отменяет предыдущий запрос.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение **HRESULT** .

## <a name="remarks"></a>Комментарии

Этот метод реализует метод [**иреференцеклокктимерконтрол:: сетдефаулттимерресолутион**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclocktimercontrol-setdefaulttimerresolution) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Рефклокк. h (включение Streams. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасереференцеклокк**](cbasereferenceclock.md)
</dt> </dl>

 

 




