---
description: Ктрансформаутпутпин. Комплетеконнект, метод Комплетеконнект завершает подключение к другому ПИН-коду.
ms.assetid: 14bc48bc-ddfb-4491-8d5b-9e5ac601ba04
title: Ктрансформаутпутпин. Комплетеконнект, метод (Трансфрм. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformOutputPin.CompleteConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8383756197e076bc309e9f05e02c9c495a084644faa24959e5a7de2ac61a1c47
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119538344"
---
# <a name="ctransformoutputpincompleteconnect-method"></a>Ктрансформаутпутпин. Комплетеконнект, метод

`CompleteConnect`Метод завершает подключение к другому ПИН-коду.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT CompleteConnect(
   IPin *pReceivePin
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*прецеивепин* 
</dt> <dd>

Указатель на интерфейс [**Ипин**](/windows/desktop/api/Strmif/nn-strmif-ipin) другого ПИН-кода.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает \_ значение, равное ОК или другому значению **HRESULT** .

## <a name="remarks"></a>Remarks

Этот метод переопределяет метод [**кбасеаутпутпин:: комплетеконнект**](cbaseoutputpin-completeconnect.md) . Он вызывает метод [**ктрансформфилтер:: комплетеконнект**](ctransformfilter-completeconnect.md) фильтра, который возвращает \_ значение s ОК в базовом классе. Производный класс может переопределить метод **ктрансформфилтер:: комплетеконнект** для выполнения дополнительных проверок.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>трансфрм. h (включает Потоки. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



 

 




