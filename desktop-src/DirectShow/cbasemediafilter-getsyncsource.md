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
ms.openlocfilehash: 03bceee63109dedbf3b2fa9a855ddbfb410014d48de613f95c7bbfb98d6b0894
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118658877"
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

## <a name="remarks"></a>Remarks

Если объект не использует ссылочный таймер, *\* пклокк* имеет значение **null**. Если метод возвращает значение, если *\* пклокк* не равен **null**, то интерфейс **иреференцеклокк** имеет необработанный счетчик ссылок. Не забудьте освободить его по завершении.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>амфилтер. h (включает Потоки. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасемедиафилтер**](cbasemediafilter.md)
</dt> </dl>

 

 




