---
description: Метод Жетпинкаунт извлекает количество ПИН-кодов.
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
ms.openlocfilehash: 8da1cbc22a49b149bdccc36c3b854b44101b9bbc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657811"
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

## <a name="remarks"></a>Комментарии

Производный класс должен реализовывать этот чистый виртуальный метод. Возврат количества ПИН-кодов, доступных в данный момент в этом фильтре. Фильтры могут динамически создавать или удалять ПИН-коды.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Амфилтер. h (включение Streams. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасефилтер**](cbasefilter.md)
</dt> </dl>

 

 




