---
description: Неактивный метод уведомляет ПИН-код о том, что фильтр остановлен.
ms.assetid: f7efb67b-cc3f-47c4-a8ba-b2365aef0d96
title: Метод Кдинамикаутпутпин. Inactive (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.Inactive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d52ec1735be6d4e89885295a9d9c2d382142fdc9d31f95b6368d0ef2f331608e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119317714"
---
# <a name="cdynamicoutputpininactive-method"></a>Кдинамикаутпутпин. Inactive, метод

`Inactive`Метод уведомляет ПИН-код о том, что фильтр остановлен.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT Inactive();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Возвращает \_ значение ОК в случае успешного выполнения или **HRESULT** , указывающий на причину сбоя.

## <a name="remarks"></a>Remarks

Этот метод переопределяет метод [**кбасеаутпутпин:: Inactive**](cbaseoutputpin-inactive.md) . Он устанавливает событие [**кдинамикаутпутпин:: m \_ хстопевент**](cdynamicoutputpin-m-hstopevent.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>амфилтер. h (включает Потоки. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кдинамикаутпутпин**](cdynamicoutputpin.md)
</dt> </dl>

 

 




