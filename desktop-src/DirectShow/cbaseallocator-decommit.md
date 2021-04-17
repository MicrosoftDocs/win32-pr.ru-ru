---
description: Метод uncommit отменяет выделение распределителя. Этот метод реализует метод Имемаллокатор::D екоммит.
ms.assetid: 0c8d44e0-17ea-4f7f-be44-f9ae2e34fbef
title: Метод Кбасеаллокатор. uncommit (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.Decommit
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 613af805f1c04a7bf375755ff8f3adba7b70be18
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657341"
---
# <a name="cbaseallocatordecommit-method"></a>Кбасеаллокатор. uncommit, метод

Метод отменяет `Decommit` выделение распределителя. Этот метод реализует метод [**имемаллокатор::D екоммит**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-decommit) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT Decommit();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение S \_ ОК.

## <a name="remarks"></a>Комментарии

После вызова этого метода вызовы метода [**кбасеаллокатор::-buffer**](cbaseallocator-getbuffer.md) завершатся ошибкой. После выпуска образцов они возвращаются в бесплатный список. Когда возвращается последняя выборка, распределитель вызывает метод [**кбасеаллокатор:: Free**](cbaseallocator-free.md) , который освобождает выделенную память. (В базовом классе **Free** является чисто виртуальным методом.)

Кроме того, этот метод освобождает все потоки, заблокированные в вызовах метода **buffer** . Вызовы метода " **buffer** " завершаются ошибкой.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Амфилтер. h (включение Streams. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасеаллокатор**](cbaseallocator.md)
</dt> </dl>

 

 




