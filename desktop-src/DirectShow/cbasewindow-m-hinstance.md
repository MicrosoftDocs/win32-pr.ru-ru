---
description: Обработчик для экземпляра модуля.
ms.assetid: ad889ebe-2bd8-4456-9517-9e2909697a02
title: 'Элемент Кбасевиндов:: m_hInstance (Винутил. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_hInstance
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ddf1da2d7f947bbaed9972a40a20497a81f84ebda68dba31cd5518b64f6e8434
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119016532"
---
# <a name="cbasewindowm_hinstance-member"></a>Элемент Кбасевиндов:: m \_ HINSTANCE

Обработчик для экземпляра модуля.

## <a name="syntax"></a>Синтаксис


```C++
HINSTANCE m_hInstance;
```



## <a name="remarks"></a>Remarks

Функция точки входа библиотеки DLL задает глобальную переменную с помощью маркера экземпляра модуля. Класс **кбасевиндов** сохраняет этот обработчик в своем методе конструктора.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>винутил. h (включает Потоки. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасевиндов**](cbasewindow.md)
</dt> </dl>

 

 




