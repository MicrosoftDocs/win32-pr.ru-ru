---
description: Метод Онсреадкреате вызывается при инициализации потока потоковой передачи.
ms.assetid: eeaa0d12-3185-4c97-b481-fc420cfc0897
title: Метод Ксаурцестреам. Онсреадкреате (Source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.OnThreadCreate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6e263f0ae72838504ab6d219c71d7841291a3edd2a7d6b719d112c74fb30c23b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119907714"
---
# <a name="csourcestreamonthreadcreate-method"></a>Ксаурцестреам. Онсреадкреате, метод

`OnThreadCreate`Метод вызывается при инициализации потока потоковой передачи.

## <a name="syntax"></a>Синтаксис


```C++
virtual HRESULT OnThreadCreate();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение S \_ ОК.

## <a name="remarks"></a>Remarks

Процедура потока, [**ксаурцестреам:: среадпрок**](csourcestream-threadproc.md), вызывает этот метод при первом получении запроса [**Ксаурцестреам:: init**](csourcestream-init.md) . Метод не выполняет никаких действий в базовом классе. Производный класс может переопределить этот метод для выполнения инициализации потока. Если производный класс возвращает код ошибки, то поток завершается с ошибкой.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>Source. h (включает Потоки. h)</dt> </dl>                                                                                    |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Ксаурцестреам**](csourcestream.md)
</dt> </dl>

 

 




