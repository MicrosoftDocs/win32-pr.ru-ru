---
title: КНОПКА. Довнимаже
description: Атрибут Довнимаже указывает или получает изображение, представляющее состояние кнопки "вниз".
ms.assetid: 18149668-5be6-4b64-8adf-8904585ff0be
keywords:
- КНОПКА. Довнимаже Windows Media Player
topic_type:
- apiref
api_name:
- BUTTON.downImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca7a405a5df20a04ae9d093f2b28ee4c68cab67d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694520"
---
# <a name="buttondownimage"></a>КНОПКА. Довнимаже

Атрибут **довнимаже** указывает или получает изображение, представляющее состояние **кнопки "вниз"**.

``` syntax
        elementID.downImage
```

## <a name="possible-values"></a>Возможные значения

Этот атрибут является **строкой** для чтения и записи, содержащей имя файла изображения.

## <a name="remarks"></a>Комментарии

Поддерживаются форматы изображений BMP, JPG, PNG и GIF.

Изображение по умолчанию — это образ, указанный в атрибуте **Image** , или его значение по умолчанию.

Если изображение вниз больше, чем заданная область во внешнем атрибуте, то изображение будет обрезано.

Если изображение не может быть получено, отображается изображение по умолчанию (изображение Красного x).

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------|
| Версия<br/> | Проигрыватель Windows Media версии 7,0 или более поздней<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**BUTTON, элемент**](button-element.md)
</dt> <dt>

[**КНОПКА. вниз**](button-down.md)
</dt> <dt>

[**BUTTON. Image**](button-image.md)
</dt> </dl>

 

 





