---
description: Метод Онсреаддестрой вызывается, когда поток потоковой передачи собирается завершить работу.
ms.assetid: a484b6d2-bce6-4a42-9176-2a6ce374e28b
title: Метод Ксаурцестреам. Онсреаддестрой (Source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.OnThreadDestroy
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b71bd7ff9da79ed42ad7d36ff176a60687ca5fd0edcd6003d77c20084adc1b84
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118953703"
---
# <a name="csourcestreamonthreaddestroy-method"></a>Ксаурцестреам. Онсреаддестрой, метод

`OnThreadDestroy`Метод вызывается, когда поток потоковой передачи собирается завершить работу.

## <a name="syntax"></a>Синтаксис


```C++
virtual HRESULT OnThreadDestroy();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение S \_ ОК.

## <a name="remarks"></a>Remarks

Процедура потока, [**ксаурцестреам:: среадпрок**](csourcestream-threadproc.md), вызывает этот метод перед выходом. Метод не выполняет никаких действий в базовом классе. Он доступен для переопределения производного класса. Если производный класс возвращает код ошибки, то поток завершается с ошибкой.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>Source. h (включает Потоки. h)</dt> </dl>                                                                                    |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Ксаурцестреам**](csourcestream.md)
</dt> </dl>

 

 




