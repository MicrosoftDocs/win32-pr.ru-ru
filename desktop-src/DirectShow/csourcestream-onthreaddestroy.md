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
ms.openlocfilehash: 3e7377ce11955d7121a33311d390464e042b98f5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657623"
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

## <a name="remarks"></a>Комментарии

Процедура потока, [**ксаурцестреам:: среадпрок**](csourcestream-threadproc.md), вызывает этот метод перед выходом. Метод не выполняет никаких действий в базовом классе. Он доступен для переопределения производного класса. Если производный класс возвращает код ошибки, то поток завершается с ошибкой.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Source. h (включение Streams. h)</dt> </dl>                                                                                    |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Ксаурцестреам**](csourcestream.md)
</dt> </dl>

 

 




