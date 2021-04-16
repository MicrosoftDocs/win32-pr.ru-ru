---
description: Указатель на критическую секцию, используемый для сериализации изменений состояния.
ms.assetid: 4fecd9a6-54df-49d7-bf2f-5dcaef919ad7
title: 'Элемент Кбасефилтер:: m_pLock (Амфилтер. h)'
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
ms.openlocfilehash: 40b2f6ece048fc6463fda0a22792d57839d59e55
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657183"
---
# <a name="cbasefilterm_plock-member"></a>Элемент Кбасефилтер:: m \_ плокк

Указатель на критическую секцию, используемый для сериализации изменений состояния.

## <a name="syntax"></a>Синтаксис


```C++
CCritSec *m_pLock;
```



## <a name="remarks"></a>Примечания

Эта переменная инициализируется в конструкторе класса. см. раздел [**кбасефилтер:: кбасефилтер**](cbasefilter-cbasefilter.md).

Держите этот критический раздел во время переходов между состояниями или когда метод обращается к состоянию за несколько операций. Базовый класс содержит критическую секцию в следующих методах:

-   [**Кбасефилтер:: Финдпин**](cbasefilter-findpin.md)
-   [**Кбасефилтер:: Жетсинксаурце**](cbasefilter-getsyncsource.md)
-   [**Кбасефилтер:: Жоинфилтерграф**](cbasefilter-joinfiltergraph.md)
-   [**Кбасефилтер:: @ Active**](cbasefilter-isactive.md)
-   [**Кбасефилтер:: Сетсинксаурце**](cbasefilter-setsyncsource.md)
-   [**Кбасефилтер::P Аусе**](cbasefilter-pause.md)
-   [**Кбасефилтер:: Run**](cbasefilter-run.md)
-   [**Кбасефилтер:: останавливаться**](cbasefilter-stop.md)

Не держите этот критический раздел во время операций потоковой передачи (то есть при доставке образцов в нисходящий фильтр). Сериализация операций потоковой передачи с использованием другой критической секции. В противном случае это может привести к взаимоблокировке.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Амфилтер. h (включение Streams. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасефилтер**](cbasefilter.md)
</dt> <dt>

[Потоки и критические разделы](threads-and-critical-sections.md)
</dt> </dl>

 

 




