---
description: Метод Жетбордерколаур извлекает текущий цвет границы окна, m \_ бордерколаур.
ms.assetid: 5cd9b834-5438-475e-9671-ee9917f9a485
title: Кбасеконтролвиндов. Жетбордерколаур, метод (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.GetBorderColour
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9b5b94e0fa58c95e74fd140c04710e8aaacef9402397fa475983c0e01e586528
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119017372"
---
# <a name="cbasecontrolwindowgetbordercolour-method"></a>Кбасеконтролвиндов. Жетбордерколаур, метод

`GetBorderColour`Метод получает текущий цвет границы окна, **m \_ бордерколаур**.

## <a name="syntax"></a>Синтаксис


```C++
COLORREF GetBorderColour();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Возвращает цвет границы.

## <a name="remarks"></a>Remarks

Приложение может задать конечный прямоугольник для вывода видео. Этот прямоугольник должен относиться к клиентской области окна. Если это сделано (по умолчанию всегда закрашивать все окно), то есть область, окружающая видео; то есть граница. Цвет границы можно задать с помощью функции-члена [**кбасеконтролвиндов::p UT \_ BorderColor**](cbasecontrolwindow-put-bordercolor.md) . Это свойство влияет на цвет границы. Используйте эту функцию-член вместо [**кбасеконтролвиндов:: Get \_ BorderColor**](cbasecontrolwindow-get-bordercolor.md), если только вы не вызываете это внешне через метод [**ивидеовиндов:: Get \_ BorderColor**](/windows/desktop/api/Control/nf-control-ivideowindow-get_bordercolor) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>ктлутил. h (включает Потоки. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасеконтролвиндов**](cbasecontrolwindow.md)
</dt> </dl>

 

 




