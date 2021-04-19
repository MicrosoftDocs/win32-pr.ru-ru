---
title: TEXT. toolTip
description: Атрибут toolTip указывает или получает текст подсказки для элемента управления Text.
ms.assetid: 3e275607-e7ff-4424-8310-c628ede22629
keywords:
- TEXT. toolTip проигрыватель Windows Media Player
topic_type:
- apiref
api_name:
- TEXT.toolTip
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b064f2abefd07ec65a82069196b1012561699b62
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675411"
---
# <a name="texttooltip"></a>TEXT. toolTip

Атрибут **ToolTip** указывает или получает текст подсказки для элемента управления Text.

``` syntax
        elementID.toolTip
```

## <a name="possible-values"></a>Возможные значения

Этот атрибут является **строкой** для чтения и записи и имеет максимальную длину 1024 символов. У него нет значения по умолчанию.

## <a name="remarks"></a>Комментарии

Если этот атрибут не указан и текст в атрибуте **value** усекается в элементе управления Text, или для свойства **WordWrap** задано значение true, подсказка будет отображать полный текст атрибута **value** .

Если для этого атрибута задано значение "" (пустая строка), подсказка не отображается.

См. атрибут [value](text-value.md) для примера, иллюстрирующий использование атрибутов **текстового** элемента.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------|
| Версия<br/> | Проигрыватель Windows Media версии 7,0 или более поздней<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**TEXT, элемент**](text-element.md)
</dt> <dt>

[**TEXT. Value**](text-value.md)
</dt> <dt>

[**TEXT. wordWrap**](text-wordwrap.md)
</dt> </dl>

 

 





