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
ms.openlocfilehash: ba1d2046bf7be31a9c0d3f3d43b13aeeffd1f76b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657758"
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

## <a name="remarks"></a>Комментарии

Этот метод переопределяет метод [**кбасефилтер:: жетпинкаунт**](cbasefilter-getpincount.md) . Класс **ктрансформфилтер** поддерживает ровно один входной ПИН-код и один выходной ПИН-код.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Трансфрм. h (включение Streams. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Ктрансформфилтер**](ctransformfilter.md)
</dt> </dl>

 

 




