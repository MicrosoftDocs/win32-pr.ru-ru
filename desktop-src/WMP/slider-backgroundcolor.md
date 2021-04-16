---
title: ПОЛЗУНок. backgroundColor
description: Атрибут backgroundColor указывает или получает цвет фона элемента управления "ползунок".
ms.assetid: 8f2c48ec-29f5-4fbe-aa62-c7cfb8a8678c
keywords:
- ПОЛЗУНок. backgroundColor Windows Media Player
topic_type:
- apiref
api_name:
- SLIDER.backgroundColor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06cc595af13b28541fcc570e130da4e804fdeafe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105656942"
---
# <a name="sliderbackgroundcolor"></a>ПОЛЗУНок. backgroundColor

Атрибут **backgroundColor** указывает или получает цвет фона элемента управления "ползунок".

``` syntax
        elementID.backgroundColor
```

## <a name="possible-values"></a>Возможные значения

Этот атрибут является **строкой** для чтения и записи, содержащей любое значение цвета Microsoft Internet Explorer. У него нет значения по умолчанию.

## <a name="remarks"></a>Комментарии

Базовый элемент управления "ползунок" может быть создан путем указания **backgroundColor** или **backgroundImage**, а также **foregroundColor** или **фореграундимаже**.

При использовании цветов размеры элемента управления Slider определяют область, заполненную цветом фона. Цвет переднего плана охватывает цвет фона по мере увеличения положения ползунка.

Чтобы сделать градиентную заливку области, занятой цветом фона или переднего плана, укажите атрибуты **баккграундендколор** или **фореграундендколор** .

См. *кустомслидер*. атрибут [поситионимаже](customslider-positionimage.md) для примера, иллюстрирующий использование атрибутов элемента **Slider** .

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------|
| Версия<br/> | Проигрыватель Windows Media версии 7,0 или более поздней<br/> |



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

 

 





