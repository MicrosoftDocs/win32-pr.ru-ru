---
description: Предыдущий метод извлекает предыдущее расположение в списке.
ms.assetid: 537c3019-373a-4974-a42e-72150da72767
title: Метод Кбаселист. PREV (Вкслист. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.Prev
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d04a63079e401b89286e10e927b540f40d04fc186546dbdbd4e31e8610fe617d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120076604"
---
# <a name="cbaselistprev-method"></a>Кбаселист. prev, метод

`Prev`Метод извлекает предыдущее расположение в списке.

## <a name="syntax"></a>Синтаксис


```C++
POSITION Prev(
   POSITION pos
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*pos* 
</dt> <dd>

Значение расположения.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает индикатор положения, предшествующий положению, указанному в *POS*.

## <a name="remarks"></a>Remarks

Если *POS* является первой позицией в списке, метод возвращает **значение NULL**. Если *POS* имеет **значение NULL**, метод возвращает последнюю положение в списке.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>вкслист. h (включает Потоки. h)</dt> </dl>                                                                                    |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Кбаселист**](cbaselist.md)
</dt> </dl>

 

 




