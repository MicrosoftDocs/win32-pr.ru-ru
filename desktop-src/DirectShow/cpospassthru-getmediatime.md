---
description: Метод Жетмедиатиме извлекает метки времени для текущего образца.
ms.assetid: 36f3b6d3-b884-4168-94f3-f334a5056c7d
title: Кпоспасссру. Жетмедиатиме, метод (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.GetMediaTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b2748d986f121a38041155dcd43f13a647916486
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675042"
---
# <a name="cpospassthrugetmediatime-method"></a>Кпоспасссру. Жетмедиатиме, метод

`GetMediaTime`Метод получает метки времени для текущего образца.

## <a name="syntax"></a>Синтаксис


```C++
virtual HRESULT GetMediaTime(
   LONGLONG *pStartTime,
   LONGLONG *pEndTime
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пстарттиме* 
</dt> <dd>

Указатель на переменную, которая получает время начала в единицах текущего формата времени.

</dd> <dt>

*пендтиме* 
</dt> <dd>

Указатель на переменную, которая получает время окончания в единицах текущего формата времени.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение E \_ Fail.

## <a name="remarks"></a>Комментарии

Переопределите этот метод, если фильтр кэширует метки времени на получаемых образцах.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ктлутил. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кпоспасссру**](cpospassthru.md)
</dt> </dl>

 

 




