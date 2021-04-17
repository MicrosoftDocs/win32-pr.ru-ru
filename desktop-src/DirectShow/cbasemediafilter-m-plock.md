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
ms.openlocfilehash: 126aa213004dd032eea43b28198b6f8b49fe7f3e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657659"
---
# <a name="cbasemediafilterm_plock-member"></a>Элемент Кбасемедиафилтер:: m \_ плокк

Указатель на критическую секцию.

## <a name="syntax"></a>Синтаксис


```C++
CCritSec *m_pLock;
```



## <a name="remarks"></a>Примечания

Критическая секция удерживается во время переходов между состояниями ([**кбасемедиафилтер:: Run**](cbasemediafilter-run.md), [**кбасемедиафилтер::P Аусе**](cbasemediafilter-pause.md), [**кбасемедиафилтер:: останавливаются**](cbasemediafilter-stop.md)) при доступе к эталонному времени ([**кбасемедиафилтер:: сетсинксаурце**](cbasemediafilter-setsyncsource.md), [**CBaseMediaFilter:: GetSyncSource**](cbasemediafilter-getsyncsource.md)) и в методе [**CBaseMediaFilter::**](cbasemediafilter-isactive.md) IsReference.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Амфилтер. h (включение Streams. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасемедиафилтер**](cbasemediafilter.md)
</dt> </dl>

 

 




