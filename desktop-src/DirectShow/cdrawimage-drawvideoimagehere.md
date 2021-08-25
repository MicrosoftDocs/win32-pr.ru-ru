---
description: Метод Драввидеоимажехере рисует изображение из примера носителя в заданном контексте устройства.
ms.assetid: b11e1c6b-5a29-444f-a0a9-049cd9d49b13
title: Кдравимаже. Драввидеоимажехере, метод (Винутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.DrawVideoImageHere
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8137c4e18708ce6a0402d1d34caf9560054f267d8de0280a6efb5c3dd36e6517
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119909814"
---
# <a name="cdrawimagedrawvideoimagehere-method"></a>Кдравимаже. Драввидеоимажехере, метод

`DrawVideoImageHere`Метод выводит изображение из примера носителя в указанный контекст устройства.

## <a name="syntax"></a>Синтаксис


```C++
BOOL DrawVideoImageHere(
   HDC          hdc,
   IMediaSample *pMediaSample,
   RECT         *lprcSrc,
   RECT         *lprcDst
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*HDC* 
</dt> <dd>

Обработайте с контекстом устройства, где будет выполняться рисование.

</dd> <dt>

*пмедиасампле* 
</dt> <dd>

Указатель на интерфейс [**имедиасампле**](/windows/desktop/api/Strmif/nn-strmif-imediasample) образца, который содержит изображение.

</dd> <dt>

*лпрксрк* 
</dt> <dd>

Указатель на исходный прямоугольник, используемый для рисования. Если **значение равно NULL**, используется прямоугольник в [**кдравимаже:: m \_ саурцерект**](cdrawimage-m-sourcerect.md) .

</dd> <dt>

*лпркдст* 
</dt> <dd>

Указатель на целевой прямоугольник, используемый для рисования. Если **значение равно NULL**, используется прямоугольник в [**кдравимаже:: m \_ таржетрект**](cdrawimage-m-targetrect.md) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение true** в случае успеха.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>винутил. h (включает Потоки. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Кдравимаже**](cdrawimage.md)
</dt> </dl>

 

 




