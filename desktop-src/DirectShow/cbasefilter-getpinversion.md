---
description: Метод Жетпинверсион извлекает номер версии для набора ПИН-кодов в этом фильтре.
ms.assetid: 6cc186b2-4d9f-4d1c-a8b3-975e9c248df7
title: Кбасефилтер. Жетпинверсион, метод (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.GetPinVersion
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2d8cb2e67f88ef7a02958cc851dd9b8c0c751096
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657807"
---
# <a name="cbasefiltergetpinversion-method"></a>Кбасефилтер. Жетпинверсион, метод

`GetPinVersion`Метод извлекает номер версии для набора ПИН-кодов в этом фильтре.

## <a name="syntax"></a>Синтаксис


```C++
virtual long GetPinVersion();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Возвращает переменную члена [**кбасефилтер:: m \_ пинверсион**](cbasefilter-m-pinversion.md) .

## <a name="remarks"></a>Комментарии

Конструктор **кбасефилтер** инициализирует версию ПИН-кода до 1. В базовом классе это число никогда не изменяется. Если фильтр динамически создает или уничтожает ПИН-коды, он должен увеличивать номер версии ПИН при каждом изменении ПИН. Чтобы увеличить номер версии, вызовите метод [**кбасефилтер:: инкрементпинверсион**](cbasefilter-incrementpinversion.md) .

Объект перечислителя PIN-кодов, реализованный классом [**ценумпинс**](cenumpins.md) , использует версию ПИН-кода для синхронизации с фильтром.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Амфилтер. h (включение Streams. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасефилтер**](cbasefilter.md)
</dt> </dl>

 

 




