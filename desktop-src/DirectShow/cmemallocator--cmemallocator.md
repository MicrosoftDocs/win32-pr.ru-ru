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
ms.openlocfilehash: 43b0505ee34df72ab82e4204b08440ac1a2558b5
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095412"
---
# <a name="cmemallocatorcmemallocator-destructor"></a>Деструктор Кмемаллокатор. ~ Кмемаллокатор

Метод деструктора.

## <a name="syntax"></a>Синтаксис


```C++
~CMemAllocator();
```



## <a name="remarks"></a>Remarks

Этот метод переопределяет деструктор базового класса для вызова [**кбасеаллокатор::D екоммит**](cbaseallocator-decommit.md) и [**Кмемаллокатор:: реаллифри**](cmemallocator-reallyfree.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Амфилтер. h (включение Streams. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Кмемаллокатор**](cmemallocator.md)
</dt> </dl>

 

 




