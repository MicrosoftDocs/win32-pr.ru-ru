---
description: 'Метод Жетсинксаурце извлекает ссылочное время, которое использует объект. Этот метод реализует метод Имедиафилтер:: Жетсинксаурце.'
ms.assetid: 7e74d6ce-cd34-4345-8ff9-174e0acb243a
title: Кбасемедиафилтер. Жетсинксаурце, метод (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseMediaFilter.GetSyncSource
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1e92c9d0fa5e486d7785ff8184ba4ce0dd42e5be
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105656975"
---
# <a name="cbasemediafiltergetsyncsource-method"></a>Кбасемедиафилтер. Жетсинксаурце, метод

`GetSyncSource`Метод получает ссылочное время, которое использует объект. Этот метод реализует метод [**имедиафилтер:: жетсинксаурце**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-getsyncsource) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetSyncSource(
   IReferenceClock **pClock
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пклокк* 
</dt> <dd>

Адрес переменной, которая получает указатель на интерфейс [**иреференцеклокк**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) часов.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение S \_ (ОК) или \_ указатель E.

## <a name="remarks"></a>Комментарии

Если объект не использует ссылочный таймер, *\* пклокк* имеет значение **null**. Если метод возвращает значение, если *\* пклокк* не равен **null**, то интерфейс **иреференцеклокк** имеет необработанный счетчик ссылок. Не забудьте освободить его по завершении.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Амфилтер. h (включение Streams. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасемедиафилтер**](cbasemediafilter.md)
</dt> </dl>

 

 




