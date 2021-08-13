---
title: TEXT. foregroundColor
description: Атрибут foregroundColor указывает или получает цвет текста для элемента управления "текст".
ms.assetid: 1ddbad93-fbff-4be6-9797-6594b5f09a1e
keywords:
- проигрыватель Windows Media TEXT. foregroundColor
topic_type:
- apiref
api_name:
- TEXT.foregroundColor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b134058fdc39b653982f752f2623c6cd69b192e24e417ac012a02813a38334a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119467074"
---
# <a name="textforegroundcolor"></a>TEXT. foregroundColor

Атрибут **foregroundColor** указывает или получает цвет текста для элемента управления "текст".

``` syntax
        elementID.foregroundColor
```

## <a name="possible-values"></a>Возможные значения

Этот атрибут является **строкой** для чтения и записи, содержащей любое значение цвета Microsoft Internet Explorer. Значение по умолчанию — "Black".

См. атрибут [value](text-value.md) для примера, иллюстрирующий использование атрибутов **текстового** элемента.

При использовании **алфабленд** или **алфаблендто** с **текстовым** элементом, в котором не указан **backgroundColor** , будет использоваться цвет фона черного цвета. Если цвет переднего плана также является черным (значением по умолчанию для атрибута **foregroundColor** ), текст может стать нечитаемым. Чтобы избежать этого, всегда указывайте атрибут **backgroundColor** или задайте для **foregroundColor** цвет, отличный от черного.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|------------------------------------------------------|
| Версия<br/> | проигрыватель Windows Media версии 7,0 или более поздней<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Амбиентаттрибутес. Алфабленд**](ambientattributes-alphablend.md)
</dt> <dt>

[**Амбиентаттрибутес. Алфаблендто**](ambientattributes-alphablendto.md)
</dt> <dt>

[**Ссылка на цвет**](color-reference.md)
</dt> <dt>

[**TEXT, элемент**](text-element.md)
</dt> <dt>

[**TEXT. backgroundColor**](text-backgroundcolor.md)
</dt> </dl>

 

 





