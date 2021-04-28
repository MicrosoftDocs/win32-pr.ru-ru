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
ms.openlocfilehash: 9a4f38a6897443763f676951f193fab5606ad2a8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085063"
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

Если производный класс использует рабочий поток для доставки образцов, он должен отбросить все данные, помещенные в очередь, прежде чем отправлять `EndFlush` вызов в нисходящем направлении. Дополнительные сведения см. в разделе [поток данных для разработчиков фильтров](data-flow-for-filter-developers.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Трансфрм. h (включение Streams. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Ктрансформфилтер**](ctransformfilter.md)
</dt> </dl>

 

 




