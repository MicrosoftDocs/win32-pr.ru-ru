---
description: Функция Креатемедиатипе выделяет новую \_ \_ структуру типа мультимедиа am, включая блок Format.
ms.assetid: 841a8c51-6027-49d6-b3d8-b5e21e3d5f13
title: Функция Креатемедиатипе (Мтипе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreateMediaType
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 03ea3eaee03ebf98ac22d702bde9a165fda21e51
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679677"
---
# <a name="createmediatype-function"></a>Функция Креатемедиатипе

Функция **креатемедиатипе** выделяет новую структуру [**\_ \_ типа мультимедиа AM**](/windows/win32/api/strmif/ns-strmif-am_media_type) , включая блок Format.

## <a name="syntax"></a>Синтаксис


```C++
AM_MEDIA_TYPE* WINAPI CreateMediaType(
   AM_MEDIA_TYPE const *pSrc
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*pSrc* 
</dt> <dd>

Указатель на структуру [**\_ \_ типа мультимедиа AM**](/windows/win32/api/strmif/ns-strmif-am_media_type) . Метод копирует эту структуру в новую структуру.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает новую структуру [**\_ \_ типа мультимедиа AM**](/windows/win32/api/strmif/ns-strmif-am_media_type) или **значение NULL** , если возникает ошибка.

## <a name="remarks"></a>Комментарии

Чтобы освободить память, выделенную этой функцией, вызовите [**делетемедиатипе**](deletemediatype.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Мтипе. h (включение Streams. h)</dt> </dl>                                                                                     |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Функции типа мультимедиа**](media-type-functions.md)
</dt> </dl>

 

 




