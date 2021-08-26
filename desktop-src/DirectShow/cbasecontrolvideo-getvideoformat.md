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
ms.openlocfilehash: e37a59b8d002a9c081de74c4974dca1f86d1c9d0a5f7f7b0caca11be6c026d3f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120052774"
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

## <a name="remarks"></a>Remarks

Чтобы вернуть и проверить определенную информацию с помощью [**ибасиквидео**](/windows/desktop/api/Control/nn-control-ibasicvideo), объект должен узнать текущий формат видео. Он получает эти сведения путем вызова чистого виртуального метода, который производные классы должны переопределить. Эта функция-член вызывается следующими функциями-членами [**кбасеконтролвидео**](cbasecontrolvideo.md) .

-   [**Кбасеконтролвидео:: Онвидеосизечанже**](cbasecontrolvideo-onvideosizechange.md)
-   [**Кбасеконтролвидео:: Get \_ авгтимеперфраме**](cbasecontrolvideo-get-avgtimeperframe.md)
-   [**Кбасеконтролвидео:: получить \_ скорость**](cbasecontrolvideo-get-bitrate.md)
-   [**Кбасеконтролвидео:: Get \_ битерроррате**](cbasecontrolvideo-get-biterrorrate.md)
-   [**Кбасеконтролвидео:: Get \_ видеовидс**](cbasecontrolvideo-get-videowidth.md)
-   [**Кбасеконтролвидео:: Get \_ видеохеигхт**](cbasecontrolvideo-get-videoheight.md)
-   [**Кбасеконтролвидео:: Жетвидеопалеттинтриес**](cbasecontrolvideo-getvideopaletteentries.md)
-   [**Кбасеконтролвидео:: Жетвидеосизе**](cbasecontrolvideo-getvideosize.md)

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>ктлутил. h (включает Потоки. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Кбасеконтролвидео**](cbasecontrolvideo.md)
</dt> </dl>

 

 




