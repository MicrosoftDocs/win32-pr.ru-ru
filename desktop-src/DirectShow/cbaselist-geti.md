---
description: Метод Жети извлекает элемент в указанной позиции.
ms.assetid: fc775230-491a-49b6-b631-e7d5b8c82d8c
title: Кбаселист. Жети, метод (Вкслист. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.GetI
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6f543a38c3394943e3ccb1eeb8bb97d29297a4ca230966940245a2f8a8c121b6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120087444"
---
# <a name="cbaselistgeti-method"></a>Кбаселист. Жети, метод

`GetI`Метод извлекает элемент в указанной позиции.

## <a name="syntax"></a>Синтаксис


```C++
void* GetI(
   POSITION pos
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*pos* 
</dt> <dd>

Индикатор позиции для извлекаемого элемента.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает указатель на элемент.

## <a name="remarks"></a>Remarks

Если *POS* имеет **значение NULL**, метод возвращает **значение NULL**.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>вкслист. h (включает Потоки. h)</dt> </dl>                                                                                    |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Кбаселист**](cbaselist.md)
</dt> </dl>

 

 




