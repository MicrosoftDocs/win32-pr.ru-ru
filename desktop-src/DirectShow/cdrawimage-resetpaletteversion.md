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
ms.openlocfilehash: d367060c86c54fb9df5bd7b0f05cea1fa3d7b7f3316dce327fca7ce9985fadfb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120055964"
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

## <a name="remarks"></a>Remarks

Этот метод устанавливает значение **m \_ палеттеверсион** в стандартную константу, **\_ версию палитры**.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>винутил. h (включает Потоки. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Кдравимаже**](cdrawimage.md)
</dt> <dt>

[**Кдравимаже:: Жетпалеттеверсион**](cdrawimage-getpaletteversion.md)
</dt> <dt>

[**Кдравимаже:: Инкрементпалеттеверсион**](cdrawimage-incrementpaletteversion.md)
</dt> </dl>

 

 




