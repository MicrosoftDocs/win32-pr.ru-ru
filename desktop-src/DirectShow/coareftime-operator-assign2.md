---
description: Оператор назначает новое время ссылки и использует параметр "RT [ref]".
ms.assetid: e3a005c0-95d5-41e0-80bb-e70399a50dca
title: Коарефтиме. operator = метод (Ктлутил. h)-RT [ref] параметр
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COARefTime.operator=
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: bad1e0d7ee63fe9bcfa7fc1664a7349e787d9927
ms.sourcegitcommit: 11f52354f570aacaf1ba2a266b2e507abd73352a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/19/2021
ms.locfileid: "105674767"
---
# <a name="coareftimeoperator-method-ctlutilh---rt-ref-parameter"></a>Коарефтиме. operator = метод (Ктлутил. h)-RT [ref] параметр

Этот оператор назначает новое время ссылки.

## <a name="syntax"></a>Синтаксис


```C++
COARefTime& operator=(
  [ref] const REFERENCE_TIME &rt
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*RT* \[ ЗНАЧ\]
</dt> <dd>

Ссылка на значение [**\_ времени ссылки**](reference-time.md) , указывающее новое время ссылки в 100-наносекундных единицах.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает ссылку на объект.

## <a name="requirements"></a>Требования

| Требование                    | Значение                                                                                                                                                                                           |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header  | Ктлутил. h (включение Streams. h)                                                                                   |
| Библиотека | Стрмбасе. lib (розничные сборки); Стрмбасд. lib (отладочные сборки) |

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Коарефтиме**](coareftime.md)
</dt> </dl>

 

 




