---
description: Неактивный метод вызывается при переключении состояния на Stopped.
ms.assetid: 2bad81ef-d2a4-4c20-a49b-e40e5097b430
title: Метод Кбасерендерер. Inactive (Ренбасе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.Inactive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e84afd1d4e4ffb013a2029f7d56a223f0aef2f019bc3beb11bd7bd6c202b88d8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119652404"
---
# <a name="cbaserendererinactive-method"></a>Кбасерендерер. Inactive, метод

`Inactive`Метод вызывается при переключении состояния на Stopped.

## <a name="syntax"></a>Синтаксис


```C++
virtual HRESULT Inactive();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение S \_ ОК.

## <a name="remarks"></a>Remarks

Входной ПИН-код вызывает этот метод из собственного метода [**крендереринпутпин:: Inactive**](crendererinputpin-inactive.md) . Фильтр вызывает метод [**кбасерендерер:: клеарпендингсампле**](cbaserenderer-clearpendingsample.md) , чтобы освободить самый последний пример.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>ренбасе. h (включает Потоки. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасерендерер**](cbaserenderer.md)
</dt> </dl>

 

 




