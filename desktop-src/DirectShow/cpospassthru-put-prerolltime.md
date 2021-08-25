---
description: Метод размещения \_ прероллтиме задает объем данных, которые будут помещены в очередь перед начальной позицией. Этот метод реализует метод Имедиапоситион::p UT \_ прероллтиме.
ms.assetid: 5c35fb1d-2296-493f-8104-601127d7dd9f
title: Метод CPosPassThru.put_PrerollTime (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.put_PrerollTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 825c3c584fc6db7eb9f94b4e8d01e003f5cf6c36ff8adac4041fd48f792ca858
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119909204"
---
# <a name="cpospassthruput_prerolltime-method"></a>Кпоспасссру. размещение \_ метода прероллтиме

`put_PrerollTime`Метод задает объем данных, которые будут помещены в очередь перед начальной позицией. Этот метод реализует метод [**имедиапоситион::p UT \_ прероллтиме**](/windows/desktop/api/Control/nf-control-imediaposition-put_prerolltime) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT put_PrerollTime(
   REFTIME llTime
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ллтиме* 
</dt> <dd>

Время в секундах.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение **HRESULT** из подключенного ПИН-кода.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>ктлутил. h (включает Потоки. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Кпоспасссру**](cpospassthru.md)
</dt> </dl>

 

 




