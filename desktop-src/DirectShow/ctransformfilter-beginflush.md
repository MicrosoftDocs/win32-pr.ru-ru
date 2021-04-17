---
description: Метод Бегинфлуш начинает операцию очистки.
ms.assetid: 15bea993-f862-4791-b784-0d0468c6c05c
title: Ктрансформфилтер. Бегинфлуш, метод (Трансфрм. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.BeginFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: bd9a4bf1543f4899d4c879e9d1a9d9cf1035b765
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657026"
---
# <a name="ctransformfilterbeginflush-method"></a>Ктрансформфилтер. Бегинфлуш, метод

`BeginFlush`Метод начинает операцию записи на диск.

## <a name="syntax"></a>Синтаксис


```C++
virtual HRESULT BeginFlush();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Возвращает \_ значение, равное ОК или другому значению **HRESULT** .

## <a name="remarks"></a>Комментарии

В начале операции очистки метод [**ктрансформинпутпин:: бегинфлуш**](ctransforminputpin-beginflush.md) закрепления вызывает этот метод. Этот метод передает `BeginFlush` вызов в нисходящем порядке.

Если производный класс использует рабочий поток для доставки образцов, он должен отбросить все данные в очереди во время операции очистки. Это можно сделать либо в `BeginFlush` методе, либо в методе [**ендфлуш**](ctransformfilter-endflush.md) . Однако обратите внимание, что вызовы метода `BeginFlush` не синхронизируются с потоком потоковой передачи. Если `BeginFlush` метод отклоняет данные в очереди, то фильтр должен быть аккуратным, чтобы не обрабатывать больше данных между `BeginFlush` вызовами и **ендфлуш** . Дополнительные сведения см. в разделе [поток данных для разработчиков фильтров](data-flow-for-filter-developers.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Трансфрм. h (включение Streams. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Ктрансформфилтер**](ctransformfilter.md)
</dt> </dl>

 

 




