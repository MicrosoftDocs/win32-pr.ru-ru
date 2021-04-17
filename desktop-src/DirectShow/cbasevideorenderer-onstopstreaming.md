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
ms.openlocfilehash: 08cf23fd2e1a7e854625d8a369d15290591386fe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675009"
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

## <a name="remarks"></a>Комментарии

Эта функция-член вызывается дважды, один раз при приостановке и снова, когда поток фактически останавливается.

Эта функция члена переопределяет [**кбасерендерер:: онстопстреаминг**](cbaserenderer-onstopstreaming.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ренбасе. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасевидеорендерер**](cbasevideorenderer.md)
</dt> </dl>

 

 




