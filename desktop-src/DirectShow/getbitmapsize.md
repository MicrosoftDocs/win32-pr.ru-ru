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
ms.openlocfilehash: 5d736e0fa0766f1776fc53c39237242017de988050a469f4f16102d124d6f5f1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118000266"
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
| Заголовок<br/>  | <dl> <dt>вксутил. h (включает Потоки. h)</dt> </dl>                                                                                    |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Функции видео и изображений](video-and-image-functions.md)
</dt> </dl>

 

 




