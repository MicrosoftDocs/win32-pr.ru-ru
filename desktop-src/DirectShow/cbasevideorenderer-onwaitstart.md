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
ms.openlocfilehash: f9bc3b895f27490377fd5de188b7cea8ccd429c55d36a5cdd0fea4ce025bac29
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119502604"
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

## <a name="remarks"></a>Remarks

Эта функция-член вызывается, когда начинается ожидание события отрисовки. Он используется только для измерения производительности.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>ренбасе. h (включает Потоки. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Кбасевидеорендерер**](cbasevideorenderer.md)
</dt> </dl>

 

 




