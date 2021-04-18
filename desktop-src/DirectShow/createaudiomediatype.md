---
description: Функция Креатеаудиомедиатипе инициализирует тип мультимедиа из структуры ВАВЕФОРМАТЕКС.
ms.assetid: 2571b7b4-86e9-443f-a99d-9ba48f469522
title: Функция Креатеаудиомедиатипе (Мтипе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreateAudioMediaType
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ef4e525762d4b6928e6a9095fad34f3f4f2e96fc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679678"
---
# <a name="createaudiomediatype-function"></a>Функция Креатеаудиомедиатипе

Функция **креатеаудиомедиатипе** инициализирует тип мультимедиа из структуры [**вавеформатекс**](/previous-versions/dd757713(v=vs.85)) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT STDAPI CreateAudioMediaType(
   const WAVEFORMATEX  *pwfx,
         AM_MEDIA_TYPE *pmt,
         BOOL          bSetFormat
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пвфкс* 
</dt> <dd>

Указатель на переданную структуру [**вавеформатекс**](/previous-versions/dd757713(v=vs.85)) .

</dd> <dt>

*состоит* 
</dt> <dd>

Указатель на структуру [**\_ \_ типа мультимедиа AM**](/windows/win32/api/strmif/ns-strmif-am_media_type) для инициализации.

</dd> <dt>

*бсетформат* 
</dt> <dd>

Флаг, указывающий, инициализировать ли блок формата. Укажите **значение true** , чтобы инициализировать его, или **false** в противном случае.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение E \_ OUTOFMEMORY, если память не может быть выделена для данных формата. \_ОК в противном случае.

## <a name="remarks"></a>Комментарии

Если параметр *бсетформат* имеет **значение true**, метод выделяет память для блока Format. Если параметр *ПЛТ* уже содержит выделенный блок формата, произойдет утечка памяти. Чтобы избежать утечки памяти, вызовите [**фримедиатипе**](freemediatype.md) перед вызовом этой функции. После возврата метода вызовите **фримедиатипе** еще раз, чтобы освободить блок формата.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Мтипе. h (включение Streams. h)</dt> </dl>                                                                                     |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Функции типа мультимедиа**](media-type-functions.md)
</dt> </dl>

 

