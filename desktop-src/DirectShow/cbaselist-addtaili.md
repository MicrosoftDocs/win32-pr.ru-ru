---
description: Метод Аддтаили добавляет элемент в конец списка.
ms.assetid: 699408d1-fee2-43d7-b2c3-51637d063b2c
title: Кбаселист. Аддтаили, метод (Вкслист. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.AddTailI
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d3317877bfa67d2d39d469882e0b12b9fd79a923873022a51ee48712fc772743
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118659130"
---
# <a name="cbaselistaddtaili-method"></a>Кбаселист. Аддтаили, метод

`AddTailI`Метод добавляет элемент в конец списка.

## <a name="syntax"></a>Синтаксис


```C++
POSITION AddTailI(
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

Возвращает значение позиции для новой позиции хвоста.

## <a name="remarks"></a>Remarks

Если метод завершается с ошибкой, возвращается **значение NULL**.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>вкслист. h (включает Потоки. h)</dt> </dl>                                                                                    |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбаселист**](cbaselist.md)
</dt> </dl>

 

 




