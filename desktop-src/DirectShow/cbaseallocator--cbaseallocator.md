---
description: Метод деструктора.
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
ms.openlocfilehash: 53587482c5d9cf8f5a772453f220c7633c17d383
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105656839"
---
# <a name="cbaseallocatorcbaseallocator-destructor"></a>Деструктор Кбасеаллокатор. ~ Кбасеаллокатор

Метод деструктора.

## <a name="syntax"></a>Синтаксис


```C++
~CBaseAllocator();
```



## <a name="remarks"></a>Примечания

Всегда вызывайте метод [**кбасеаллокатор::D екоммит**](cbaseallocator-decommit.md) перед уничтожением объекта. Деструктор базового класса не может вызвать метод **uncommit**, так как этот метод вызывает чистый виртуальный метод [**Кбасеаллокатор:: Free**](cbaseallocator-free.md). Производные классы должны переопределять этот деструктор и вызывать метод **uncommit**.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Амфилтер. h (включение Streams. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасеаллокатор**](cbaseallocator.md)
</dt> </dl>

 

 




