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
ms.openlocfilehash: 14cc4df95507a0c28bd61ec6db405f01353f9228419d0da84c4fc9fc35ca6b55
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119537294"
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

## <a name="remarks"></a>Remarks

Значение, возвращаемое этим методом, применяется только в том случае, если распределитель является объектом [**Цимажеаллокатор**](cimageallocator.md) .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>винутил. h (включает Потоки. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Кдравимаже**](cdrawimage.md)
</dt> <dt>

[**Кдравимаже:: Инкрементпалеттеверсион**](cdrawimage-incrementpaletteversion.md)
</dt> <dt>

[**Кдравимаже:: Ресетпалеттеверсион**](cdrawimage-resetpaletteversion.md)
</dt> </dl>

 

 




