---
description: Метод Моветотаил разделяет список и добавляет его в конец другого списка.
ms.assetid: f5cefe7c-075c-433b-9ece-aa10217344fa
title: Кбаселист. Моветотаил, метод (Вкслист. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.MoveToTail
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8ae7ab918c8c4ef707b2754f8b1ba1f8f3e76265a6b8ac0b252e765de2aff1b2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119016922"
---
# <a name="cbaselistmovetotail-method"></a>Кбаселист. Моветотаил, метод

`MoveToTail`Метод разбивает список и добавляет его в конец другого списка.

## <a name="syntax"></a>Синтаксис


```C++
BOOL MoveToTail(
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

Этот метод разделяет список после того, как позиция задается параметром *POS* . Заключительная часть остается в списке. Главная часть добавляется в конец другого списка.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>вкслист. h (включает Потоки. h)</dt> </dl>                                                                                    |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбаселист**](cbaselist.md)
</dt> </dl>

 

 




