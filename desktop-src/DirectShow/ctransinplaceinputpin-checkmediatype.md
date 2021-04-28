---
description: Ктрансинплацеинпутпин. Чеккмедиатипе, метод Чеккмедиатипе определяет, принимает ли ПИН-код конкретный тип носителя.
ms.assetid: 2d5f784a-8970-487d-94ef-d96d04f8eb2e
title: Ктрансинплацеинпутпин. Чеккмедиатипе, метод (Трансип. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceInputPin.CheckMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5de3cec87d740db42824b0d7abf1ee4bfc6aeecb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094802"
---
# <a name="ctransinplaceinputpincheckmediatype-method"></a>Ктрансинплацеинпутпин. Чеккмедиатипе, метод

`CheckMediaType`Метод определяет, принимает ли ПИН-код конкретный тип носителя.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT CheckMediaType(
   const CMediaType *pmt
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*состоит* 
</dt> <dd>

Указатель на объект [**кмедиатипе**](cmediatype.md) , который содержит предложенный тип мультимедиа.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

\_Если предложенный тип мультимедиа приемлем, возвращается значение S. В противном случае возвращает \_ значение S false или код ошибки.

## <a name="remarks"></a>Remarks

Этот метод переопределяет метод [**ктрансформинпутпин:: чеккмедиатипе**](ctransforminputpin-checkmediatype.md) . Он вызывает метод [**ктрансформфилтер:: чеккинпуттипе**](ctransformfilter-checkinputtype.md) фильтра для проверки входного типа. Если выходной ПИН-код подключен, этот метод также вызывает метод [**Ипин:: куерякцепт**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) для входного ПИН-кода нисходящего входа.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Трансип. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Ктрансинплацеинпутпин**](ctransinplaceinputpin.md)
</dt> </dl>

 

 




