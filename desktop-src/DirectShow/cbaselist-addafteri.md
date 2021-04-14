---
description: Метод Аддафтери вставляет элемент после указанной позиции.
ms.assetid: 6da6c1ed-5f22-4364-b636-64b5a0ce1560
title: Кбаселист. Аддафтери, метод (Вкслист. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.AddAfterI
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 760c0bea3a213d7126ea795e9575b3897117f7a1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668619"
---
# <a name="cbaselistaddafteri-method"></a>Кбаселист. Аддафтери, метод

`AddAfterI`Метод вставляет элемент после указанной позиции.

## <a name="syntax"></a>Синтаксис


```C++
POSITION AddAfterI(
   POSITION pos,
   void     *pObj
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*pos* 
</dt> <dd>

Позиция, после которой нужно добавить элемент.

</dd> <dt>

*побж* 
</dt> <dd>

Указатель на добавляемый элемент.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает индикатор позиции вставленного элемента.

## <a name="remarks"></a>Комментарии

Если *POS* имеет **значение NULL**, этот метод добавляет элемент в заголовок списка (эквивалентно вызову метода [**кбаселист:: аддхеади**](cbaselist-addheadi.md) ).

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Вкслист. h (включение Streams. h)</dt> </dl>                                                                                    |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбаселист**](cbaselist.md)
</dt> </dl>

 

 




