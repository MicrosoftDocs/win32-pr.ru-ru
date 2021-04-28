---
description: Ктрансформинпутпин. Чеккмедиатипе, метод Чеккмедиатипе определяет, принимает ли ПИН-код конкретный тип носителя.
ms.assetid: e09a4a3e-ac39-4d0e-9e8c-3e8f18057d0d
title: Ктрансформинпутпин. Чеккмедиатипе, метод (Трансфрм. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.CheckMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c775618c9fe30de6171919d5b8bc8a80ea81d3a5
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085002"
---
# <a name="ctransforminputpincheckmediatype-method"></a>Ктрансформинпутпин. Чеккмедиатипе, метод

`CheckMediaType`Метод определяет, принимает ли ПИН-код конкретный тип носителя.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT CheckMediaType(
   const CMediaType *mtIn
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*мтин* 
</dt> <dd>

Указатель на объект [**кмедиатипе**](cmediatype.md) , который содержит предложенный тип мультимедиа.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает \_ значение, равное ОК или другому значению **HRESULT** .

## <a name="remarks"></a>Remarks

Этот метод реализует чистый виртуальный метод [**кбасепин:: чеккмедиатипе**](cbasepin-checkmediatype.md) . Он вызывает метод [**ктрансформфилтер:: чеккинпуттипе**](ctransformfilter-checkinputtype.md) фильтра, который также является чистым виртуальным. Производный класс фильтра должен реализовать **чеккинпуттипе** , чтобы определить, допустим ли данный входной тип.

Если закрепление вывода фильтра подключено, этот метод также вызывает метод [**ктрансформфилтер:: чекктрансформ**](ctransformfilter-checktransform.md) фильтра, чтобы определить, совместим ли входной тип с выходным типом. Метод **чекктрансформ** также является чистым виртуальным.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Трансфрм. h (включение Streams. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



 

 




