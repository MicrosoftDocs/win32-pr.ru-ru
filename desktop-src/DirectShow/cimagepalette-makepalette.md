---
description: Метод Макепалетте создает логическую палитру из таблицы цветов в видеоформате.
ms.assetid: f158e529-d683-4210-818d-21a834fc7683
title: Цимажепалетте. Макепалетте, метод (Винутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImagePalette.MakePalette
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 20c4484b2666b25b5d713ede450a9a5a99f93348
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105674943"
---
# <a name="cimagepalettemakepalette-method"></a>Цимажепалетте. Макепалетте, метод

`MakePalette`Метод создает логическую палитру из таблицы цветов в видеоформате.

## <a name="syntax"></a>Синтаксис


```C++
HPALETTE MakePalette(
   const VIDEOINFOHEADER *pVideoInfo,
         LPSTR           szDevice
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пвидеоинфо* 
</dt> <dd>

Указатель на структуру [**видеоинфохеадер**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) , содержащую таблицу цветов.

</dd> <dt>

*сздевице* 
</dt> <dd>

Указатель на строку, содержащую имя устройства вывода, которое возвращается функцией GDI **енумдисплайдевицес** . Чтобы использовать основное устройство вывода, присвойте этому параметру **значение NULL**.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

В случае успеха возвращает маркер для палитры. В противном случае возвращает **значение NULL**.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Винутил. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Цимажепалетте**](cimagepalette.md)
</dt> </dl>

 

 




