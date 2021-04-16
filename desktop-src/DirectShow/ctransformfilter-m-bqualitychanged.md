---
description: Флаг, указывающий, изменилось ли качество.
ms.assetid: 9084ab1d-b6a0-4e87-a653-86e64c74b07f
title: 'Элемент Ктрансформфилтер:: m_bQualityChanged (Трансфрм. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bQualityChanged
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: abd0371389d6c17a074580643a06c3fe25bdf433
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679643"
---
# <a name="ctransformfilterm_bqualitychanged-member"></a>Элемент Ктрансформфилтер:: m \_ бкуалитичанжед

Флаг, указывающий, изменилось ли качество. В первый раз при удалении образца фильтр отправляет событие [**EC об \_ \_ изменении качества**](ec-quality-change.md) в Диспетчер графа фильтров и устанавливает для этого флага **значение true**. Он не отправляет это событие повторно, пока фильтр не остановится и не перезапускается, даже если он продолжит удалять образцы.

## <a name="syntax"></a>Синтаксис


```C++
BOOL m_bQualityChanged;
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Трансфрм. h (включение Streams. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Ктрансформфилтер**](ctransformfilter.md)
</dt> </dl>

 

 




