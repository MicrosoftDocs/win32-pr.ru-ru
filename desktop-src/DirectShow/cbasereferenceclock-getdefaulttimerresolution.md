---
description: Метод Жетдефаулттимерресолутион возвращает текущее разрешение таймера ссылочного времени.
ms.assetid: 14176f9c-7fa1-47f6-a261-9c66e271a3f2
title: Кбасереференцеклокк. Жетдефаулттимерресолутион, метод (Рефклокк. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseReferenceClock.GetDefaultTimerResolution
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 40a1c430f95b13086d50811e63cc2e411b3bf377
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657311"
---
# <a name="cbasereferenceclockgetdefaulttimerresolution-method"></a>Кбасереференцеклокк. Жетдефаулттимерресолутион, метод

`GetDefaultTimerResolution`Метод возвращает текущее разрешение таймера ссылочного времени.

## <a name="syntax"></a>Синтаксис


```C++
STDMETHODIMP GetDefaultTimerResolution(
   REFERENCE_TIME *pTimerResolution
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*птимерресолутион* 
</dt> <dd>

Получает запрошенное разрешение таймера в единицах 100-наносекундных.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение **HRESULT** .

## <a name="remarks"></a>Комментарии

Этот метод реализует метод [**иреференцеклокктимерконтрол:: жетдефаулттимерресолутион**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclocktimercontrol-getdefaulttimerresolution) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Рефклокк. h (включение Streams. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасереференцеклокк**](cbasereferenceclock.md)
</dt> </dl>

 

 




