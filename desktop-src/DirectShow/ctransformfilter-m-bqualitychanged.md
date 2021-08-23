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
ms.openlocfilehash: 454d8bad4ced2291b061b09992ad450d9e483f269e3fd72b192adbbacb077d7c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118953613"
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
| Заголовок<br/>  | <dl> <dt>трансфрм. h (включает Потоки. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Ктрансформфилтер**](ctransformfilter.md)
</dt> </dl>

 

 




