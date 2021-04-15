---
description: Оператор ссылки \_ time () приводит объект к ссылочному \_ типу данных времени.
ms.assetid: 36f51e03-a458-46e6-9657-977b263c127f
title: Метод REFERENCE_TIME Крефтиме. operator (Рефтиме. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRefTime.operator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a3ceeeb00ba1de4f305f87ef3fe15e70a8d91457
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675711"
---
# <a name="creftimeoperator-reference_time-method"></a>Метод времени ссылки Крефтиме. operator \_

`REFERENCE_TIME()`Оператор приводит объект к ссылочному типу данных [**\_ времени**](reference-time.md) .

## <a name="syntax"></a>Синтаксис


```C++
REFERENCE_TIME operator REFERENCE_TIME() const;
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение [**крефтиме:: m \_ time**](creftime-m-time.md).

## <a name="remarks"></a>Комментарии

В следующем примере показано, как использовать этот оператор приведения:


```C++
CRefTime cRT(1000);
REFERENCE_TIME rt = (REFERENCE_TIME)cRT;
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Рефтиме. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



 

 




