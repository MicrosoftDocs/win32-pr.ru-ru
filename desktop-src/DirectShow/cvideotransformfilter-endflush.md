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
ms.openlocfilehash: ca160bd2e3e66df3bcf6f293abe6f828309172c0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657651"
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

## <a name="remarks"></a>Комментарии

Этот метод сбрасывает все внутренние измерения производительности фильтра.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Втранс. h (включение Streams. h)</dt> </dl>                                                                                    |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Квидеотрансформфилтер**](cvideotransformfilter.md)
</dt> </dl>

 

 




