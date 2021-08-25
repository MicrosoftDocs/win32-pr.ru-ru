---
description: Метод Моветохеад разделяет список и вставляет фрагмент хвоста в заголовок другого списка.
ms.assetid: 46e4f8fe-6707-44c6-9d49-0168b35d2364
title: Кбаселист. Моветохеад, метод (Вкслист. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.MoveToHead
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 18133107a3c8038780662bc39c8bd621c8b2c445a6e1e930f8fbfc015807e9fe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119928684"
---
# <a name="cbaselistmovetohead-method"></a>Кбаселист. Моветохеад, метод

`MoveToHead`Метод разделяет список и вставляет фрагмент хвоста в начало другого списка.

## <a name="syntax"></a>Синтаксис


```C++
BOOL MoveToHead(
   POSITION  pos,
   CBaseList *pList
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*pos* 
</dt> <dd>

Индикатор положения, помечающий разбиение в списке.

</dd> <dt>

*pList* 
</dt> <dd>

Указатель на другой список.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение true** , если успешно, или **false** в противном случае.

## <a name="remarks"></a>Remarks

Этот метод разделяет список перед позицией, заданной параметром *POS* . Главная часть остается в списке. Заключительная часть вставляется в заголовок другого списка.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>вкслист. h (включает Потоки. h)</dt> </dl>                                                                                    |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Кбаселист**](cbaselist.md)
</dt> </dl>

 

 




