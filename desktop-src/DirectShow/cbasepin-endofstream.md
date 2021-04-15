---
description: 'Метод EndOfStream уведомляет ПИН-код о том, что дополнительные данные не ожидаются. Этот метод реализует метод Ипин:: EndOfStream. Вызывайте этот метод только для входных ПИН-кодов.'
ms.assetid: 52a71c30-bd68-4152-8901-71ef2e65913a
title: Кбасепин. EndOfStream, метод (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.EndOfStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2324bae8ec1266dce2471049f8ba2f06b0c9e6e1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669303"
---
# <a name="cbasepinendofstream-method"></a>Кбасепин. EndOfStream, метод

`EndOfStream`Метод уведомляет ПИН-код о том, что дополнительные данные не ожидаются. Этот метод реализует метод [**Ипин:: EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) . Вызывайте этот метод только для входных ПИН-кодов.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT EndOfStream();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение S \_ ОК.

## <a name="remarks"></a>Комментарии

Фильтр должен передавать уведомления о завершении потока в подчиненные входные контакты подключенных фильтров. Если фильтр является модулем подготовки отчетов, он должен опубликовать уведомление о событии [**EC \_ Complete**](ec-complete.md) в диспетчере графов фильтров. Дополнительные сведения см. [в разделе поток данных в графе фильтра](data-flow-in-the-filter-graph.md).

В базовом классе этот метод не выполняет никаких действий. Производные классы должны переопределять этот метод.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Амфилтер. h (включение Streams. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасепин**](cbasepin.md)
</dt> </dl>

 

 




