---
description: 'Метод Стартстреаминг вызывается, когда фильтр переключается в состояние паузы. Этот метод переопределяет метод Ктрансформфилтер:: Стартстреаминг.'
ms.assetid: fa05f88f-fed8-479d-b0b4-d9df982d51e7
title: Квидеотрансформфилтер. Стартстреаминг, метод (Втранс. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CVideoTransformFilter.StartStreaming
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5ae8d49401389830f9d5dbf0ec91e7f390c51ca6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675035"
---
# <a name="cvideotransformfilterstartstreaming-method"></a>Квидеотрансформфилтер. Стартстреаминг, метод

`StartStreaming`Метод вызывается, когда фильтр переключается в состояние паузы. Этот метод переопределяет метод [**ктрансформфилтер:: стартстреаминг**](ctransformfilter-startstreaming.md) .

## <a name="syntax"></a>Синтаксис


```C++
virtual HRESULT StartStreaming();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение S \_ ОК.

## <a name="remarks"></a>Комментарии

Этот метод сбрасывает всю статистику производительности.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Втранс. h (включение Streams. h)</dt> </dl>                                                                                    |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Квидеотрансформфилтер**](cvideotransformfilter.md)
</dt> </dl>

 

 




