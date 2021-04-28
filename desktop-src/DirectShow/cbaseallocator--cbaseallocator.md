---
description: Метод деструктора Кбасеаллокатор. ~ Кбасеаллокатор.
ms.assetid: b1e5653f-d72f-4cde-a8c9-d25763434374
title: Деструктор Кбасеаллокатор. ~ Кбасеаллокатор (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.~CBaseAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9a4b754c8937b87a547f4583b3270f5782a6a415
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096422"
---
# <a name="cbaseallocatorcbaseallocator-destructor"></a>Деструктор Кбасеаллокатор. ~ Кбасеаллокатор

Метод деструктора.

## <a name="syntax"></a>Синтаксис


```C++
~CBaseAllocator();
```



## <a name="remarks"></a>Remarks

Всегда вызывайте метод [**кбасеаллокатор::D екоммит**](cbaseallocator-decommit.md) перед уничтожением объекта. Деструктор базового класса не может вызвать метод **uncommit**, так как этот метод вызывает чистый виртуальный метод [**Кбасеаллокатор:: Free**](cbaseallocator-free.md). Производные классы должны переопределять этот деструктор и вызывать метод **uncommit**.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Амфилтер. h (включение Streams. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Кбасеаллокатор**](cbaseallocator.md)
</dt> </dl>

 

 




