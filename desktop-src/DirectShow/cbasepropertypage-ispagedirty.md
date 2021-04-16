---
description: 'Метод Испажедирти указывает, изменилась ли страница свойств с момента ее активации или последнего вызова метода Ипропертипаже:: Apply. Этот метод реализует метод Ипропертипаже:: Испажедирти.'
ms.assetid: 95eeec26-7dbb-4add-a827-6505b40afe48
title: Кбасепропертипаже. Испажедирти, метод (Кпроп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.IsPageDirty
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c69c2e7d480f63542e146c73e56b9e692693f665
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657714"
---
# <a name="cbasepropertypageispagedirty-method"></a>Кбасепропертипаже. Испажедирти, метод

`IsPageDirty`Метод указывает, изменилась ли страница свойств с момента ее активации или последнего вызова метода **ипропертипаже:: Apply**. Этот метод реализует метод **ипропертипаже:: испажедирти** .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT IsPageDirty();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение S \_ ОК, если [**кбасепропертипаже:: m \_ Бдирти**](cbasepropertypage-m-bdirty.md) имеет **значение true**, или \_ false в противном случае.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Кпроп. h (включение Streams. h)</dt> </dl>                                                                                     |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасепропертипаже**](cbasepropertypage.md)
</dt> </dl>

 

 




