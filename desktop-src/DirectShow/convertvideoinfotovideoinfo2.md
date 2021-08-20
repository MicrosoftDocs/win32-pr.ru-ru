---
description: Функция ConvertVideoInfoToVideoInfo2 преобразует тип мультимедиа, который использует ВИДЕОИНФОХЕАДЕР, в тот, который использует VIDEOINFOHEADER2.
ms.assetid: d938bfc0-a5ae-475b-b183-56ff39b4bae1
title: Функция ConvertVideoInfoToVideoInfo2 (Винутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConvertVideoInfoToVideoInfo2
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3f1865652edf01a612ba7d1a46520f92a8461c9ba53a80395e27e6252e0018ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119073768"
---
# <a name="convertvideoinfotovideoinfo2-function"></a>Функция ConvertVideoInfoToVideoInfo2

`ConvertVideoInfoToVideoInfo2`Функция преобразует тип мультимедиа, который использует [**видеоинфохеадер**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) , в один, использующий [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2).

## <a name="syntax"></a>Синтаксис


```C++
HRESULT STDAPI ConvertVideoInfoToVideoInfo2(
   AM_MEDIA_TYPE *pmt
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*состоит* 
</dt> <dd>

Указатель на преобразуемую структуру [**\_ \_ типа файлов мультимедиа**](/windows/win32/api/strmif/ns-strmif-am_media_type) . Структура должна иметь формат типа Format \_ видеоинфо.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает S \_ OK или E \_ OUTOFMEMORY.

## <a name="remarks"></a>Remarks

Эта функция выделяет новую структуру **VIDEOINFOHEADER2** , копирует члены структуры **видеоинфохеадер** в нее и заменяет старую структуру новой структурой в блоке формата типа мультимедиа.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>винутил. h (включает Потоки. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Функции видео и изображений](video-and-image-functions.md)
</dt> </dl>

 

 




