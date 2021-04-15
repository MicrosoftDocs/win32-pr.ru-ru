---
description: Метод Жетнексти извлекает элемент в указанной позиции и перемещает позицию.
ms.assetid: 3ec217ec-b0f9-4ff4-bdb7-ac204df99010
title: Кбаселист. Жетнексти, метод (Вкслист. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.GetNextI
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f96be8d8cdf286a4017e56af7050970d45e8a56e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668603"
---
# <a name="cbaselistgetnexti-method"></a>Кбаселист. Жетнексти, метод

`GetNextI`Метод получает элемент в указанной позиции и перемещает позицию.

## <a name="syntax"></a>Синтаксис


```C++
void* GetNextI(
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

Возвращает указатель на элемент. Если значение *RP* равно **null**, метод возвращает **значение NULL**.

## <a name="remarks"></a>Комментарии

Этот метод перемещает индикатор положения на следующую позицию. Если индикатор позиции перемещается за концом списка, метод присваивает ему **значение NULL**.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Вкслист. h (включение Streams. h)</dt> </dl>                                                                                    |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбаселист**](cbaselist.md)
</dt> </dl>

 

 




