---
title: EDITBOX. fontStyle
description: Атрибут fontStyle указывает или получает стиль шрифта для элемента управления "поле ввода".
ms.assetid: bc71359d-2b75-4134-99e8-52b2ca48dcde
keywords:
- FontStyle Windows Media Player
topic_type:
- apiref
api_name:
- EDITBOX.fontStyle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4249f6224099c3d2a36a3b26244c9b804be519c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694537"
---
# <a name="editboxfontstyle"></a>EDITBOX. fontStyle

Атрибут **FontStyle** указывает или получает стиль шрифта для элемента управления "поле ввода".

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

[**EDITBOX, элемент**](editbox-element.md)
</dt> <dt>

[**EDITBOX. Фонтфаце**](editbox-fontface.md)
</dt> <dt>

[**EDITBOX. fontSize**](editbox-fontsize.md)
</dt> </dl>

 

 





