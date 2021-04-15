---
description: Метод Pause сигнализирует потоку потоковой передачи на активное выполнение.
ms.assetid: c97da113-c5a7-422d-9215-70b556e0b8ca
title: Метод Ксаурцестреам. Pause (Source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.Pause
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b6f7cd3b38144edebd98ca655b32bf6092f44269
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105676003"
---
# <a name="csourcestreampause-method"></a>Ксаурцестреам. Pause, метод

`Pause`Метод сигнализирует потоку потоковой передачи на активность.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT Pause();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Непредвиденное значение: S \_ (ОК или E) \_ .

## <a name="remarks"></a>Комментарии

Метод [**ксаурцестреам:: Active**](csourcestream-active.md) вызывает этот метод. Когда метод [**ксаурцестреам:: среадпрок**](csourcestream-threadproc.md) получает этот запрос, он вызывает метод [**Ксаурцестреам::D обуфферпроцессинглуп**](csourcestream-dobufferprocessingloop.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Source. h (включение Streams. h)</dt> </dl>                                                                                    |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Ксаурцестреам**](csourcestream.md)
</dt> </dl>

 

 




