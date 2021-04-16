---
description: Префикс каждого буфера в байтах.
ms.assetid: 471b73bf-f959-41aa-84ba-324a2738dd0e
title: 'Элемент Кбасеаллокатор:: m_lPrefix (Амфилтер. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_lPrefix
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fc52db44dcdfa050cf8bc7faf57cb7094d8cac91
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657047"
---
# <a name="cbaseallocatorm_lprefix-member"></a>Элемент Кбасеаллокатор:: m \_ лпрефикс

Префикс каждого буфера в байтах. Если значение не равно нулю, то каждый указатель буфера, возвращенный методом [**кбасеаллокатор::**](cbaseallocator-getbuffer.md) GetBytes, предшествует блоку байтов размером *m \_ лпрефикс*. Этот блок памяти называется *префиксом*. Переменная члена [**кбасеаллокатор:: m \_ лсизе**](cbaseallocator-m-lsize.md) не включает значение префикса.

## <a name="syntax"></a>Синтаксис


```C++
long m_lPrefix;
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

 

 




