---
description: Функция Контаинспалетте определяет, содержит ли указанная структура ВИДЕОИНФОХЕАДЕР палитру.
ms.assetid: e87ab1af-a822-45d8-9326-08b450e11279
title: Функция Контаинспалетте (Вксутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ContainsPalette
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6c9e5ab793dfaadb868cc09cfbe25e59c02dc338b470992b81ab1990581e5c19
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118954173"
---
# <a name="containspalette-function"></a>Функция Контаинспалетте

Функция **контаинспалетте** определяет, содержит ли указанная структура [**видеоинфохеадер**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) палитру.

## <a name="syntax"></a>Синтаксис


```C++
BOOL ContainsPalette(
   const VIDEOINFOHEADER *pVideoInfo

);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пвидеоинфо* 
</dt> <dd>

Указатель на структуру [**видеоинфохеадер**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение true** , если значение битдепс равно 8 или меньше (**бмихеадер. бибиткаунт**), или количество цветовых индексов больше нуля (**бмихеадер. биклрусед**). В противном случае возвращает **false** .

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>вксутил. h (включает Потоки. h)</dt> </dl>                                                                                    |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Функции видео и изображений](video-and-image-functions.md)
</dt> </dl>

 

 




