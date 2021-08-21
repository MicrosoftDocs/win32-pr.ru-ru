---
description: 'Метод Ендфлуш завершает операцию очистки. Этот метод переопределяет метод Ктрансформфилтер:: Ендфлуш.'
ms.assetid: e7dfc6f9-1630-426b-95b2-9814331b5e61
title: Квидеотрансформфилтер. Ендфлуш, метод (Втранс. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CVideoTransformFilter.EndFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 359229e690715667d7bbfbe3d3a9134f41f5af9febc185885e08cde7d986896e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118155878"
---
# <a name="cvideotransformfilterendflush-method"></a>Квидеотрансформфилтер. Ендфлуш, метод

`EndFlush`Метод завершает операцию очистки. Этот метод переопределяет метод [**ктрансформфилтер:: ендфлуш**](ctransformfilter-endflush.md) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT EndFlush();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение \_ ОК, если успешно, или код ошибки.

## <a name="remarks"></a>Remarks

Этот метод сбрасывает все внутренние измерения производительности фильтра.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>втранс. h (включает Потоки. h)</dt> </dl>                                                                                    |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Квидеотрансформфилтер**](cvideotransformfilter.md)
</dt> </dl>

 

 




