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
ms.openlocfilehash: 89b87bd4e706e5270b49ca94d1c86a6c5a5326fd3efccb1dcc45b9681e6e2fca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119017562"
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
| Заголовок<br/>  | <dl> <dt>амфилтер. h (включает Потоки. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасеаллокатор**](cbaseallocator.md)
</dt> </dl>

 

 




