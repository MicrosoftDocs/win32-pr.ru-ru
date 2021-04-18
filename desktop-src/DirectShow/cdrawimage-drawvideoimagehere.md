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
ms.openlocfilehash: 599dd82e282f2d14ac7e974363a62695e209c080
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657179"
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

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Винутил. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кдравимаже**](cdrawimage.md)
</dt> </dl>

 

 




