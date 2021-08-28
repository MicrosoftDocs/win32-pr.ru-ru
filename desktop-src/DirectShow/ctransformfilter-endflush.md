---
description: Ктрансформфилтер. Ендфлуш, метод Ендфлуш завершает операцию очистки.
ms.assetid: ebb6beec-84e2-49a7-9771-bbd191faada7
title: Ктрансформфилтер. Ендфлуш, метод (Трансфрм. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.EndFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 593ce39dbba6ccf90838b4847bb0a548b67e4785bb21d3f299882e1eecdf8394
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120083914"
---
# <a name="ctransformfilterendflush-method"></a>Ктрансформфилтер. Ендфлуш, метод

`EndFlush`Метод завершает операцию очистки.

## <a name="syntax"></a>Синтаксис


```C++
virtual HRESULT EndFlush();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Возвращает \_ значение, равное ОК или другому значению **HRESULT** .

## <a name="remarks"></a>Remarks

В конце операции записи на диск метод [**ктрансформинпутпин:: ендфлуш**](ctransforminputpin-endflush.md) закрепления вызывает этот метод. Этот метод передает `EndFlush` вызов в нисходящем порядке.

Если производный класс использует рабочий поток для доставки образцов, он должен отбросить все данные, помещенные в очередь, прежде чем отправлять `EndFlush` вызов в нисходящем направлении. дополнительные сведения см. в статье [Flow данных для разработчиков фильтров](data-flow-for-filter-developers.md).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>трансфрм. h (включает Потоки. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Ктрансформфилтер**](ctransformfilter.md)
</dt> </dl>

 

 




