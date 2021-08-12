---
description: Количество буферов для предоставления.
ms.assetid: 73f87b14-4346-4909-bd1e-c4981cde403d
title: 'Элемент Кбасеаллокатор:: m_lCount (Амфилтер. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_lCount
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c33749ee6293c301501962939e25118595db10592713fb46dc10d01083c0096f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118661696"
---
# <a name="cbaseallocatorm_lcount-member"></a>Элемент Кбасеаллокатор:: m \_ lCount

Количество буферов для предоставления. Это значение задается методом [**кбасеаллокатор:: SetProperties**](cbaseallocator-setproperties.md) . Буферы не выделяются, пока не будет вызван метод [**кбасеаллокатор:: Commit**](cbaseallocator-commit.md) . Текущее число выделенных буферов задается переменной-членом [**кбасеаллокатор:: m \_ лаллокатед**](cbaseallocator-m-lallocated.md) .

## <a name="syntax"></a>Синтаксис


```C++
long m_lCount;
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

 

 




