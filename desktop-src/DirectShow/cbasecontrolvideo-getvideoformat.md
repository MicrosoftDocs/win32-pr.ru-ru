---
description: Метод Жетвидеоформат извлекает образец видео, представляющий текущий формат видео.
ms.assetid: f7457c5b-037c-4a63-963e-0fc6086609a4
title: Кбасеконтролвидео. Жетвидеоформат, метод (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.GetVideoFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d84b64818a02a60073fc21411e4a99bde07a6e00
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657895"
---
# <a name="cbasecontrolvideogetvideoformat-method"></a>Кбасеконтролвидео. Жетвидеоформат, метод

`GetVideoFormat`Метод получает образец видео, представляющий текущий формат видео.

## <a name="syntax"></a>Синтаксис


```C++
virtual VIDEOINFOHEADER* GetVideoFormat() = 0;
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Возвращает указатель на структуру [**видеоинфохеадер**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) , содержащую текущий формат видео.

## <a name="remarks"></a>Комментарии

Чтобы вернуть и проверить определенную информацию с помощью [**ибасиквидео**](/windows/desktop/api/Control/nn-control-ibasicvideo), объект должен узнать текущий формат видео. Он получает эти сведения путем вызова чистого виртуального метода, который производные классы должны переопределить. Эта функция-член вызывается следующими функциями-членами [**кбасеконтролвидео**](cbasecontrolvideo.md) .

-   [**Кбасеконтролвидео:: Онвидеосизечанже**](cbasecontrolvideo-onvideosizechange.md)
-   [**Кбасеконтролвидео:: Get \_ авгтимеперфраме**](cbasecontrolvideo-get-avgtimeperframe.md)
-   [**Кбасеконтролвидео:: получить \_ скорость**](cbasecontrolvideo-get-bitrate.md)
-   [**Кбасеконтролвидео:: Get \_ битерроррате**](cbasecontrolvideo-get-biterrorrate.md)
-   [**Кбасеконтролвидео:: Get \_ видеовидс**](cbasecontrolvideo-get-videowidth.md)
-   [**Кбасеконтролвидео:: Get \_ видеохеигхт**](cbasecontrolvideo-get-videoheight.md)
-   [**Кбасеконтролвидео:: Жетвидеопалеттинтриес**](cbasecontrolvideo-getvideopaletteentries.md)
-   [**Кбасеконтролвидео:: Жетвидеосизе**](cbasecontrolvideo-getvideosize.md)

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ктлутил. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасеконтролвидео**](cbasecontrolvideo.md)
</dt> </dl>

 

 




