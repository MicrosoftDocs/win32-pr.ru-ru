---
description: Указывает, насколько поздние образцы поступают в модуль подготовки отчетов в ссылочных единицах времени. Syntax.
ms.assetid: 7b30fbe1-5e57-4aa4-8e87-ddd584f186e4
title: 'Элемент Квидеотрансформфилтер:: m_itrLate (Втранс. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_itrLate
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6ba2d14d19849768538184e54de5ca84b9495371783d57231ab9ad6aa7738718
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120075954"
---
# <a name="cvideotransformfilterm_itrlate-member"></a>Элемент Квидеотрансформфилтер:: m \_ итрлате

Указывает, насколько поздние образцы поступают в модуль подготовки отчетов в ссылочных единицах времени. Синтаксис

## <a name="syntax"></a>Синтаксис


```C++
int m_itrLate;
```



## <a name="remarks"></a>Remarks

Когда фильтр получает сообщение о качестве подчиненного, он сохраняет значение просрочки в этой переменной. Поскольку фильтр удаляет кадры, он обновляет это значение, вычитая продолжительность каждого кадра.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>втранс. h (включает Потоки. h)</dt> </dl>                                                                                    |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Квидеотрансформфилтер**](cvideotransformfilter.md)
</dt> </dl>

 

 




