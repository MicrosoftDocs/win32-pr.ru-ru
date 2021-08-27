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
ms.openlocfilehash: e1a1e4c9482c187db7d5d5377535763b9fbab126b2153e0efa56bc341b402b74
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120103164"
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

## <a name="requirements"></a>Requirements (Требования)

| Требование                    | Значение                                                                                                                                                                                           |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок  | ктлутил. h (включает Потоки. h)                                                                                   |
| Библиотека | Стрмбасе. lib (розничные сборки); Стрмбасд. lib (отладочные сборки) |

## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Коарефтиме**](coareftime.md)
</dt> </dl>

 

 




