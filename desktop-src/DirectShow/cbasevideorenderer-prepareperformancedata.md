---
description: Метод Препареперформанцедата задает \_ значения m трлате и m \_ трфраме текущего кадра.
ms.assetid: c4c5701b-eccd-4259-a1d1-7c5000f6b2df
title: Кбасевидеорендерер. Препареперформанцедата, метод (Ренбасе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.PreparePerformanceData
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e8cb276b37e64b6bb34751ed2d034666f7ceeddd90d8e52e47b2a1fca499ff9a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118658338"
---
# <a name="cbasevideorendererprepareperformancedata-method"></a>Кбасевидеорендерер. Препареперформанцедата, метод

`PreparePerformanceData`Метод задает значения **m \_ трлате** и **m \_ трфраме** для текущего кадра.

## <a name="syntax"></a>Синтаксис


```C++
void PreparePerformanceData(
   int trLate,
   int trFrame
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*трлате* 
</dt> <dd>

Значение, указывающее, насколько поздно образец превысил время его выполнения в ссылочных единицах времени.

</dd> <dt>

*трфраме* 
</dt> <dd>

Время между кадрами, в ссылочных единицах времени.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Remarks

Эта функция члена устанавливает **m \_ трлате** в значение *трлате* и **m \_ трфраме** в значение *трфраме*.

Когда функция-член [**кбасевидеорендерер:: рекордфрамелатенесс**](cbasevideorenderer-recordframelateness.md) вызывается из [**Кбасевидеорендерер:: онрендерстарт**](cbasevideorenderer-onrenderstart.md) или [**кбасевидеорендерер:: OnDirectRender**](cbasevideorenderer-ondirectrender.md), она передает значения **m \_ trLate** и **m \_ trFrame** для обновления статистики. `PreparePerformanceData` вызывается из [**кбасевидеорендерер:: онваитенд**](cbasevideorenderer-onwaitend.md) для задания этих значений элементов данных.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>ренбасе. h (включает Потоки. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Кбасевидеорендерер**](cbasevideorenderer.md)
</dt> </dl>

 

 




