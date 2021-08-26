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
ms.openlocfilehash: 4c5b7548eca20f9ec6d9e03d0e708ead1b106f543ca8cac108700c64c9352ea3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120087084"
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

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>Source. h (включает Потоки. h)</dt> </dl>                                                                                    |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Ксаурце**](csource.md)
</dt> </dl>

 

 




