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
ms.openlocfilehash: 80adec6c8e2f6d42b5cf2cabd3a83a4c3aededa3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668598"
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

## <a name="remarks"></a>Комментарии

Этот метод разделяет список перед позицией, заданной параметром *POS* . Главная часть остается в списке. Заключительная часть вставляется в заголовок другого списка.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Вкслист. h (включение Streams. h)</dt> </dl>                                                                                    |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбаселист**](cbaselist.md)
</dt> </dl>

 

 




