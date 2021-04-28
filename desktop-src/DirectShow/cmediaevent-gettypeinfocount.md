---
description: Кмедиаевент. Жеттипеинфокаунт, метод возвращает количество интерфейсов типа данных, предоставленных объектом.
ms.assetid: e16bc324-bb49-4df2-afeb-2c2cd1620693
title: Кмедиаевент. Жеттипеинфокаунт, метод (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaEvent.GetTypeInfoCount
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c9402ad973a08afed4d338cfdc7b5df7fb14b9f0
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099122"
---
# <a name="cmediaeventgettypeinfocount-method"></a>Кмедиаевент. Жеттипеинфокаунт, метод

Извлекает количество интерфейсов типа данных, предоставленных объектом.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetTypeInfoCount(
   UINT *pctinfo
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пктинфо* 
</dt> <dd>

Указатель на число интерфейсов типа данных, предоставляемых объектом. Если объект предоставляет сведения о типе, это число равно 1; в противном случае число равно 0.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает \_ указатель E, если *пктинфо* является недопустимым; в противном случае возвращает значение S \_ ОК.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ктлутил. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Кмедиаевент**](cmediaevent.md)
</dt> </dl>

 

 




