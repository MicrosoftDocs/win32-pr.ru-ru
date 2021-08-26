---
description: Метод DrawImage рисует кадр видео в окне видео.
ms.assetid: 22e7f59c-90f7-4e0c-8993-eea1eaf58fba
title: Метод Кдравимаже. DrawImage (Винутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.DrawImage
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c2791d20b906f2a2adce31ce99b9e7498854c8fca00ade4507db0207e04b2cde
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120043611"
---
# <a name="cdrawimagedrawimage-method"></a>Кдравимаже. DrawImage, метод

`DrawImage`Метод рисует кадр видео в окне видео.

## <a name="syntax"></a>Синтаксис


```C++
BOOL DrawImage(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пмедиасампле* 
</dt> <dd>

Указатель на интерфейс [**имедиасампле**](/windows/desktop/api/Strmif/nn-strmif-imediasample) образца, который содержит изображение.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение true** в случае успеха или **false** в противном случае.

## <a name="remarks"></a>Remarks

Этот метод делегирует [**кдравимаже:: фастрендер**](cdrawimage-fastrender.md) или [**Кдравимаже:: словрендер**](cdrawimage-slowrender.md)в зависимости от того, владеет ли фильтр распределителем, который предоставил пример. Если фильтр владеет распределителем, пример гарантированно будет объектом [**Цимажесампле**](cimagesample.md) . В этом случае в примере используется общая память, выделенная GDI, а изображение можно изобразить с помощью **BitBlt** или **стретчблт**. В противном случае изображения должны быть выведены с помощью медленных функций **сетдибитстодевице** или **стретчдибитс** .

В отладочных сборках этот метод вызывает **дисплайсамплетимес** , чтобы нарисовать отметки времени образца на изображении видео.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>винутил. h (включает Потоки. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кдравимаже**](cdrawimage.md)
</dt> <dt>

[**Кдравимаже:: Усингимажеаллокатор**](cdrawimage-usingimageallocator.md)
</dt> </dl>

 

 




