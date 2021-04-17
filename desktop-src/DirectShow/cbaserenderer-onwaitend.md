---
description: Метод Онваитенд вызывается, когда фильтр выполняется в ожидании времени презентации в примере.
ms.assetid: 47ff8f79-da69-4dcf-8cbb-02c1b56e382e
title: Кбасерендерер. Онваитенд, метод (Ренбасе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.OnWaitEnd
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a5a290ad5d39fc83a4213d1c8a32119b4caa9858
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669406"
---
# <a name="cbaserendereronwaitend-method"></a>Кбасерендерер. Онваитенд, метод

`OnWaitEnd`Метод вызывается, когда фильтр выполняется в ожидании времени презентации в примере.

## <a name="syntax"></a>Синтаксис


```C++
virtual void OnWaitEnd();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Комментарии

Метод [**кбасерендерер:: ваитфоррендертиме**](cbaserenderer-waitforrendertime.md) вызывает этот метод, когда он завершает ожидание времени презентации в примере. Этот метод не выполняет никаких действий в базовом классе, но производный класс может его переопределить.

Если вы реализуете контроль качества, вы можете переопределить этот метод вместе с методом [**кбасерендерер:: онваитстарт**](cbaserenderer-onwaitstart.md) . Эти методы можно использовать для наблюдения за производительностью фильтра.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ренбасе. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасерендерер**](cbaserenderer.md)
</dt> </dl>

 

 




