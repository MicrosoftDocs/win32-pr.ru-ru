---
description: Метод деструктора Кмемаллокатор. ~ Кмемаллокатор.
ms.assetid: e0a04d93-fb77-4dc1-9bc8-7d3965bc6803
title: Деструктор Кмемаллокатор. ~ Кмемаллокатор (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMemAllocator.~CMemAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 588b370fc56f6af547ead19c7a52758a3851dd7e46d88b90f8f621ed6002d6e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118954383"
---
# <a name="cmemallocatorcmemallocator-destructor"></a>Деструктор Кмемаллокатор. ~ Кмемаллокатор

Метод деструктора.

## <a name="syntax"></a>Синтаксис


```C++
~CMemAllocator();
```



## <a name="remarks"></a>Remarks

Этот метод переопределяет деструктор базового класса для вызова [**кбасеаллокатор::D екоммит**](cbaseallocator-decommit.md) и [**Кмемаллокатор:: реаллифри**](cmemallocator-reallyfree.md).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>амфилтер. h (включает Потоки. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Кмемаллокатор**](cmemallocator.md)
</dt> </dl>

 

 




