---
description: '\_Метод курса размещения задает скорость воспроизведения. Этот метод реализует метод Имедиапоситион::p UT \_ .'
ms.assetid: c077f344-de34-4f8a-8e08-6d7086a5a4f1
title: Метод CPosPassThru.put_Rate (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.put_Rate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 21e7e654233f78adcda2addf73b87a178654872e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105674836"
---
# <a name="cpospassthruput_rate-method"></a>Кпоспасссру. помещает \_ метод Rate

`put_Rate`Метод задает скорость воспроизведения. Этот метод реализует метод [**имедиапоситион::p UT \_**](/windows/desktop/api/Control/nf-control-imediaposition-put_rate) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT put_Rate(
   double dRate
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*драте* 
</dt> <dd>

Скорость воспроизведения. Не должно быть нулем.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает E \_ INVALIDARG, если *драте* равен нулю. В противном случае возвращает значение **HRESULT** из подключенного ПИН-кода.

## <a name="remarks"></a>Комментарии

Отрицательные тарифы указывают на обратную игру. Не все носители будут поддерживать обратную воспроизведение.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ктлутил. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кпоспасссру**](cpospassthru.md)
</dt> </dl>

 

 




