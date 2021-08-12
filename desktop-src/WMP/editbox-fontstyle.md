---
title: EDITBOX. fontStyle
description: Атрибут fontStyle указывает или получает стиль шрифта для элемента управления "поле ввода".
ms.assetid: bc71359d-2b75-4134-99e8-52b2ca48dcde
keywords:
- EDITBOX. fontStyle проигрыватель Windows Media
topic_type:
- apiref
api_name:
- EDITBOX.fontStyle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 65d9dc5ac5fe3750fb3a6af8658a5ddb30274764cc891438162434a44651322a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118578850"
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

[**EDITBOX, элемент**](editbox-element.md)
</dt> <dt>

[**EDITBOX. Фонтфаце**](editbox-fontface.md)
</dt> <dt>

[**EDITBOX. fontSize**](editbox-fontsize.md)
</dt> </dl>

 

 





