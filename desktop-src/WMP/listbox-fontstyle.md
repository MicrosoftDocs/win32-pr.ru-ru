---
title: LISTBOX. fontStyle
description: Атрибут fontStyle указывает или получает стиль шрифта для элемента управления "список".
ms.assetid: c42b80b6-0dea-4080-a06e-931fdc02fa55
keywords:
- проигрыватель Windows Media LISTBOX. fontStyle
topic_type:
- apiref
api_name:
- LISTBOX.fontStyle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 258064ca4ee97fc33bb98bf64d8e3dcf305c5d7e045282a5218a060e904aff50
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118575041"
---
# <a name="listboxfontstyle"></a>LISTBOX. fontStyle

Атрибут **FontStyle** указывает или получает стиль шрифта для элемента управления "список".

``` syntax
        elementID.fontStyle
```

## <a name="possible-values"></a>Возможные значения

Этот атрибут является **строкой** для чтения и записи, содержащей одно или несколько из следующих значений.



| Значение     | Описание           |
|-----------|-----------------------|
| Полужирный      | Начертание шрифта полужирным шрифтом.      |
| Курсив    | Стиль шрифта курсивом.    |
| Underline | Подчеркнуть стиль шрифта. |
| Перечеркивание | Зачеркивание стиля шрифта. |
| Норм.    | Обычный стиль шрифта.    |



 

## <a name="remarks"></a>Remarks

Можно использовать любое сочетание значений, разделенных пробелами. Стиль "Стандартный" имеет приоритет над всеми другими значениями, и все остальные, указанные вместе с параметром "нормально", будут игнорироваться.

Для целей отрисовки используется обычный стиль шрифта по умолчанию. Значение по умолчанию, полученное из этого атрибута, — "" (пустая строка).

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------------|
| Версия<br/> | проигрыватель Windows Media для Windows XP или более поздней версии<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Элемент LISTBOX**](listbox-element.md)
</dt> <dt>

[**Список LISTBOX. fontSize**](listbox-fontsize.md)
</dt> </dl>

 

 





