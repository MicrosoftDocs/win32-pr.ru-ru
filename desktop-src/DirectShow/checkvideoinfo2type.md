---
description: Функция CheckVideoInfo2Type проверяет тип носителя, содержащий структуру формата VIDEOINFOHEADER2, для некоторых распространенных ошибок, которые могут привести к переполнению буфера или переполнению целочисленных значений.
ms.assetid: 6a71ce7e-c6fc-4811-9182-67949644a0a5
title: Функция CheckVideoInfo2Type (Чеккбми. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CheckVideoInfo2Type
api_type:
- HeaderDef
api_location:
- checkbmi.h
ms.openlocfilehash: 5ec092bdea1e3dd00de36893d1816f70ca6d7945
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675830"
---
# <a name="checkvideoinfo2type-function"></a>Функция CheckVideoInfo2Type

`CheckVideoInfo2Type`Функция проверяет тип мультимедиа, содержащий структуру формата [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) для некоторых распространенных ошибок, которые могут привести к переполнению буфера или переполнению целочисленных значений.

> [!Note]  
> Эта функция не гарантирует, что тип носителя является допустимым или что код, использующий структуру, является безопасным.

 

## <a name="syntax"></a>Синтаксис


```C++
HRESULT CheckVideoInfo2Type(
   const AM_MEDIA_TYPE *pmt
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*состоит* 
</dt> <dd>

Указатель на структуру [**\_ \_ типа мультимедиа AM**](/windows/win32/api/strmif/ns-strmif-am_media_type) для проверки.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает одно из следующих значений **HRESULT** .



| Код возврата                                                                                                | Описание                       |
|------------------------------------------------------------------------------------------------------------|-----------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl>                       | Успешно<br/>                |
| <dl> <dt>**\_указатель E**</dt> </dl>                  | Значение указателя **null**<br/> |
| <dl> <dt>**\_тип VFW \_ E \_ не \_ принят**</dt> </dl> | Недопустимый тип носителя<br/>     |



 

## <a name="remarks"></a>Комментарии

Эта функция вызывает [**валидатебитмапинфохеадер**](validatebitmapinfoheader.md) для проверки структуры [**битмапинфохеадер**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) в типе мультимедиа. Если тип формата отличается от **Format \_ VideoInfo2**, функция возвращает **\_ тип VFW E \_ \_ не \_ принято**.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Чеккбми. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Функции видео и изображений](video-and-image-functions.md)
</dt> </dl>

 

 




