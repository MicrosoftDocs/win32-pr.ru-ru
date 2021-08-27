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
ms.openlocfilehash: 9a084d4e142f57b724343ac5a353461b41aac0be216b8e3851bc8b7e40000a1f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120108034"
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

## <a name="remarks"></a>Remarks

В следующем примере показано, как использовать этот оператор приведения:


```C++
CRefTime cRT(1000);
REFERENCE_TIME rt = (REFERENCE_TIME)cRT;
```



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>рефтиме. h (включает Потоки. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



 

 




