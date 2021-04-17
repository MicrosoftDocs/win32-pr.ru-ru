---
description: Метод Жетпалеттеверсион извлекает текущую версию палитры.
ms.assetid: 9f97a810-04a4-4ea3-8918-416e9cd8e5e4
title: Кдравимаже. Жетпалеттеверсион, метод (Винутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.GetPaletteVersion
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c86f1a0dad8d33913a52962dfe2ec09b7b8244db
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679864"
---
# <a name="cdrawimagegetpaletteversion-method"></a>Кдравимаже. Жетпалеттеверсион, метод

`GetPaletteVersion`Метод получает текущую версию палитры.

## <a name="syntax"></a>Синтаксис


```C++
LONG GetPaletteVersion();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение переменной члена **m \_ палеттеверсион** .

## <a name="remarks"></a>Комментарии

Значение, возвращаемое этим методом, применяется только в том случае, если распределитель является объектом [**Цимажеаллокатор**](cimageallocator.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Винутил. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кдравимаже**](cdrawimage.md)
</dt> <dt>

[**Кдравимаже:: Инкрементпалеттеверсион**](cdrawimage-incrementpaletteversion.md)
</dt> <dt>

[**Кдравимаже:: Ресетпалеттеверсион**](cdrawimage-resetpaletteversion.md)
</dt> </dl>

 

 




