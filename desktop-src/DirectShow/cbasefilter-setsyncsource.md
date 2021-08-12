---
description: 'Метод Сетсинксаурце задает время ссылки для фильтра. Этот метод реализует метод Имедиафилтер:: Сетсинксаурце.'
ms.assetid: 298039fc-dd38-4063-8752-2669b134b8ef
title: Кбасефилтер. Сетсинксаурце, метод (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.SetSyncSource
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 95e1f1b3578fa88d4616fc9e0b7d0af9fe89ab80c2e93ee32eef305b93d45478
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118659590"
---
# <a name="cbasefiltersetsyncsource-method"></a>Кбасефилтер. Сетсинксаурце, метод

Метод **сетсинксаурце** задает время ссылки для фильтра. Этот метод реализует метод [**имедиафилтер:: сетсинксаурце**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT SetSyncSource(
   IReferenceClock *pClock
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пклокк* 
</dt> <dd>

Указатель на интерфейс [**иреференцеклокк**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) часов или **значение NULL**.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>амфилтер. h (включает Потоки. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасефилтер**](cbasefilter.md)
</dt> </dl>

 

 




