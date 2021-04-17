---
description: Метод размещения \_ CurrentPosition задает текущую точку относительно общей продолжительности потока. Этот метод реализует метод Имедиапоситион::p UT \_ CurrentPosition.
ms.assetid: 22d7e9e4-47da-45b5-9be0-3c5128f90353
title: Метод CPosPassThru.put_CurrentPosition (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.put_CurrentPosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 85426636a34d0e197b36496d5a38a847c61b9501
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679964"
---
# <a name="cpospassthruput_currentposition-method"></a>Кпоспасссру. размещение \_ метода CurrentPosition

`put_CurrentPosition`Метод задает текущую точку относительно общей продолжительности потока. Этот метод реализует метод [**имедиапоситион::p UT \_ CurrentPosition**](/windows/desktop/api/Control/nf-control-imediaposition-put_currentposition) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT put_CurrentPosition(
   REFTIME llTime
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ллтиме* 
</dt> <dd>

Новое расположение в секундах.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение **HRESULT** из подключенного ПИН-кода.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ктлутил. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кпоспасссру**](cpospassthru.md)
</dt> </dl>

 

 




