---
description: 'Метод SetTime задает время потока, когда должен начинаться и заканчиваться этот образец. Этот метод реализует метод Имедиасампле:: SetTime.'
ms.assetid: cab4907f-eb6f-4444-9b41-1f95a6ecffed
title: Кмедиасампле. SetTime, метод (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.SetTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 935c4f3aa565b291e459d36e067805944b4fd6b2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105674794"
---
# <a name="cmediasamplesettime-method"></a>Кмедиасампле. SetTime, метод

`SetTime`Метод задает время потока, когда должен начинаться и заканчиваться этот образец. Этот метод реализует метод [**имедиасампле:: setTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-settime) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT SetTime(
   REFERENCE_TIME *pTimeStart,
   REFERENCE_TIME *pTimeEnd
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*птиместарт* 
</dt> <dd>

Указатель на время потока, с которого начинается выборка, в единицах 100-наносекундных или **null**.

</dd> <dt>

*птиминд* 
</dt> <dd>

Указатель на время потока, в котором заканчивается образец, в единицах 100-наносекундных или **null**.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение S \_ ОК.

## <a name="remarks"></a>Комментарии

Этот метод задает переменные конечного элемента [**кмедиасампле:: m \_ Start**](cmediasample-m-start.md) и [**кмедиасампле: \_ : m**](cmediasample-m-end.md) , которые определяют метки времени. Он также обновляет переменную члена [**кмедиасампле:: m \_ dwFlags**](cmediasample-m-dwflags.md) , которая указывает, являются ли отметки времени допустимыми.

Дополнительные сведения о метках времени см. [в разделе время и часы в DirectShow](time-and-clocks-in-directshow.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Амфилтер. h (включение Streams. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кмедиасампле**](cmediasample.md)
</dt> </dl>

 

 




