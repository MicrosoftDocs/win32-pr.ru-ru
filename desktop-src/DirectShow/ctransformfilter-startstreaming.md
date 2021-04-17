---
description: Метод Стартстреаминг вызывается, когда фильтр переключается в состояние паузы.
ms.assetid: 1e3bbca7-b5b1-41fd-8f70-b7ef39c9491b
title: Ктрансформфилтер. Стартстреаминг, метод (Трансфрм. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.StartStreaming
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 50df2db2aada7f96744af5e553f474818594d399
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657744"
---
# <a name="ctransformfilterstartstreaming-method"></a>Ктрансформфилтер. Стартстреаминг, метод

`StartStreaming`Метод вызывается, когда фильтр переключается в состояние паузы.

## <a name="syntax"></a>Синтаксис


```C++
virtual HRESULT StartStreaming();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение S \_ ОК.

## <a name="remarks"></a>Комментарии

Этот метод не выполняет никаких действий в базовом классе, но производный класс может его переопределить.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Трансфрм. h (включение Streams. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Ктрансформфилтер**](ctransformfilter.md)
</dt> </dl>

 

 




