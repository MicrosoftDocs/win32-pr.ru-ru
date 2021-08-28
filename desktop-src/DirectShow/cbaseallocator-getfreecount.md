---
description: Метод Жетфрикаунт извлекает количество неиспользуемых выборок мультимедиа.
ms.assetid: f4ce4cca-0168-42db-9fe7-858862f033a8
title: Кбасеаллокатор. Жетфрикаунт, метод (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.GetFreeCount
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c4552829482a604b368a6710c62d0fc0b26a94aa3bb33b67ef386f2785d6c90e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120057514"
---
# <a name="cbaseallocatorgetfreecount-method"></a>Кбасеаллокатор. Жетфрикаунт, метод

`GetFreeCount`Метод получает количество неиспользуемых выборок мультимедиа.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetFreeCount(
   LONG *plBuffersFree
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*плбуфферсфри* 
</dt> <dd>

Адрес переменной, которая получает количество неиспользуемых выборок.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение S \_ ОК.

## <a name="remarks"></a>Remarks

Этот метод реализует метод [**имемаллокаторкаллбакктемп:: жетфрикаунт**](/windows/desktop/api/Strmif/nf-strmif-imemallocatorcallbacktemp-getfreecount) . Распределитель не предоставляет интерфейс Имемаллокаторкаллбакктемп, если в конструкторе Кбасеаллокатор для флага *фенаблерелеасекаллбакк* не задано **значение true** .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>амфилтер. h (включает Потоки. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Кбасеаллокатор**](cbaseallocator.md)
</dt> </dl>

 

 




