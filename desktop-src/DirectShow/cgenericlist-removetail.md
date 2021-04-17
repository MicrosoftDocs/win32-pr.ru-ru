---
description: Метод Ремоветаил удаляет последний элемент в списке.
ms.assetid: 377af676-8042-430e-87a6-b41c00482a90
title: Кженериклист. Ремоветаил, метод (Вкслист. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList.RemoveTail
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a7b98187c663f643acdce28b4f12ebc37b1d4c25
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657556"
---
# <a name="cgenericlistremovetail-method"></a>Кженериклист. Ремоветаил, метод

`RemoveTail`Метод удаляет последний элемент в списке.

## <a name="syntax"></a>Синтаксис


```C++
OBJECT* RemoveTail();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Возвращает указатель на объект типа **Object** (тип шаблона) или **значение NULL** , если список пуст.

## <a name="remarks"></a>Комментарии

Этот метод удаляет узел списка, но не элемент, содержащийся в узле.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Вкслист. h (включение Streams. h)</dt> </dl>                                                                                    |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кженериклист**](cgenericlist.md)
</dt> </dl>

 

 




