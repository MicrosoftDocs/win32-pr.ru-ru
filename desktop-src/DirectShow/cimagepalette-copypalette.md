---
description: Метод Копипалетте копирует палитру из любой структуры ВИДЕОИНФО в любую палеттизед ВИДЕОИНФО структуру.
ms.assetid: ea06b40b-3f96-4c11-921c-52f3a44e0a30
title: Цимажепалетте. Копипалетте, метод (Винутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImagePalette.CopyPalette
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b429c5fd4d3d0e0e28cd0662fbee0a1ac926ddc5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669213"
---
# <a name="cimagepalettecopypalette-method"></a>Цимажепалетте. Копипалетте, метод

`CopyPalette`Метод копирует палитру из любой структуры [**видеоинфо**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) в любую структуру палеттизед **видеоинфо** .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT CopyPalette(
   const CMediaType *pSrc,
   const CMediaType *pDest
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*pSrc* 
</dt> <dd>

Указатель на исходный тип носителя.

</dd> <dt>

*pDest* 
</dt> <dd>

Указатель на тип носителя назначения.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение \_ ОК, если палитра скопирована. Возвращает \_ значение false, если исходный или конечный тип носителя не имеет палитры.

## <a name="remarks"></a>Комментарии

Тип носителя *пдест* должен быть форматом палеттизед с глубиной цвета 8 бит или меньше. Тип носителя *pSrc* может быть любым типом [**видеоинфохеадер**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) с палитрой, включая форматы YUV и True-Color с записями палитры. Метод копирует записи палитры из *pSrc* в новую палитру и прикрепляет новую палитру к *пдест*.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Винутил. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Цимажепалетте**](cimagepalette.md)
</dt> </dl>

 

 




