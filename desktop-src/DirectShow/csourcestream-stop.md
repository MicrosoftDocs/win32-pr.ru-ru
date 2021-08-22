---
description: Метод «завершение» сигнализирует потоку потоковой передачи на завершение.
ms.assetid: 79bc528a-cf53-43f3-aa17-c459063c99ab
title: Метод Ксаурцестреам. останавливаться (Source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.Stop
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7ac5eb7d6b066920210d4f955084afa46ddc71d1c17820fe0300acc66b53bb8c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119073168"
---
# <a name="csourcestreamstop-method"></a>Ксаурцестреам. останавливаться, метод

`Stop`Метод сигнализирует потоку потоковой передачи на завершение.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT Stop();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Непредвиденное значение: S \_ (ОК или E) \_ .

## <a name="remarks"></a>Remarks

Метод [**ксаурцестреам:: Inactive**](csourcestream-inactive.md) вызывает этот метод.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>Source. h (включает Потоки. h)</dt> </dl>                                                                                    |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Ксаурцестреам**](csourcestream.md)
</dt> </dl>

 

 




