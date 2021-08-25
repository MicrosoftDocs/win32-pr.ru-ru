---
description: Указатель на критическую секцию.
ms.assetid: 7d949b7f-a6a7-4ab5-b651-f85b70d55065
title: 'Элемент Кбасемедиафилтер:: m_pLock (Амфилтер. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_pLock
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ad92cf07cc096c50ffa50f862c26f6133fc8dbb9b9b059419bb516e07cbd5daa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119910794"
---
# <a name="cbasemediafilterm_plock-member"></a>Элемент Кбасемедиафилтер:: m \_ плокк

Указатель на критическую секцию.

## <a name="syntax"></a>Синтаксис


```C++
CCritSec *m_pLock;
```



## <a name="remarks"></a>Remarks

Критическая секция удерживается во время переходов между состояниями ([**кбасемедиафилтер:: Run**](cbasemediafilter-run.md), [**кбасемедиафилтер::P Аусе**](cbasemediafilter-pause.md), [**кбасемедиафилтер:: останавливаются**](cbasemediafilter-stop.md)) при доступе к эталонному времени ([**кбасемедиафилтер:: сетсинксаурце**](cbasemediafilter-setsyncsource.md), [**CBaseMediaFilter:: GetSyncSource**](cbasemediafilter-getsyncsource.md)) и в методе [**CBaseMediaFilter::**](cbasemediafilter-isactive.md) IsReference.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>амфилтер. h (включает Потоки. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасемедиафилтер**](cbasemediafilter.md)
</dt> </dl>

 

 




