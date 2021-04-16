---
description: Метод Ресетпалеттеверсион сбрасывает версию палитры. Вызывайте этот метод, если ПИН-код фильтра владельца повторно подключится.
ms.assetid: c9e5588c-5501-4356-bdec-a339d33f9eb5
title: Кдравимаже. Ресетпалеттеверсион, метод (Винутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.ResetPaletteVersion
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a94cd04de428a29308ead8fa33ccfe1792e021a0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657145"
---
# <a name="cdrawimageresetpaletteversion-method"></a>Кдравимаже. Ресетпалеттеверсион, метод

`ResetPaletteVersion`Метод сбрасывает версию палитры. Вызывайте этот метод, если ПИН-код фильтра владельца повторно подключится.

## <a name="syntax"></a>Синтаксис


```C++
void ResetPaletteVersion();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Комментарии

Этот метод устанавливает значение **m \_ палеттеверсион** в стандартную константу, **\_ версию палитры**.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Винутил. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кдравимаже**](cdrawimage.md)
</dt> <dt>

[**Кдравимаже:: Жетпалеттеверсион**](cdrawimage-getpaletteversion.md)
</dt> <dt>

[**Кдравимаже:: Инкрементпалеттеверсион**](cdrawimage-incrementpaletteversion.md)
</dt> </dl>

 

 




