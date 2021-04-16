---
description: 'Метод Сетсинксаурце устанавливает ссылочный таймер для объекта. Этот метод реализует метод Имедиафилтер:: Сетсинксаурце.'
ms.assetid: ae296741-e3da-4376-a88a-8470f0a414ed
title: Кбасемедиафилтер. Сетсинксаурце, метод (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseMediaFilter.SetSyncSource
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 01597228ddbadec6c1b0db481719fb690584b7fe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105656924"
---
# <a name="cbasemediafiltersetsyncsource-method"></a>Кбасемедиафилтер. Сетсинксаурце, метод

`SetSyncSource`Метод задает время ссылки для объекта. Этот метод реализует метод [**имедиафилтер:: сетсинксаурце**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource) .

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

Возвращает значение S \_ ОК.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Амфилтер. h (включение Streams. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасемедиафилтер**](cbasemediafilter.md)
</dt> </dl>

 

 




