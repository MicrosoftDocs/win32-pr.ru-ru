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
ms.openlocfilehash: 2eb9dc01a398a498252cca2f1f3af012608f8e0ca80c62800c56e4026c0b0a7d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119908824"
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

## <a name="remarks"></a>Remarks

Если параметр *бсетформат* имеет **значение true**, метод выделяет память для блока Format. Если параметр *ПЛТ* уже содержит выделенный блок формата, произойдет утечка памяти. Чтобы избежать утечки памяти, вызовите [**фримедиатипе**](freemediatype.md) перед вызовом этой функции. После возврата метода вызовите **фримедиатипе** еще раз, чтобы освободить блок формата.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>мтипе. h (включает Потоки. h)</dt> </dl>                                                                                     |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Функции типа мультимедиа**](media-type-functions.md)
</dt> </dl>

 

