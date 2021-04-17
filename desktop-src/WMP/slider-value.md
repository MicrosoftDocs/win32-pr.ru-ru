---
title: ПОЛЗУНок. Value
description: Атрибут value указывает или получает текущую точку ползунка. | ПОЛЗУНок. Value
ms.assetid: 2cd2f8b2-d3f1-4897-98b0-af551d6693e6
keywords:
- Windows Media Player с ПОЛЗУНКом. Value
topic_type:
- apiref
api_name:
- SLIDER.value
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e87aeff5c97808efb812f530236227b07f463855
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657269"
---
# <a name="slidervalue"></a>ПОЛЗУНок. Value

Атрибут **value** указывает или получает текущую точку ползунка.

``` syntax
        elementID.value
```

## <a name="possible-values"></a>Возможные значения

Этот атрибут является **числом** для чтения и записи (**float**) и значением по умолчанию **min**.

## <a name="remarks"></a>Комментарии

**Значение** всегда должно быть больше или равно **min** и меньше или равно **Max**. Если указать значение вне этого диапазона, **значение** и положение ползунка не изменяются.

См. **кустомслидер**. атрибут [поситионимаже](customslider-positionimage.md) для примера, иллюстрирующий использование атрибутов элемента **Slider** .

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------|
| Версия<br/> | Проигрыватель Windows Media версии 7,0 или более поздней<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Элемент SLIDER**](slider-element.md)
</dt> <dt>

[**SLIDER. min**](slider-min.md)
</dt> </dl>

 

 





