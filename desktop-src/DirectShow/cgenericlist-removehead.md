---
description: Метод Ремовехеад удаляет первый элемент из списка.
ms.assetid: 95902028-d2c2-4c16-9ca6-ef57174a9292
title: Кженериклист. Ремовехеад, метод (Вкслист. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList.RemoveHead
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7b374ad6a08aac039de3c7d54ee4403f240fdf6bf9839a5ea2554901de789f11
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119317754"
---
# <a name="cgenericlistremovehead-method"></a>Кженериклист. Ремовехеад, метод

`RemoveHead`Метод удаляет первый элемент из списка.

## <a name="syntax"></a>Синтаксис


```C++
OBJECT* RemoveHead();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Возвращает указатель на объект типа **Object** (тип шаблона) или **значение NULL** , если список пуст.

## <a name="remarks"></a>Remarks

Этот метод удаляет узел списка, но не элемент, содержащийся в узле.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>вкслист. h (включает Потоки. h)</dt> </dl>                                                                                    |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кженериклист**](cgenericlist.md)
</dt> </dl>

 

 




