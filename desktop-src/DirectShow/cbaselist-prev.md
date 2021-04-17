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
ms.openlocfilehash: 03c35a89754b27aa67a5bba33ee694433d74c0fd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657386"
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

## <a name="remarks"></a>Комментарии

Если *POS* является первой позицией в списке, метод возвращает **значение NULL**. Если *POS* имеет **значение NULL**, метод возвращает последнюю положение в списке.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Вкслист. h (включение Streams. h)</dt> </dl>                                                                                    |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбаселист**](cbaselist.md)
</dt> </dl>

 

 




