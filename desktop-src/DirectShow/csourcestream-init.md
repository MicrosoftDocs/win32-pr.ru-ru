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
ms.openlocfilehash: e656ba46b25045406fb794653078b72e2c47155635cf24ae4a99b35238aa51df
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119871321"
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

## <a name="remarks"></a>Remarks

Этот метод должен быть первым запросом потока, отправленным методу [**ксаурцестреам:: среадпрок**](csourcestream-threadproc.md) . Метод [**ксаурцестреам:: Active**](csourcestream-active.md) вызывает этот метод.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>Source. h (включает Потоки. h)</dt> </dl>                                                                                    |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Ксаурцестреам**](csourcestream.md)
</dt> </dl>

 

 




