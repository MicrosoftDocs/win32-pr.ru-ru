---
description: Метод Pause сигнализирует потоку потоковой передачи на активное выполнение.
ms.assetid: c97da113-c5a7-422d-9215-70b556e0b8ca
title: Метод Ксаурцестреам. Pause (Source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.Pause
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 454f6e64461c036e9e3d9ef2f13033e5a210d783f3f6b734b7137a99b16402c5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120079314"
---
# <a name="csourcestreampause-method"></a>Ксаурцестреам. Pause, метод

`Pause`Метод сигнализирует потоку потоковой передачи на активность.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT Pause();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Непредвиденное значение: S \_ (ОК или E) \_ .

## <a name="remarks"></a>Remarks

Метод [**ксаурцестреам:: Active**](csourcestream-active.md) вызывает этот метод. Когда метод [**ксаурцестреам:: среадпрок**](csourcestream-threadproc.md) получает этот запрос, он вызывает метод [**Ксаурцестреам::D обуфферпроцессинглуп**](csourcestream-dobufferprocessingloop.md) .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>Source. h (включает Потоки. h)</dt> </dl>                                                                                    |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Ксаурцестреам**](csourcestream.md)
</dt> </dl>

 

 




