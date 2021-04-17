---
title: TEXT. backgroundColor
description: Атрибут backgroundColor указывает или получает цвет фона для элемента управления "текст".
ms.assetid: 0c16318f-bf57-4c5f-85c1-46641124d431
keywords:
- Проигрыватель Windows Media TEXT. backgroundColor
topic_type:
- apiref
api_name:
- TEXT.backgroundColor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bff833fad0b5ad60b49479c57dc51cbe82f48dbd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105717826"
---
# <a name="textbackgroundcolor"></a>TEXT. backgroundColor

Атрибут **backgroundColor** указывает или получает цвет фона для элемента управления "текст".

``` syntax
        elementID.backgroundColor
```

## <a name="possible-values"></a>Возможные значения

Этот атрибут является **строкой** для чтения и записи, содержащей любое значение цвета Microsoft Internet Explorer, или значение None. Он имеет значение по умолчанию «нет», что означает, что фон прозрачен.

## <a name="remarks"></a>Комментарии

Цвет фона задается для высоты и ширины элемента управления. Если высота и ширина не заданы, то цвет фона устанавливается равным высоте и ширине текста.

При использовании **алфабленд** или **алфаблендто** с **текстовым** элементом, в котором не указан **backgroundColor** , будет использоваться цвет фона черного цвета. Если цвет переднего плана также является черным (значением по умолчанию для атрибута **foregroundColor** ), текст может стать нечитаемым. Чтобы избежать этого, всегда указывайте атрибут **backgroundColor** или задайте для **foregroundColor** цвет, отличный от черного.

См. атрибут [value](text-value.md) для примера, иллюстрирующий использование атрибутов **текстового** элемента.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------|
| Версия<br/> | Проигрыватель Windows Media версии 7,0 или более поздней<br/> |



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

[**TEXT. foregroundColor**](text-foregroundcolor.md)
</dt> </dl>

 

 





