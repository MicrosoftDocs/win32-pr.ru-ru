---
description: Неактивный метод завершает работу рабочего потока, который извлекает данные из выходного ПИН-кода. Этот метод также отменяет выделение распределителя.
ms.assetid: 90b91686-b9a8-4196-b559-de924334f11c
title: Метод Кпуллпин. Inactive (Пуллпин. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.Inactive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 56307362651761dbe2bc5c0242a24f189cf14d1e820df6a5ba21bdeb9c7deb0e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119565374"
---
# <a name="cpullpininactive-method"></a>Кпуллпин. Inactive, метод

`Inactive`Метод завершает работу рабочего потока, который извлекает данные из выходного ПИН-кода. Этот метод также отменяет выделение распределителя.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT Inactive();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение S \_ ОК.

## <a name="remarks"></a>Remarks

Вызывайте этот метод, когда фильтр владельца станет неактивным. (Если входной ПИН-код является производным от [**кбасепин**](cbasepin.md), переопределите метод [**Кбасепин:: Inactive**](cbasepin-inactive.md) .)

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>Пуллпин. h</dt> </dl>                                                                                                       |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Кпуллпин**](cpullpin.md)
</dt> </dl>

 

 




