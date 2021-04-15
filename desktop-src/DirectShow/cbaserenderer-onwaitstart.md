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
ms.openlocfilehash: c2f88f11e370c6d1962ae6076f4c8f5eecc31407
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669405"
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

## <a name="remarks"></a>Комментарии

Метод [**кбасерендерер:: ваитфоррендертиме**](cbaserenderer-waitforrendertime.md) вызывает этот метод, когда он начинает ожидание времени презентации в примере. Этот метод не выполняет никаких действий в базовом классе, но производный класс может его переопределить.

Если вы реализуете контроль качества, вы можете переопределить этот метод вместе с методом [**кбасерендерер:: онваитенд**](cbaserenderer-onwaitend.md) . Эти методы можно использовать для наблюдения за производительностью фильтра.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ренбасе. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасерендерер**](cbaserenderer.md)
</dt> </dl>

 

 




