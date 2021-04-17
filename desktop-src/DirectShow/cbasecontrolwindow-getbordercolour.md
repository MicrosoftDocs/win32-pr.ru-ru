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
ms.openlocfilehash: 0ba6e1be9babf96d03235c49d9cde0f11cae1b83
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657461"
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

## <a name="remarks"></a>Комментарии

Приложение может задать конечный прямоугольник для вывода видео. Этот прямоугольник должен относиться к клиентской области окна. Если это сделано (по умолчанию всегда закрашивать все окно), то есть область, окружающая видео; то есть граница. Цвет границы можно задать с помощью функции-члена [**кбасеконтролвиндов::p UT \_ BorderColor**](cbasecontrolwindow-put-bordercolor.md) . Это свойство влияет на цвет границы. Используйте эту функцию-член вместо [**кбасеконтролвиндов:: Get \_ BorderColor**](cbasecontrolwindow-get-bordercolor.md), если только вы не вызываете это внешне через метод [**ивидеовиндов:: Get \_ BorderColor**](/windows/desktop/api/Control/nf-control-ivideowindow-get_bordercolor) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ктлутил. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасеконтролвиндов**](cbasecontrolwindow.md)
</dt> </dl>

 

 




