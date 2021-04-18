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
ms.openlocfilehash: 16ab469db1d50007bd3aa55ab692c51aa7600452
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657600"
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
| Header<br/>  | <dl> <dt>Амфилтер. h (включение Streams. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасеаллокатор**](cbaseallocator.md)
</dt> </dl>

 

 




