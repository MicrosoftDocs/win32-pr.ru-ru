---
title: LISTBOX. fontStyle
description: Атрибут fontStyle указывает или получает стиль шрифта для элемента управления "список".
ms.assetid: c42b80b6-0dea-4080-a06e-931fdc02fa55
keywords:
- Проигрыватель Windows Media LISTBOX. fontStyle
topic_type:
- apiref
api_name:
- LISTBOX.fontStyle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0903ac77f1fa4307dfcabad6311eb556617d8153
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694971"
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
| Жирный      | Начертание шрифта полужирным шрифтом.      |
| Курсив    | Стиль шрифта курсивом.    |
| Underline | Подчеркнуть стиль шрифта. |
| Перечеркивание | Зачеркивание стиля шрифта. |
| Норм.    | Обычный стиль шрифта.    |



 

## <a name="remarks"></a>Комментарии

Можно использовать любое сочетание значений, разделенных пробелами. Стиль "Стандартный" имеет приоритет над всеми другими значениями, и все остальные, указанные вместе с параметром "нормально", будут игнорироваться.

Для целей отрисовки используется обычный стиль шрифта по умолчанию. Значение по умолчанию, полученное из этого атрибута, — "" (пустая строка).

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------------|
| Версия<br/> | Проигрыватель Windows Media для Windows XP или более поздней версии<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Элемент LISTBOX**](listbox-element.md)
</dt> <dt>

[**Список LISTBOX. fontSize**](listbox-fontsize.md)
</dt> </dl>

 

 





