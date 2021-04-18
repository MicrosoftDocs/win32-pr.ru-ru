---
description: Метод Онваитстарт обновляет время, потраченное на ожидание и неожидание.
ms.assetid: 3f2e2bf2-f205-4b59-b969-cf8c2136437d
title: Кбасевидеорендерер. Онваитстарт, метод (Ренбасе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.OnWaitStart
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d4fab7e1a1f24c3d00f46018db9478990be71666
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675008"
---
# <a name="cbasevideorendereronwaitstart-method"></a>Кбасевидеорендерер. Онваитстарт, метод

`OnWaitStart`Метод обновляет время, затраченное на ожидание и неожидание.

## <a name="syntax"></a>Синтаксис


```C++
void OnWaitStart();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Комментарии

Эта функция-член вызывается, когда начинается ожидание события отрисовки. Он используется только для измерения производительности.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ренбасе. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасевидеорендерер**](cbasevideorenderer.md)
</dt> </dl>

 

 




