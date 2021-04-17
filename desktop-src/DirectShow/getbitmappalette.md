---
description: Функция Жетбитмаппалетте возвращает первую запись Palette в структуре ВИДЕОИНФОХЕАДЕР.
ms.assetid: 7c620f81-31d9-408f-954d-aeff39f93956
title: Функция Жетбитмаппалетте (Вксутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetBitmapPalette
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ffa4139c7aaece3e92a26fbf69fc02b8759f1613
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675530"
---
# <a name="getbitmappalette-function"></a>Функция Жетбитмаппалетте

`GetBitmapPalette`Функция возвращает первую запись Palette в структуре [**видеоинфохеадер**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) .

## <a name="syntax"></a>Синтаксис


```C++
const RGBQUAD* GetBitmapPalette(
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

Возвращает указатель на первую запись в палитре.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Вксутил. h (включение Streams. h)</dt> </dl>                                                                                    |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



 

 




