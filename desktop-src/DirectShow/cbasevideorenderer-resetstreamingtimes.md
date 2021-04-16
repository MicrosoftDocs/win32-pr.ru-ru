---
description: Метод Ресетстреамингтимес сбрасывает все значения времени, которые управляют потоковой передачей.
ms.assetid: 8a596760-a45a-4486-bb91-aab10bbf927f
title: Кбасевидеорендерер. Ресетстреамингтимес, метод (Ренбасе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.ResetStreamingTimes
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d887ca9e246d5e3fb746c119b1ed6784201ec702
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105656964"
---
# <a name="cbasevideorendererresetstreamingtimes-method"></a>Кбасевидеорендерер. Ресетстреамингтимес, метод

`ResetStreamingTimes`Метод сбрасывает все значения времени, которые управляют потоковой передачей.

## <a name="syntax"></a>Синтаксис


```C++
virtual HRESULT ResetStreamingTimes();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение **HRESULT** .

## <a name="remarks"></a>Комментарии

Время задается таким образом, чтобы фреймы не удалялись изначально, а первый кадр был нарисован.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ренбасе. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасевидеорендерер**](cbasevideorenderer.md)
</dt> </dl>

 

 




