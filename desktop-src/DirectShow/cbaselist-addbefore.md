---
description: Метод Аддбефоре вставляет список перед указанной позицией.
ms.assetid: a4c0dbec-64a0-445b-95e5-000603cc0264
title: Кбаселист. Аддбефоре, метод (Вкслист. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.AddBefore
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2b4f85536b6a9372f164f596f96758a503096dbb0a5e5ed55adab42bc406b053
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119016972"
---
# <a name="cbaselistaddbefore-method"></a>Кбаселист. Аддбефоре, метод

`AddBefore`Метод вставляет список перед указанной позицией.

## <a name="syntax"></a>Синтаксис


```C++
BOOL AddBefore(
   POSITION  pos,
   CBaseList *pList
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*pos* 
</dt> <dd>

Расположение, до которого необходимо вставить список.

</dd> <dt>

*pList* 
</dt> <dd>

Указатель на список для вставки.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение true** в случае успеха. В противном случае возвращает **значение false**.

## <a name="remarks"></a>Remarks

Существующие индикаторы позиционирования, включая указанные в параметре *POS* , остаются действительными. В случае сбоя метода некоторые элементы могли быть добавлены.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>вкслист. h (включает Потоки. h)</dt> </dl>                                                                                    |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбаселист**](cbaselist.md)
</dt> </dl>

 

 




