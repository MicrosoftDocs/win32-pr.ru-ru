---
description: Метод Аддбефореи вставляет элемент перед указанной позицией.
ms.assetid: d310e303-889a-43a6-bda5-2e7b805b25d1
title: Кбаселист. Аддбефореи, метод (Вкслист. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.AddBeforeI
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cfb995e614904e807e67eeee9c0f344525fd701d039c596eb081b6ff3be4f078
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117823751"
---
# <a name="cbaselistaddbeforei-method"></a>Кбаселист. Аддбефореи, метод

`AddBeforeI`Метод вставляет элемент перед указанной позицией.

## <a name="syntax"></a>Синтаксис


```C++
POSITION AddBeforeI(
   POSITION pos,
   void     *pObj
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*pos* 
</dt> <dd>

Позиция, до которой нужно добавить элемент.

</dd> <dt>

*побж* 
</dt> <dd>

Указатель на элемент.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает индикатор позиции для вставленного элемента.

## <a name="remarks"></a>Remarks

Если *POS* имеет **значение NULL**, этот метод добавляет элемент в конец списка (эквивалентно вызову метода [**кбаселист:: аддтаили**](cbaselist-addtaili.md) ).

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>вкслист. h (включает Потоки. h)</dt> </dl>                                                                                    |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбаселист**](cbaselist.md)
</dt> </dl>

 

 




