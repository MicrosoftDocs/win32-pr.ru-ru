---
description: Метод конструктора.
ms.assetid: 50fa573c-a244-4a1e-9fd9-2b33a3427c84
title: Конструктор Цимажепалетте. Цимажепалетте (Винутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImagePalette.CImagePalette
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 38b5766617e1d17fa3917048c2fb845b5194cc42
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679823"
---
# <a name="cimagepalettecimagepalette-constructor"></a>Цимажепалетте. Цимажепалетте, конструктор

Метод конструктора.

## <a name="syntax"></a>Синтаксис


```C++
CImagePalette(
   CBaseFilter *pBaseFilter,
   CBaseWindow *pBaseWindow,
   CDrawImage  *pDrawImage
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пбасефилтер* 
</dt> <dd>

Указатель на фильтр-владелец.

</dd> <dt>

*пбасевиндов* 
</dt> <dd>

Указатель на объект **кбасевиндов** , который управляет окном, в котором реализована палитра. Этот параметр может принимать значение **NULL**.

</dd> <dt>

*пдравимаже* 
</dt> <dd>

Указатель на объект **кдравимаже** , который рисует изображение видео. Этот параметр может принимать значение **NULL**.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Винутил. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Цимажепалетте**](cimagepalette.md)
</dt> </dl>

 

 




