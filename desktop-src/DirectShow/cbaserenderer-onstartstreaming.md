---
description: Метод Онстартстреаминг вызывается, когда фильтр начинает потоковую передачу.
ms.assetid: 02a5b334-f6c4-4cba-8882-c6b36d97feb3
title: Кбасерендерер. Онстартстреаминг, метод (Ренбасе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.OnStartStreaming
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1b0f050222b0ca6a88c7cf1d9348597e4d7b68f2a2ed431b4f6843afe97efd5b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118157677"
---
# <a name="cbaserendereronstartstreaming-method"></a>Кбасерендерер. Онстартстреаминг, метод

`OnStartStreaming`Метод вызывается, когда фильтр начинает потоковую передачу.

## <a name="syntax"></a>Синтаксис


```C++
virtual HRESULT OnStartStreaming();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение S \_ ОК.

## <a name="remarks"></a>Remarks

Метод [**кбасерендерер:: стартстреаминг**](cbaserenderer-startstreaming.md) вызывает этот метод. Он не выполняет никаких действий в базовом классе, но производный класс может его переопределить.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>ренбасе. h (включает Потоки. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Кбасерендерер**](cbaserenderer.md)
</dt> </dl>

 

 




