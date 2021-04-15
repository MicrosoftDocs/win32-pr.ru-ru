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
ms.openlocfilehash: 6104b6acae0f22c028f3bad050567f4da34ff0f6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668611"
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

## <a name="remarks"></a>Комментарии

Если метод завершается ошибкой, возвращается значение **null**.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Вкслист. h (включение Streams. h)</dt> </dl>                                                                                    |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбаселист**](cbaselist.md)
</dt> </dl>

 

 




