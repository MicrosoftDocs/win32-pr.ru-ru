---
description: Функция Конверттомиллисекондс преобразует время ссылки в миллисекунды.
ms.assetid: fae3baa4-9344-4197-b375-4abe2656e1b7
title: Функция Конверттомиллисекондс (Рефклокк. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConvertToMilliseconds
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6e68b84482a437789c620efee7455144905fd33e7b1bdb651df207958ee6befc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119073747"
---
# <a name="converttomilliseconds-function"></a>Функция Конверттомиллисекондс

`ConvertToMilliseconds`Функция преобразует время ссылки в миллисекунды.

## <a name="syntax"></a>Синтаксис


```C++
LONGLONG ConvertToMilliseconds(
   const REFERENCE_TIME &RT
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*RT* \[ ЗНАЧ\]
</dt> <dd>

Время ссылки в единицах измерения 100-наносекундных.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает время ссылки, преобразованное в миллисекунды.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>рефклокк. h (включает Потоки. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Кбасереференцеклокк**](cbasereferenceclock.md)
</dt> </dl>

 

 




