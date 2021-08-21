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
ms.openlocfilehash: f116dd1a965145e5bdf4808d25a7406b4709967c5cf971ad3529ae9d301ebc4f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119539744"
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

## <a name="remarks"></a>Remarks

Этот метод перемещает индикатор положения на следующую позицию. Если индикатор позиции перемещается за концом списка, метод присваивает ему **значение NULL**.

Если значение *RP* равно **null**, метод возвращает **значение NULL**.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>вкслист. h (включает Потоки. h)</dt> </dl>                                                                                    |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Кженериклист**](cgenericlist.md)
</dt> </dl>

 

 




