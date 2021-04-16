---
description: Функция Фримедиатипе удаляет блок формата в \_ \_ структуре типа мультимедиа AM.
ms.assetid: b7ec335e-518d-4aa6-8cde-8cb92184d0b0
title: Функция Фримедиатипе (Мтипе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FreeMediaType
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9f332ccc9a60473a9d814481b759221dc6468d5c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679689"
---
# <a name="freemediatype-function"></a>Функция Фримедиатипе

Функция **фримедиатипе** удаляет блок формата в структуре [**\_ \_ типа мультимедиа AM**](/windows/win32/api/strmif/ns-strmif-am_media_type) .

## <a name="syntax"></a>Синтаксис


```C++
void FreeMediaType(
   AM_MEDIA_TYPE &mt
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*MT* \[ ЗНАЧ\]
</dt> <dd>

Ссылка на структуру [**\_ \_ типа мультимедиа AM**](/windows/win32/api/strmif/ns-strmif-am_media_type) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Эта функция не возвращает значение.

## <a name="remarks"></a>Комментарии

Блок формата выделяется в куче. Элемент **пбформат** [**\_ \_ типа носителя AM**](/windows/win32/api/strmif/ns-strmif-am_media_type) указывает на блок формата. Используйте эту функцию, чтобы освободить только блок формата. Чтобы удалить выделенную **структуру \_ \_ типа носителя** , вызовите [**делетемедиатипе**](deletemediatype.md).

Эта функция определена в библиотеке [базовых классов DirectShow](directshow-base-classes.md) . Если вы предпочитаете не ссылаться на библиотеку базовых классов, можно использовать следующий код:


```C++
// Release the format block for a media type.

void _FreeMediaType(AM_MEDIA_TYPE& mt)
{
    if (mt.cbFormat != 0)
    {
        CoTaskMemFree((PVOID)mt.pbFormat);
        mt.cbFormat = 0;
        mt.pbFormat = NULL;
    }
    if (mt.pUnk != NULL)
    {
        // pUnk should not be used.
        mt.pUnk->Release();
        mt.pUnk = NULL;
    }
}
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Мтипе. h (включение Streams. h)</dt> </dl>                                                                                     |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**делетемедиатипе**](deletemediatype.md)
</dt> <dt>

[**Функции типа мультимедиа**](media-type-functions.md)
</dt> </dl>

 

 




