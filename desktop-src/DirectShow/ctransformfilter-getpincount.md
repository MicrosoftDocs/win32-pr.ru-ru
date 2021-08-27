---
description: Метод Жетпинкаунт извлекает количество ПИН-кодов в фильтре.
ms.assetid: 29039ada-fccd-4890-b36b-3dd5c0bbdc3e
title: Ктрансформфилтер. Жетпинкаунт, метод (Трансфрм. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.GetPinCount
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ac9269149d7f2bbc95e811515f70aa279a4aafd8cf34b2d5077ed69019b86c2d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118953603"
---
# <a name="ctransformfiltergetpincount-method"></a>Ктрансформфилтер. Жетпинкаунт, метод

`GetPinCount`Метод извлекает количество ПИН-кодов в фильтре.

## <a name="syntax"></a>Синтаксис


```C++
virtual int GetPinCount();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение 2.

## <a name="remarks"></a>Remarks

Этот метод переопределяет метод [**кбасефилтер:: жетпинкаунт**](cbasefilter-getpincount.md) . Класс **ктрансформфилтер** поддерживает ровно один входной ПИН-код и один выходной ПИН-код.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>трансфрм. h (включает Потоки. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Ктрансформфилтер**](ctransformfilter.md)
</dt> </dl>

 

 




