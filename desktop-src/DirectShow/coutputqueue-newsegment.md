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
ms.openlocfilehash: 4057cafa3962c85fbca9342debbf7bb0e92355fc083e693889df298e53509259
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119768144"
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

## <a name="remarks"></a>Remarks

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

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>аутпутк. h (включает Потоки. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Каутпуткуеуе**](coutputqueue.md)
</dt> </dl>

 

 




