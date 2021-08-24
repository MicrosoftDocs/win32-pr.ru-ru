---
description: Метод Аддхеади добавляет элемент в начало списка.
ms.assetid: d83b3c5e-2c6d-4369-a74d-18bf19cfd34d
title: Кбаселист. Аддхеади, метод (Вкслист. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.AddHeadI
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4c1f22434aa2c927933c36ec496d5880ca8f3f673b314d7a8197079203757427
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119568124"
---
# <a name="cbaselistaddheadi-method"></a>Кбаселист. Аддхеади, метод

`AddHeadI`Метод добавляет элемент в начало списка.

## <a name="syntax"></a>Синтаксис


```C++
POSITION AddHeadI(
   void *pObj
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*побж* 
</dt> <dd>

Указатель на элемент.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение расположения, указывающее новую головную точку.

## <a name="remarks"></a>Remarks

Если метод завершается ошибкой, возвращается значение **null**.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>вкслист. h (включает Потоки. h)</dt> </dl>                                                                                    |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Кбаселист**](cbaselist.md)
</dt> </dl>

 

 




