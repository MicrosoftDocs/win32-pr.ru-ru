---
description: Этот оператор Вычитает одно время ссылки из другого.
ms.assetid: 5691cd76-0d25-45c0-bb58-6668abe1db01
title: Коарефтиме. operator-метод (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COARefTime.operator-
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: da8de864f344321cc5dca801782aab1f8476eb91608b42577cca6a34c625e153
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119073828"
---
# <a name="coareftimeoperator--method"></a>Коарефтиме. operator — метод

Этот оператор Вычитает одно время ссылки из другого.

## <a name="syntax"></a>Синтаксис


```C++
COARefTime operator-(
  [ref] const COARefTime &rt
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*RT* \[ ЗНАЧ\]
</dt> <dd>

Ссылка на объект **коарефтиме** для вычитания.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает новый объект **коарефтиме** , равный разности времени ссылки.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>Ктлутил. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Коарефтиме**](coareftime.md)
</dt> </dl>

 

 




