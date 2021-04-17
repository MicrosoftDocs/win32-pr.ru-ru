---
title: BUTTONGROUP. Довнимаже
description: Атрибут Довнимаже указывает или получает имя изображения, представляющего состояние down BUTTONGROUP.
ms.assetid: 022e77e7-d3c0-41b5-984a-84d016a5a25a
keywords:
- Проигрыватель Windows Media BUTTONGROUP. Довнимаже
topic_type:
- apiref
api_name:
- BUTTONGROUP.downImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82b8a1d5bc2f4c68894a3bba1ad8ce9f2b3aa28a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694957"
---
# <a name="buttongroupdownimage"></a>BUTTONGROUP. Довнимаже

Атрибут **довнимаже** указывает или получает имя изображения, представляющего состояние down **BUTTONGROUP**.

``` syntax
        elementID.downImage
```

## <a name="possible-values"></a>Возможные значения

Этот атрибут является **строкой** для чтения и записи.

## <a name="remarks"></a>Комментарии

Поддерживаются форматы изображений BMP, JPG, PNG и GIF. Если изображение является 8-битным файлом BMP, его значения тона и насыщенности можно динамически изменить с помощью атрибутов **хуешифт** и **насыщенности** .

Изображение по умолчанию — это образ, указанный в атрибуте **Image** .

Если изображение вниз больше, чем определенная область, то изображение будет обрезано.

Если изображение не может быть получено, отображается изображение по умолчанию (изображение Красного x).

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------|
| Версия<br/> | Проигрыватель Windows Media версии 7,0 или более поздней<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**BUTTONGROUP, элемент**](buttongroup-element.md)
</dt> <dt>

[**BUTTONGROUP. Хуешифт**](buttongroup-hueshift.md)
</dt> <dt>

[**BUTTONGROUP. Image**](buttongroup-image.md)
</dt> <dt>

[**BUTTONGROUP. насыщенность**](buttongroup-saturation.md)
</dt> </dl>

 

 





