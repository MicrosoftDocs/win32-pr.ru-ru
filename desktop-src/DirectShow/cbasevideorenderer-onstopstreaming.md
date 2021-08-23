---
description: Метод Онстопстреаминг вызывается в конце потоковой передачи, чтобы исправить время для отчета страницы свойств.
ms.assetid: 92174edb-2f6c-4bad-91c5-769aaebcc495
title: Кбасевидеорендерер. Онстопстреаминг, метод (Ренбасе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.OnStopStreaming
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 38e1e3fef83bab4d598cfd36294c5c405c1eca938372b43f12a6401c4be3c46b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119586044"
---
# <a name="cbasevideorendereronstopstreaming-method"></a>Кбасевидеорендерер. Онстопстреаминг, метод

`OnStopStreaming`Метод вызывается в конце потоковой передачи, чтобы исправить время для отчета страницы свойств.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT OnStopStreaming();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение **HRESULT** .

## <a name="remarks"></a>Remarks

Эта функция-член вызывается дважды, один раз при приостановке и снова, когда поток фактически останавливается.

Эта функция члена переопределяет [**кбасерендерер:: онстопстреаминг**](cbaserenderer-onstopstreaming.md).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>ренбасе. h (включает Потоки. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Кбасевидеорендерер**](cbasevideorenderer.md)
</dt> </dl>

 

 




