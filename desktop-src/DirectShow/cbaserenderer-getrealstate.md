---
description: Метод Жетреалстате Извлекает состояние фильтра.
ms.assetid: d31c5c0b-6220-4d2e-a81a-d16b7d513c87
title: Кбасерендерер. Жетреалстате, метод (Ренбасе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.GetRealState
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0c65ac4310abddc619296776981040cc5e1e6c5ad48ce37ea24210bc5a85d94b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118403423"
---
# <a name="cbaserenderergetrealstate-method"></a>Кбасерендерер. Жетреалстате, метод

`GetRealState`Метод получает состояние фильтра.

## <a name="syntax"></a>Синтаксис


```C++
FILTER_STATE GetRealState();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение [**\_ состояния кбасефилтер:: m**](cbasefilter-m-state.md). Значение является членом перечисляемого типа [**\_ состояния фильтра**](/windows/win32/api/strmif/ne-strmif-filter_state) .

## <a name="remarks"></a>Remarks

Этот метод предоставляет более простую альтернативу методу [**кбасерендерер::-State**](cbaserenderer-getstate.md) для внутреннего использования.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>ренбасе. h (включает Потоки. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасерендерер**](cbaserenderer.md)
</dt> </dl>

 

 




