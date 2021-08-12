---
title: ПОЛЗУНок. foregroundColor
description: Атрибут foregroundColor указывает или получает цвет переднего плана для элемента управления "ползунок".
ms.assetid: 8c8de4a9-0021-41ed-aeb8-75653855b6f1
keywords:
- проигрыватель Windows Media SLIDER. foregroundColor
topic_type:
- apiref
api_name:
- SLIDER.foregroundColor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a111dca131351dedaf2080d16bffa4db1344e9993cabcfe8ca44f149fd97eb3c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118569096"
---
# <a name="sliderforegroundcolor"></a>ПОЛЗУНок. foregroundColor

Атрибут **foregroundColor** указывает или получает цвет переднего плана для элемента управления "ползунок".

``` syntax
        elementID.foregroundColor
```

## <a name="possible-values"></a>Возможные значения

Этот атрибут является **строкой** для чтения и записи, содержащей любое значение цвета Microsoft Internet Explorer. Значение по умолчанию — "белый".

## <a name="remarks"></a>Remarks

Базовый элемент управления "ползунок" может быть создан путем указания одной из двух пар атрибутов: **backgroundColor** и **foregroundColor**, **backgroundImage** и **фореграундимаже**.

При создании элемента управления "ползунок" с помощью атрибутов цвета размеры элемента управления "ползунок" определяют область, заполненную цветом фона. Цвет переднего плана охватывает цвет фона по мере увеличения положения ползунка.

Чтобы сделать градиентную заливку в области, занимаемой цветом фона или переднего плана, укажите атрибуты **баккграундендколор** или **фореграундендколор** .

См. *кустомслидер*. атрибут [поситионимаже](customslider-positionimage.md) для примера, иллюстрирующий использование атрибутов элемента **Slider** .

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------|
| Версия<br/> | проигрыватель Windows Media версии 7,0 или более поздней<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Ссылка на цвет**](color-reference.md)
</dt> <dt>

[**Элемент SLIDER**](slider-element.md)
</dt> <dt>

[**ПОЛЗУНок. backgroundColor**](slider-backgroundcolor.md)
</dt> <dt>

[**ПОЛЗУНок. Баккграундендколор**](slider-backgroundendcolor.md)
</dt> <dt>

[**ПОЛЗУНок. Фореграундендколор**](slider-foregroundendcolor.md)
</dt> <dt>

[**ПОЛЗУНок. Фореграундимаже**](slider-foregroundimage.md)
</dt> </dl>

 

 





