---
description: Следующий метод извлекает следующее расположение в списке.
ms.assetid: ba9753b0-c82e-4772-84a7-e9982de3b8ad
title: Метод Кбаселист. Next (Вкслист. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.Next
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d07030c046f3fe55178707af297542f383bfd5cf75f40169b5c93cfafa1c698b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118658960"
---
# <a name="cbaselistnext-method"></a>Кбаселист. Next, метод

`Next`Метод получает следующую точку в списке.

## <a name="syntax"></a>Синтаксис


```C++
POSITION Next(
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

Возвращает индикатор положения, следующий за позицией, заданной в *POS*.

## <a name="remarks"></a>Remarks

Если *POS* является последней позицией в списке, метод возвращает **значение NULL**. Если *POS* имеет **значение NULL**, метод возвращает первую точку в списке.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>вкслист. h (включает Потоки. h)</dt> </dl>                                                                                    |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбаселист**](cbaselist.md)
</dt> </dl>

 

 




