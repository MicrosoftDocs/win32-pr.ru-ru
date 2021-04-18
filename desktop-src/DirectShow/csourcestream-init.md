---
description: Метод init инициализирует поток потоковой передачи.
ms.assetid: c746e595-de97-478c-8b22-5c4dd5594a8f
title: Метод CSourceStream.Init (Source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.Init
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6a3abf2b4637385616862c0613f72afd676f5b79
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689016"
---
# <a name="csourcestreaminit-method"></a>Метод CSourceStream.Init

`Init`Метод инициализирует поток потоковой передачи.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT Init();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Возвращает \_ или другое значение **HRESULT** .

## <a name="remarks"></a>Комментарии

Этот метод должен быть первым запросом потока, отправленным методу [**ксаурцестреам:: среадпрок**](csourcestream-threadproc.md) . Метод [**ксаурцестреам:: Active**](csourcestream-active.md) вызывает этот метод.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Source. h (включение Streams. h)</dt> </dl>                                                                                    |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Ксаурцестреам**](csourcestream.md)
</dt> </dl>

 

 




