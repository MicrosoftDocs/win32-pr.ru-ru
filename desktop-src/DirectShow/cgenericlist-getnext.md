---
description: Метод GetNext извлекает элемент в указанной позиции и перемещает позицию.
ms.assetid: d24d3388-1af9-4a62-bdb6-d3d3f5b0b97a
title: Метод Кженериклист. GetNext (Вкслист. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList.GetNext
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9491e58d817ce2c9dc4fb59fafa9bf96812a013a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668808"
---
# <a name="cgenericlistgetnext-method"></a>Кженериклист. GetNext, метод

`GetNext`Метод получает элемент в указанной позиции и перемещает позицию.

## <a name="syntax"></a>Синтаксис


```C++
OBJECT* GetNext(
  [ref] POSITION &rp
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*RP* \[ ЗНАЧ\]
</dt> <dd>

Ссылка на значение должности.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает указатель на объект типа **Object** (тип шаблона).

## <a name="remarks"></a>Комментарии

Этот метод перемещает индикатор положения на следующую позицию. Если индикатор позиции перемещается за концом списка, метод присваивает ему **значение NULL**.

Если значение *RP* равно **null**, метод возвращает **значение NULL**.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Вкслист. h (включение Streams. h)</dt> </dl>                                                                                    |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кженериклист**](cgenericlist.md)
</dt> </dl>

 

 




