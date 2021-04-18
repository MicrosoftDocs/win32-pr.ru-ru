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
ms.openlocfilehash: 86c700f3c0ee820206613bcf3147652b1826b57a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669119"
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
| Header<br/>  | <dl> <dt>Амфилтер. h (включение Streams. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасеаллокатор**](cbaseallocator.md)
</dt> </dl>

 

 




