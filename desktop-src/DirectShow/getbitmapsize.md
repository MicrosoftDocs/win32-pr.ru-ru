---
description: Функция Жетбитмапсизе вычисляет число байтов, необходимых для аппаратно-независимого точечного рисунка (DIB). Эта функция просто вызывает макрос ДИБСИЗЕ.
ms.assetid: ce23cdf2-9804-4d2e-b9ef-16e54b2d571e
title: Функция Жетбитмапсизе (Вксутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetBitmapSize
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 004201cf3ff839aa1301dcfff0240a73a9128e50
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651933"
---
# <a name="getbitmapsize-function"></a>Функция Жетбитмапсизе

`GetBitmapSize`Функция вычисляет число байтов, необходимых для аппаратно-независимого точечного рисунка (DIB). Эта функция просто вызывает макрос [**дибсизе**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-dibsize) .

## <a name="syntax"></a>Синтаксис


```C++
DWORD GetBitmapSize(
   const BITMAPINFOHEADER *pHeader
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*феадер* 
</dt> <dd>

Указатель на структуру [**битмапинфохеадер**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает размер в байтах.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Вксутил. h (включение Streams. h)</dt> </dl>                                                                                    |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Функции видео и изображений](video-and-image-functions.md)
</dt> </dl>

 

 




