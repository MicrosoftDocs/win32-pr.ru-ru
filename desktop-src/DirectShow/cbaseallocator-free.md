---
description: Метод Free освобождает всю буферную память. Этот метод вызывается, когда фильтр-владелец отменяет распределитель, после освобождения последнего примера носителя.
ms.assetid: dd1e6c4d-762a-4caf-902b-015c6c9fdb4d
title: Метод Кбасеаллокатор. Free (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.Free
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e77555094625bfc6a31a0527fc3223a124b012e72c28ea76e5774de289d63391
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119794214"
---
# <a name="cbaseallocatorfree-method"></a>Кбасеаллокатор. Free, метод

`Free`Метод освобождает всю буферную память. Этот метод вызывается, когда фильтр-владелец отменяет распределитель, после освобождения последнего примера носителя.

## <a name="syntax"></a>Синтаксис


```C++
virtual void Free() = 0;
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Remarks

После вызова метода [**uncommit**](cbaseallocator-decommit.md) распределитель вызывает этот метод при освобождении последнего примера носителя. Производный класс должен реализовывать этот метод.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>амфилтер. h (включает Потоки. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Кбасеаллокатор**](cbaseallocator.md)
</dt> </dl>

 

 




