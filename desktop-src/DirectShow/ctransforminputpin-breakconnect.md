---
description: Ктрансформинпутпин. Бреакконнект, метод Бреакконнект освобождает ПИН-код из соединения.
ms.assetid: 9874717d-f4d8-426d-a717-9f5d83b4683c
title: Ктрансформинпутпин. Бреакконнект, метод (Трансфрм. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.BreakConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fe425ba617909dcfb1d66dbb4777b579139d436b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085022"
---
# <a name="ctransforminputpinbreakconnect-method"></a>Ктрансформинпутпин. Бреакконнект, метод

`BreakConnect`Метод освобождает ПИН-код из соединения.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT BreakConnect();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Возвращает \_ значение, равное ОК или другому значению **HRESULT** .

## <a name="remarks"></a>Remarks

Этот метод переопределяет метод [**кбасеинпутпин:: бреакконнект**](cbaseinputpin-breakconnect.md) . Он вызывает метод [**ктрансформфилтер:: бреакконнект**](ctransformfilter-breakconnect.md) фильтра, который возвращает \_ значение s ОК в базовом классе. Производный класс может переопределить метод **ктрансформфилтер:: бреакконнект** .

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Трансфрм. h (включение Streams. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



 

 




