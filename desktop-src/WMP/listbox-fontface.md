---
title: LISTBOX. Фонтфаце
description: Атрибут Фонтфаце указывает или получает шрифт для элемента управления "список".
ms.assetid: 15e3180a-6e1e-4654-a0bb-164d66a86a26
keywords:
- Проигрыватель Windows Media LISTBOX. Фонтфаце
topic_type:
- apiref
api_name:
- LISTBOX.fontFace
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82c03c367001b307dd8bd5059ec7e3f4a0b364e6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694973"
---
# <a name="listboxfontface"></a>LISTBOX. Фонтфаце

Атрибут **фонтфаце** указывает или получает шрифт для элемента управления "список".

``` syntax
        elementID.fontFace
```

## <a name="possible-values"></a>Возможные значения

Этот атрибут является **строкой** для чтения и записи.

## <a name="remarks"></a>Комментарии

Этот атрибут может быть именем любого допустимого шрифта, доступного в Windows. Проигрыватель Windows Media не поддерживает установку шрифтов, поэтому выберите шрифт, который вы будете использовать в предполагаемой системе.

Если указанный **фонтфаце** недоступен в системе пользователя, элемент управления "список" по умолчанию имеет значение системный шрифт Windows. По умолчанию для английских языковых систем используется значение Tahoma. Для международных систем значение по умолчанию загружается из файла ресурсов.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------------|
| Версия<br/> | Проигрыватель Windows Media для Windows XP или более поздней версии<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Элемент LISTBOX**](listbox-element.md)
</dt> <dt>

[**Список LISTBOX. fontSize**](listbox-fontsize.md)
</dt> <dt>

[**LISTBOX. fontStyle**](listbox-fontstyle.md)
</dt> </dl>

 

 





