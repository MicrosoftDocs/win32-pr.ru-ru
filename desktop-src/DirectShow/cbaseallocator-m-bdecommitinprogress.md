---
description: Флаг, указывающий, выполняется ли операция дефиксации.
ms.assetid: aa008be1-8faa-4dc1-9641-37dcc59ce6c7
title: 'Элемент Кбасеаллокатор:: m_bDecommitInProgress (Амфилтер. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bDecommitInProgress
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d6d73514ffbe2b6e2430230e64ccfa9006809523a95cd3220ca078d4c4e40f41
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119017542"
---
# <a name="cbaseallocatorm_bdecommitinprogress-member"></a>Элемент Кбасеаллокатор:: m \_ бдекоммитинпрогресс

Флаг, указывающий, выполняется ли операция дефиксации. Значение равно **true** после вызова метода [**кбасеаллокатор::D екоммит**](cbaseallocator-decommit.md) , но до освобождения всех буферов. Если значение равно **true**, метод [**кбасеаллокатор::-buffer**](cbaseallocator-getbuffer.md) завершается ошибкой. Кроме того, распределитель не должен удалять себя, пока значение равно **true**.

## <a name="syntax"></a>Синтаксис


```C++
BOOL m_bDecommitInProgress;
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>амфилтер. h (включает Потоки. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасеаллокатор**](cbaseallocator.md)
</dt> </dl>

 

 




