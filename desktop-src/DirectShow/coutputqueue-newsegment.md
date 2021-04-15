---
description: Метод Невсегмент доставляет новый сегмент входного ПИН-кода.
ms.assetid: 53189729-9f47-425e-9df6-faea01dd4482
title: Каутпуткуеуе. Невсегмент, метод (Аутпутк. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.NewSegment
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e682211a98f4409fda35687160c88b121fa93898
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675789"
---
# <a name="coutputqueuenewsegment-method"></a>Каутпуткуеуе. Невсегмент, метод

`NewSegment`Метод доставляет новый сегмент для входного ПИН-кода.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT NewSegment(
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

Возвращает значение **HRESULT** .

## <a name="remarks"></a>Комментарии

Если объект использует поток, он помещает в очередь следующие элементы по порядку:

-   НОВОЕ \_ сообщение управления сегментами.
-   Данные сегмента.

\_Сообщение о новом сегменте уведомляет поток о том, что следующий элемент в очереди будет содержать данные сегмента. Данные сегмента упаковываются в структуру, объявленную следующим образом:


```C++
struct NewSegmentPacket {
    REFERENCE_TIME tStart;
    REFERENCE_TIME tStop;
    double dRate;
}; 
```



Поток вызывает метод [**Ипин:: невсегмент**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment) для входного ПИН-кода, используя данные, представленные в структуре.

Если объект не использует поток, он вызывает метод [**каутпуткуеуе:: сенданивай**](coutputqueue-sendanyway.md) для доставки всех ожидающих выборок. Затем он вызывает **Ипин:: невсегмент** для входного ПИН-кода.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Аутпутк. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Каутпуткуеуе**](coutputqueue.md)
</dt> </dl>

 

 




