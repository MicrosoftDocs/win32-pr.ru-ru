---
description: 'Метод Куеридиректион извлекает направление ПИН-кода (ввод или вывод). Этот метод реализует метод Ипин:: Куеридиректион.'
ms.assetid: c28332dc-5ac4-4c89-98b4-281424f36ba9
title: Кбасепин. Куеридиректион, метод (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.QueryDirection
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7e2ebfaa3d12b5f582b4b67014280fa0a0d5299d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668545"
---
# <a name="cbasepinquerydirection-method"></a>Кбасепин. Куеридиректион, метод

`QueryDirection`Метод получает направление ПИН-кода (ввод или вывод). Этот метод реализует метод [**Ипин:: куеридиректион**](/windows/desktop/api/Strmif/nf-strmif-ipin-querydirection) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT QueryDirection(
   PIN_DIRECTION *pPinDir
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ппиндир* 
</dt> <dd>

Указатель на переменную, которая получает элемент перечисляемого [**типа \_ направления**](/windows/win32/api/strmif/ne-strmif-pin_direction) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение S \_ (ОК) или \_ указатель E.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Амфилтер. h (включение Streams. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасепин**](cbasepin.md)
</dt> </dl>

 

 




