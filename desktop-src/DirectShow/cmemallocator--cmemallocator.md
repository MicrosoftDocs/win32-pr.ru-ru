---
description: Метод деструктора.
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
ms.openlocfilehash: d49046eccd8d7ef71c4eeb4c75acffbf90f7d826
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665499"
---
# <a name="cmemallocatorcmemallocator-destructor"></a>Деструктор Кмемаллокатор. ~ Кмемаллокатор

Метод деструктора.

## <a name="syntax"></a>Синтаксис


```C++
~CMemAllocator();
```



## <a name="remarks"></a>Примечания

Этот метод переопределяет деструктор базового класса для вызова [**кбасеаллокатор::D екоммит**](cbaseallocator-decommit.md) и [**Кмемаллокатор:: реаллифри**](cmemallocator-reallyfree.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Амфилтер. h (включение Streams. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кмемаллокатор**](cmemallocator.md)
</dt> </dl>

 

 




