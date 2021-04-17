---
description: 'Метод Жетпин извлекает ПИН-код. Этот метод реализует чистый виртуальный метод Кбасефилтер:: Жетпин.'
ms.assetid: 7f30a1ba-8e7b-4bde-9f4d-a85b3a2122e9
title: Метод Ксаурце. Жетпин (Source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSource.GetPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f11ff79c9d2d535a3370183b7f36bae25c5e1383
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665445"
---
# <a name="csourcegetpin-method"></a>Ксаурце. Жетпин, метод

`GetPin`Метод извлекает ПИН-код. Этот метод реализует чистый виртуальный метод [**кбасефилтер:: жетпин**](cbasefilter-getpin.md) .

## <a name="syntax"></a>Синтаксис


```C++
CBasePin* GetPin(
   int n
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*n* 
</dt> <dd>

Номер указанного пин-кода.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает указатель на объект [**кбасепин**](cbasepin.md) , который реализует ПИН-код, или **значение NULL** , если индекс выходит за пределы диапазона.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Source. h (включение Streams. h)</dt> </dl>                                                                                    |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Ксаурце**](csource.md)
</dt> </dl>

 

 




