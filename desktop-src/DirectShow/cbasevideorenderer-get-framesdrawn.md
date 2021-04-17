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
ms.openlocfilehash: ec8254e06429022bf657322e98ab317475c82f90
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675213"
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

## <a name="remarks"></a>Комментарии

Эта функция члена реализует метод [**икуалпроп:: Get \_ фрамесдравн**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-iqualprop-get_framesdrawn) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ренбасе. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасевидеорендерер**](cbasevideorenderer.md)
</dt> </dl>

 

 




