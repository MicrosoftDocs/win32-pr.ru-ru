---
description: Метод Ресетстреамингтимес сбрасывает все значения времени, которые управляют потоковой передачей.
ms.assetid: 8a596760-a45a-4486-bb91-aab10bbf927f
title: Кбасевидеорендерер. Ресетстреамингтимес, метод (Ренбасе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.ResetStreamingTimes
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: bebf6f827cac883660b383b76f3a6ead7987e9fb468d0fd6f14205f59ad4d530
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119074778"
---
# <a name="cbasevideorendererresetstreamingtimes-method"></a>Кбасевидеорендерер. Ресетстреамингтимес, метод

`ResetStreamingTimes`Метод сбрасывает все значения времени, которые управляют потоковой передачей.

## <a name="syntax"></a>Синтаксис


```C++
virtual HRESULT ResetStreamingTimes();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение **HRESULT** .

## <a name="remarks"></a>Remarks

Время задается таким образом, чтобы фреймы не удалялись изначально, а первый кадр был нарисован.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>ренбасе. h (включает Потоки. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Кбасевидеорендерер**](cbasevideorenderer.md)
</dt> </dl>

 

 




