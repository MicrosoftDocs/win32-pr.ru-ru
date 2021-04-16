---
description: Создает копию изображения в памяти.
ms.assetid: 83a980bc-1298-439f-8dfc-49534591977f
title: Кбасеконтролвидео. Копимаже, метод (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.CopyImage
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 23ada87e77d3c3441f489abed2e7af86a2a556ad
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657250"
---
# <a name="cbasecontrolvideocopyimage-method"></a>Кбасеконтролвидео. Копимаже, метод

Создает копию изображения в памяти.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT CopyImage(
   IMediaSample    *pMediaSample,
   VIDEOINFOHEADER *pVideoInfo,
   LONG            *pBufferSize,
   BYTE            *pVideoImage,
   RECT            *pSourceRect
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пмедиасампле* 
</dt> <dd>

Указатель на образец, содержащий изображение видео.

</dd> <dt>

*пвидеоинфо* 
</dt> <dd>

Указатель на формат, представляющий изображение видео.

</dd> <dt>

*пбуфферсизе* 
</dt> <dd>

Указатель на размер выходного буфера.

</dd> <dt>

*пвидеоимаже* 
</dt> <dd>

Указатель на выходной буфер.

</dd> <dt>

*псаурцерект* 
</dt> <dd>

Указатель на исходный прямоугольник видео.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если параметр *пвидеоимаже* имеет **значение NULL**, параметр *пбуфферсизе* заполняется числом байтов, необходимых выходному буферу для хранения изображения. Если переданный буфер слишком мал или функция-член не может выделить достаточно памяти, функция-член возвращает E \_ OUTOFMEMORY.

## <a name="remarks"></a>Комментарии

Функция члена получает изображение из примера и копирует его в выходной буфер. Раздел видео, скопированный в выходной буфер, отражает исходный прямоугольник, заданный через интерфейс [**ибасиквидео**](/windows/desktop/api/Control/nn-control-ibasicvideo) (хотя он не отражает конечный прямоугольник).

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ктлутил. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасеконтролвидео**](cbasecontrolvideo.md)
</dt> </dl>

 

 




