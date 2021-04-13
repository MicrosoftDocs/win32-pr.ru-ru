---
description: Метод Инкремементпинверсион увеличивает номер версии в наборе ПИН-кодов.
ms.assetid: e1b3ec33-104d-4a12-9b11-f8bea09690a7
title: Кбасефилтер. Инкрементпинверсион, метод (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.IncrementPinVersion
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 53e66ccd5bdd34c4767001403439f4372ff2938a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657802"
---
# <a name="cbasefilterincrementpinversion-method"></a>Кбасефилтер. Инкрементпинверсион, метод

`IncremementPinVersion`Метод увеличивает номер версии набора ПИН-кодов.

## <a name="syntax"></a>Синтаксис


```C++
void IncrementPinVersion();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Комментарии

Этот метод увеличивает значение переменной члена [**кбасефилтер:: m \_ пинверсион**](cbasefilter-m-pinversion.md) . Если фильтр динамически создает или уничтожает ПИН-коды, вызывайте этот метод при каждом изменении ПИН-кода.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Амфилтер. h (включение Streams. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасефилтер**](cbasefilter.md)
</dt> <dt>

[**Кбасефилтер:: Жетпинверсион**](cbasefilter-getpinversion.md)
</dt> </dl>

 

 




