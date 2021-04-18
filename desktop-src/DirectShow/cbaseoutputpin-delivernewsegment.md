---
description: Метод Деливерневсегмент доставляет уведомление о новом сегменте в подключенный входной ПИН-код.
ms.assetid: 304f0267-88e0-4642-98a2-68ce973bdeab
title: Кбасеаутпутпин. Деливерневсегмент, метод (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.DeliverNewSegment
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3eb6d31a50095affdf38d44b69040304674ec6fe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669175"
---
# <a name="cbaseoutputpindelivernewsegment-method"></a>Кбасеаутпутпин. Деливерневсегмент, метод

`DeliverNewSegment`Метод доставляет уведомление о новом сегменте в подключенный входной ПИН-код.

## <a name="syntax"></a>Синтаксис


```C++
virtual HRESULT DeliverNewSegment(
   REFERENCE_TIME tStart,
   REFERENCE_TIME tStop,
   double         dRate
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*тстарт* 
</dt> <dd>

Начальная координата носителя сегмента, в единицах 100-наносекундных.

</dd> <dt>

*тстоп* 
</dt> <dd>

Конечное расположение носителя сегмента в единицах 100-наносекундных.

</dd> <dt>

*драте* 
</dt> <dd>

Скорость обработки этого сегмента в процентах от исходной ставки.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение **HRESULT** . Возможные значения включают перечисленные в следующей таблице.



| Код возврата                                                                                           | Описание                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl>                  | Успешно.<br/>              |
| <dl> <dt>**VFW \_ E \_ не \_ подключен**</dt> </dl> | ПИН-код не подключен.<br/> |



 

## <a name="remarks"></a>Комментарии

Этот метод вызывает метод [**Ипин:: невсегмент**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment) для входного ПИН-кода.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Амфилтер. h (включение Streams. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасеаутпутпин**](cbaseoutputpin.md)
</dt> </dl>

 

 




