---
description: Метод Remove удаляет элемент в указанной позиции.
ms.assetid: a7b8f6fb-f13a-4c24-aa18-463446602e29
title: Метод Кженериклист. Remove (Вкслист. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList.Remove
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 40b00d0772f391978fa6e581623446c67c2f37deabb1737e2602d7da7382fbaf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119317764"
---
# <a name="cgenericlistremove-method"></a>Кженериклист. Remove, метод

`Remove`Метод удаляет элемент в указанной позиции.

## <a name="syntax"></a>Синтаксис


```C++
OBJECT* Remove(
   POSITION pos
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*pos* 
</dt> <dd>

Значение позиции, указывающее удаляемый элемент.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает указатель на объект типа **Object** (тип шаблона).

## <a name="remarks"></a>Remarks

Этот метод удаляет узел из списка, но не удаляет элемент, содержащийся в этом узле.

Если *POS* имеет **значение NULL**, метод возвращает **значение NULL**.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>вкслист. h (включает Потоки. h)</dt> </dl>                                                                                    |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кженериклист**](cgenericlist.md)
</dt> </dl>

 

 




