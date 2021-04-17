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
ms.openlocfilehash: a3ed93a4612d8fa5d4fe79239c6a7f4f5e479717
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657649"
---
# <a name="cvideotransformfilterm_itrlate-member"></a>Элемент Квидеотрансформфилтер:: m \_ итрлате

Указывает, насколько поздние образцы поступают в модуль подготовки отчетов в ссылочных единицах времени. Синтаксис

## <a name="syntax"></a>Синтаксис


```C++
int m_itrLate;
```



## <a name="remarks"></a>Примечания

Когда фильтр получает сообщение о качестве подчиненного, он сохраняет значение просрочки в этой переменной. Поскольку фильтр удаляет кадры, он обновляет это значение, вычитая продолжительность каждого кадра.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Втранс. h (включение Streams. h)</dt> </dl>                                                                                    |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Квидеотрансформфилтер**](cvideotransformfilter.md)
</dt> </dl>

 

 




