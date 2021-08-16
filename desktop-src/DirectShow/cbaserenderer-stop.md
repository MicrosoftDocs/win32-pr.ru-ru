---
description: Метод Stop останавливает фильтр.
ms.assetid: 80eac207-5db3-4b06-bbae-eca72e37d09d
title: Метод Кбасерендерер. останавливаться (Ренбасе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.Stop
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 942fae3ee1ea2c7481f475dc2d8dba421fd21d44290c98b822b9bc489ee25334
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117822624"
---
# <a name="cbaserendererstop-method"></a>Кбасерендерер. останавливаться, метод

`Stop`Метод останавливает фильтр.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT Stop();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение S \_ ОК.

## <a name="remarks"></a>Remarks

Этот метод переопределяет метод [**кбасефилтер:: останавливаться**](cbasefilter-stop.md) . Он выполняет следующие действия:

-   Вызывает [**кбасефилтер:: останавливаться**](cbasefilter-stop.md).
-   Отменяет выделение распределителя. (См. раздел [**имемаллокатор::D екоммит**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-decommit).)
-   Отменяет любую запланированную отрисовку и освобождает поток потоковой передачи.
-   Ожидает завершения любого ожидающего вызова **Receive** .

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>ренбасе. h (включает Потоки. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасерендерер**](cbaserenderer.md)
</dt> </dl>

 

 




