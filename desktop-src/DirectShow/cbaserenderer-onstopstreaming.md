---
description: Метод Онстопстреаминг вызывается, когда фильтр останавливает потоковую передачу.
ms.assetid: d882fec8-09e1-4d36-a09c-44568e743da3
title: Кбасерендерер. Онстопстреаминг, метод (Ренбасе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.OnStopStreaming
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5c61490a0719ce45d9776982b9230734d1126cef747330bb595c205500aca331
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118157667"
---
# <a name="cbaserendereronstopstreaming-method"></a>Кбасерендерер. Онстопстреаминг, метод

`OnStopStreaming`Метод вызывается, когда фильтр останавливает потоковую передачу.

## <a name="syntax"></a>Синтаксис


```C++
virtual HRESULT OnStopStreaming();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение S \_ ОК.

## <a name="remarks"></a>Remarks

Метод [**кбасерендерер:: стопстреаминг**](cbaserenderer-stopstreaming.md) вызывает этот метод. Он не выполняет никаких действий в базовом классе, но производный класс может его переопределить.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>ренбасе. h (включает Потоки. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Кбасерендерер**](cbaserenderer.md)
</dt> </dl>

 

 




