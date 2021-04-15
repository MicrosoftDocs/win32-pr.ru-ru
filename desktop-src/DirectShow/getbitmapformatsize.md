---
description: Функция Жетбитмапформатсизе вычисляет размер, необходимый для структуры ВИДЕОИНФО, которая может содержать указанную структуру БИТМАПИНФОХЕАДЕР.
ms.assetid: a559415a-070f-4674-be12-a65a46025809
title: Функция Жетбитмапформатсизе (Вксутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetBitmapFormatSize
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 39a64f6d975e403de6c177906b23ef7e09f29ddf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651934"
---
# <a name="getbitmapformatsize-function"></a>Функция Жетбитмапформатсизе

`GetBitmapFormatSize`Функция вычисляет размер, необходимый для структуры [**видеоинфо**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) , которая может содержать указанную структуру [**битмапинфохеадер**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) .

## <a name="syntax"></a>Синтаксис


```C++
LONG GetBitmapFormatSize(
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

## <a name="remarks"></a>Комментарии

За структурой [**битмапинфохеадер**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) могут следовать цветные маски или записи палитры, поэтому может быть трудно определить число байтов, необходимое для создания структуры [**видеоинфо**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) из существующей структуры **битмапинфохеадер** .

Чтобы скопировать структуру [**битмапинфохеадер**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) в структуру [**видеоинфо**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) , используйте макрос [**Header**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-header) , который вычисляет правильное смещение.

## <a name="examples"></a>Примеры


```
LONG size = GetBitmapFormatSize(&bmi);

VIDEOINFO *pVi = static_cast<VIDEOINFO*>(CoTaskMemAlloc(size));

if (pVi != NULL)
{
    CopyMemory(HEADER(pVi), &bmi, sizeof(BITMAPINFOHEADER));
}
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Вксутил. h (включение Streams. h)</dt> </dl>                                                                                    |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Функции видео и изображений](video-and-image-functions.md)
</dt> </dl>

 

 




