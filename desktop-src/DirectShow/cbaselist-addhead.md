---
description: Метод Аддхеад вставляет еще один список в начале этого списка.
ms.assetid: 10999d93-2eb0-481f-8909-6f1184137786
title: Кбаселист. Аддхеад, метод (Вкслист. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.AddHead
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fa8108af5f779bea4c1a1e756ab018ed9c902d3e516556c42b7899f442cb7704
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119814324"
---
# <a name="cbaselistaddhead-method"></a>Кбаселист. Аддхеад, метод

`AddHead`Метод вставляет еще один список в начале этого списка.

## <a name="syntax"></a>Синтаксис


```C++
BOOL AddHead(
   CBaseList *pList
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*pList* 
</dt> <dd>

Указатель на список элементов для добавления.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение true** , если успешно, или **false** в противном случае.

## <a name="remarks"></a>Remarks

В случае сбоя метода некоторые элементы могут быть добавлены в список.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>вкслист. h (включает Потоки. h)</dt> </dl>                                                                                    |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Кбаселист**](cbaselist.md)
</dt> </dl>

 

 




