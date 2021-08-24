---
description: Кбасефилтер. Жетпинкаунт, метод Жетпинкаунт извлекает количество ПИН-кодов.
ms.assetid: 6cbeb123-d899-4f13-8b40-5666adec610f
title: Кбасефилтер. Жетпинкаунт, метод (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.GetPinCount
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e7d136b5b3bbdcd8a6b21fcbd9f854de7a78a91be87a199c990e294ce8b28fb6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119640484"
---
# <a name="cbasefiltergetpincount-method"></a>Кбасефилтер. Жетпинкаунт, метод

`GetPinCount`Метод получает количество ПИН-кодов.

## <a name="syntax"></a>Синтаксис


```C++
virtual int GetPinCount() = 0;
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Возвращает число ПИН-кодов.

## <a name="remarks"></a>Remarks

Производный класс должен реализовывать этот чистый виртуальный метод. Возврат количества ПИН-кодов, доступных в данный момент в этом фильтре. Фильтры могут динамически создавать или удалять ПИН-коды.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>амфилтер. h (включает Потоки. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Кбасефилтер**](cbasefilter.md)
</dt> </dl>

 

 




