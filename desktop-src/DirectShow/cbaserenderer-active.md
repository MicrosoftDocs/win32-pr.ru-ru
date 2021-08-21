---
description: Активный метод вызывается при переключении состояния на приостановку или выполнение.
ms.assetid: 2913bc81-572d-4ee1-a1b6-9e1638e04c9d
title: Метод Кбасерендерер. Active (Ренбасе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.Active
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: df5ec659b5e76940ebf279e3feb8995d34380db0543d9eebcf42c1f3bff8c0e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118954973"
---
# <a name="cbaserendereractive-method"></a>Кбасерендерер. активный метод

`Active`Метод вызывается при переключении состояния на приостановку или выполнение.

## <a name="syntax"></a>Синтаксис


```C++
virtual HRESULT Active();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение S \_ ОК.

## <a name="remarks"></a>Remarks

Входной ПИН-код вызывает этот метод из собственного метода [**крендереринпутпин:: Active**](crendererinputpin-active.md) . Этот метод не выполняет никаких действий в базовом классе.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>ренбасе. h (включает Потоки. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Кбасерендерер**](cbaserenderer.md)
</dt> </dl>

 

 




