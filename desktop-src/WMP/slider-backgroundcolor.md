---
title: ПОЛЗУНок. backgroundColor
description: Атрибут backgroundColor указывает или получает цвет фона элемента управления "ползунок".
ms.assetid: 8f2c48ec-29f5-4fbe-aa62-c7cfb8a8678c
keywords:
- проигрыватель Windows Media SLIDER. backgroundColor
topic_type:
- apiref
api_name:
- SLIDER.backgroundColor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4fc2de30392c58cfad151e2d3c209f0407880a47522a536bf08dbe42d7f56dc0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118995234"
---
# <a name="sliderbackgroundcolor"></a>ПОЛЗУНок. backgroundColor

Атрибут **backgroundColor** указывает или получает цвет фона элемента управления "ползунок".

``` syntax
        elementID.backgroundColor
```

## <a name="possible-values"></a>Возможные значения

Этот атрибут является **строкой** для чтения и записи, содержащей любое значение цвета Microsoft Internet Explorer. У него нет значения по умолчанию.

## <a name="remarks"></a>Remarks

Базовый элемент управления "ползунок" может быть создан путем указания **backgroundColor** или **backgroundImage**, а также **foregroundColor** или **фореграундимаже**.

При использовании цветов размеры элемента управления Slider определяют область, заполненную цветом фона. Цвет переднего плана охватывает цвет фона по мере увеличения положения ползунка.

Чтобы сделать градиентную заливку области, занятой цветом фона или переднего плана, укажите атрибуты **баккграундендколор** или **фореграундендколор** .

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

[**ПОЛЗУНок. Баккграундендколор**](slider-backgroundendcolor.md)
</dt> <dt>

[**ПОЛЗУНок. backgroundImage**](slider-backgroundimage.md)
</dt> <dt>

[**ПОЛЗУНок. foregroundColor**](slider-foregroundcolor.md)
</dt> <dt>

[**ПОЛЗУНок. Фореграундендколор**](slider-foregroundendcolor.md)
</dt> <dt>

[**ПОЛЗУНок. Фореграундимаже**](slider-foregroundimage.md)
</dt> </dl>

 

 





