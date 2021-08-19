---
description: Метод Онваитстарт вызывается, когда фильтр начинает ожидание времени презентации в примере.
ms.assetid: 598cd676-3afe-4ec9-ae38-83971412e6a7
title: Кбасерендерер. Онваитстарт, метод (Ренбасе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.OnWaitStart
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: eaad14d0eec765a0ad12693c0a1eee67386bc9bb26344ee52c29224d129edf5c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117822651"
---
# <a name="cbaserendereronwaitstart-method"></a>Кбасерендерер. Онваитстарт, метод

`OnWaitStart`Метод вызывается, когда фильтр начинает ожидание времени презентации в примере.

## <a name="syntax"></a>Синтаксис


```C++
virtual void OnWaitStart();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Remarks

Метод [**кбасерендерер:: ваитфоррендертиме**](cbaserenderer-waitforrendertime.md) вызывает этот метод, когда он начинает ожидание времени презентации в примере. Этот метод не выполняет никаких действий в базовом классе, но производный класс может его переопределить.

Если вы реализуете контроль качества, вы можете переопределить этот метод вместе с методом [**кбасерендерер:: онваитенд**](cbaserenderer-onwaitend.md) . Эти методы можно использовать для наблюдения за производительностью фильтра.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>ренбасе. h (включает Потоки. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Кбасерендерер**](cbaserenderer.md)
</dt> </dl>

 

 




