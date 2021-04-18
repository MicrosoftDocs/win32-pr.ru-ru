---
title: EDITBOX. Фонтфаце
description: Атрибут Фонтфаце указывает или получает шрифт для текста в элементе управления "поле ввода".
ms.assetid: 5fb5e6d2-8535-402e-9ca1-d43e334e94e3
keywords:
- Фонтфаце Windows Media Player
topic_type:
- apiref
api_name:
- EDITBOX.fontFace
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49c5794da93821db840a48facbba45540da9249a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698971"
---
# <a name="editboxfontface"></a>EDITBOX. Фонтфаце

Атрибут **фонтфаце** указывает или получает шрифт для текста в элементе управления "поле ввода".

``` syntax
        elementID.fontFace
```

## <a name="possible-values"></a>Возможные значения

Этот атрибут является **строкой** для чтения и записи.

## <a name="remarks"></a>Комментарии

Этот атрибут может быть именем любого допустимого шрифта, доступного в Windows. Проигрыватель Windows Media не поддерживает установку шрифтов, поэтому выберите шрифт, который вы будете использовать в предполагаемой системе.

Если указанный **фонтфаце** недоступен в системе пользователя, элемент управления "поле ввода" по умолчанию имеет значение системный шрифт Windows. По умолчанию для английских языковых систем используется значение Tahoma. Для международных систем значение по умолчанию загружается из файла ресурсов.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------------|
| Версия<br/> | Проигрыватель Windows Media для Windows XP или более поздней версии<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**EDITBOX, элемент**](editbox-element.md)
</dt> <dt>

[**EDITBOX. fontSize**](editbox-fontsize.md)
</dt> <dt>

[**EDITBOX. fontStyle**](editbox-fontstyle.md)
</dt> </dl>

 

 





