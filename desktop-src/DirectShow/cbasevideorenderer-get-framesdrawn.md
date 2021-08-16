---
description: Метод Get \_ фрамесдравн извлекает \_ переменную члена m кфрамесдравн, выдавая число кадров, рисуемых после начала потоковой передачи.
ms.assetid: 486b5541-2952-47ce-944e-4efb8e5af9dd
title: Метод CBaseVideoRenderer.get_FramesDrawn (Ренбасе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.get_FramesDrawn
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 65a7c698d129a3606f6ba75f856289ca2b4e15c438d3890eb0a97e4a198ee808
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117822587"
---
# <a name="cbasevideorendererget_framesdrawn-method"></a>Кбасевидеорендерер. Get \_ фрамесдравн, метод

`get_FramesDrawn`Метод получает переменную члена **m \_ кфрамесдравн** , выдавая число кадров, созданных с момента начала потоковой передачи.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT get_FramesDrawn(
   int *pcFramesDrawn
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пкфрамесдравн* 
</dt> <dd>

Указатель на число рисуемых кадров.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение **HRESULT** .

## <a name="remarks"></a>Remarks

Эта функция члена реализует метод [**икуалпроп:: Get \_ фрамесдравн**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-iqualprop-get_framesdrawn) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>ренбасе. h (включает Потоки. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасевидеорендерер**](cbasevideorenderer.md)
</dt> </dl>

 

 




