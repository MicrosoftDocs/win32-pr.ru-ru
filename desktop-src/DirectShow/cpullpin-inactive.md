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
ms.openlocfilehash: 4f32084428a36032152d3c3297b1fc9419e51cb3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669054"
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

## <a name="remarks"></a>Комментарии

Вызывайте этот метод, когда фильтр владельца станет неактивным. (Если входной ПИН-код является производным от [**кбасепин**](cbasepin.md), переопределите метод [**Кбасепин:: Inactive**](cbasepin-inactive.md) .)

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Пуллпин. h</dt> </dl>                                                                                                       |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кпуллпин**](cpullpin.md)
</dt> </dl>

 

 




