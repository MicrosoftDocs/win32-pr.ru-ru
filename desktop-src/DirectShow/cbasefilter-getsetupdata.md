---
description: Метод Жетсетупдата извлекает данные регистрации для фильтра.
ms.assetid: 93582c75-4f40-492c-919c-c8a06dce7715
title: Кбасефилтер. Жетсетупдата, метод (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.GetSetupData
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 40223a22f4de4a078ce84f8ebe49bddd5ab13575
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657806"
---
# <a name="cbasefiltergetsetupdata-method"></a>Кбасефилтер. Жетсетупдата, метод

`GetSetupData`Метод получает данные регистрации для фильтра.

> [!Note]  
> Этот метод устарел. Он вызывается методами [**кбасефилтер:: Register**](cbasefilter-register.md) и [**кбасефилтер:: Unregister**](cbasefilter-unregister.md) .

 

## <a name="syntax"></a>Синтаксис


```C++
virtual LPAMOVIESETUP_FILTER GetSetupData();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Возвращает указатель на структуру [**\_ фильтра амовиесетуп**](amoviesetup-filter.md) , содержащую сведения о регистрации для фильтра.

## <a name="remarks"></a>Комментарии

Базовый класс возвращает **значение NULL**.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Амфилтер. h (включение Streams. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасефилтер**](cbasefilter.md)
</dt> </dl>

 

 




