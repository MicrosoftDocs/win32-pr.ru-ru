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
ms.openlocfilehash: 6482aac80c1298ea403019f43ddc4effdc30b00a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657045"
---
# <a name="cbasewindowm_hinstance-member"></a>Элемент Кбасевиндов:: m \_ HINSTANCE

Обработчик для экземпляра модуля.

## <a name="syntax"></a>Синтаксис


```C++
HINSTANCE m_hInstance;
```



## <a name="remarks"></a>Примечания

Функция точки входа библиотеки DLL задает глобальную переменную с помощью маркера экземпляра модуля. Класс **кбасевиндов** сохраняет этот обработчик в своем методе конструктора.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Винутил. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасевиндов**](cbasewindow.md)
</dt> </dl>

 

 




