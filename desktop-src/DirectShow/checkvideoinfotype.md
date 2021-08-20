---
description: Функция Чекквидеоинфотипе проверяет тип носителя, содержащий структуру формата ВИДЕОИНФОХЕАДЕР, для некоторых распространенных ошибок, которые могут привести к переполнению буфера или переполнению целочисленных значений.
ms.assetid: 7ffca7de-26f9-4d8d-b70e-231eca462211
title: Функция Чекквидеоинфотипе (Чеккбми. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CheckVideoInfoType
api_type:
- HeaderDef
api_location:
- checkbmi.h
ms.openlocfilehash: 4463a1edb2002f64e983a38eb4a0ace5b5289b4d47ac43c8ea27bf165138ff95
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119539544"
---
# <a name="checkvideoinfotype-function"></a>Функция Чекквидеоинфотипе

`CheckVideoInfoType`Функция проверяет тип мультимедиа, содержащий структуру формата [**видеоинфохеадер**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) для некоторых распространенных ошибок, которые могут привести к переполнению буфера или переполнению целочисленных значений.

> [!Note]  
> Эта функция не гарантирует, что тип носителя является допустимым или что код, использующий структуру, является безопасным.

 

## <a name="syntax"></a>Синтаксис


```C++
HRESULT CheckVideoInfoType(
   const AM_MEDIA_TYPE *pmt
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*состоит* 
</dt> <dd>

Указатель на структуру [**\_ \_ типа мультимедиа AM**](/windows/win32/api/strmif/ns-strmif-am_media_type) для проверки

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает одно из следующих значений **HRESULT** .



| Код возврата                                                                                                | Описание                        |
|------------------------------------------------------------------------------------------------------------|------------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl>                       | Успешно.<br/>                |
| <dl> <dt>**\_указатель E**</dt> </dl>                  | Значение указателя **null** .<br/> |
| <dl> <dt>**\_тип VFW \_ E \_ не \_ принят**</dt> </dl> | Недопустимый тип носителя.<br/>     |



 

## <a name="remarks"></a>Remarks

Эта функция вызывает [**валидатебитмапинфохеадер**](validatebitmapinfoheader.md) для проверки структуры [**битмапинфохеадер**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) в типе мультимедиа. Если тип формата отличается от FORMAT \_ видеоинфо, функция возвращает \_ тип VFW E \_ \_ не \_ принято.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------|---------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>Чеккбми. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Функции видео и изображений](video-and-image-functions.md)
</dt> </dl>

 

 




