---
description: Метод Стопстреаминг вызывается, когда фильтр переключается в состояние Stopped.
ms.assetid: cfebfed2-4105-4dea-8d47-60d6160ee337
title: Ктрансформфилтер. Стопстреаминг, метод (Трансфрм. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.StopStreaming
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4990b55ad87a4eb754af7101e762ce227a090993
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657609"
---
# <a name="ctransformfilterstopstreaming-method"></a>Ктрансформфилтер. Стопстреаминг, метод

`StopStreaming`Метод вызывается, когда фильтр переключается в состояние Stopped.

## <a name="syntax"></a>Синтаксис


```C++
virtual HRESULT StopStreaming();
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

 

 




