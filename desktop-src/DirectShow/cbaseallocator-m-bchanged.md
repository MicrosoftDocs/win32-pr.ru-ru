---
description: Флаг, указывающий, изменились ли требования к буферу.
ms.assetid: 34d946f9-125c-40fb-b09e-82457add07d6
title: 'Элемент Кбасеаллокатор:: m_bChanged (Амфилтер. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bChanged
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7edb5ed770628d7dfd982017e720ef0136bace74dd7e311121925f6c8657d2fe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120131504"
---
# <a name="cbaseallocatorm_bchanged-member"></a>Элемент Кбасеаллокатор:: m \_ бчанжед

Флаг, указывающий, изменились ли требования к буферу. Метод [**кбасеаллокатор:: SetProperties**](cbaseallocator-setproperties.md) устанавливает значение **true**. В производном классе чистый виртуальный метод [**кбасеаллокатор:: Alloc**](cbaseallocator-alloc.md) должен вернуть значение **false**. После выделения буферов нет необходимости их повторного выделения, пока *m \_ Бчанжед* имеет **значение false**.

## <a name="syntax"></a>Синтаксис


```C++
BOOL m_bChanged;
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>амфилтер. h (включает Потоки. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Кбасеаллокатор**](cbaseallocator.md)
</dt> </dl>

 

 




