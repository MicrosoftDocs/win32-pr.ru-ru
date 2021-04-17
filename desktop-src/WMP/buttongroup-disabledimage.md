---
title: BUTTONGROUP. Дисабледимаже
description: Атрибут Дисабледимаже указывает или получает имя изображения, представляющего отключенное состояние кнопок в BUTTONGROUP.
ms.assetid: 34d4e6a9-de73-4dfa-9c23-4f17b55298f6
keywords:
- Проигрыватель Windows Media BUTTONGROUP. Дисабледимаже
topic_type:
- apiref
api_name:
- BUTTONGROUP.disabledImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9659c4d726313c0fb202a840e12891f00ad3fcf0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694589"
---
# <a name="buttongroupdisabledimage"></a>BUTTONGROUP. Дисабледимаже

Атрибут **дисабледимаже** указывает или получает имя изображения, представляющего отключенное состояние кнопок в **BUTTONGROUP**.

``` syntax
        elementID.disabledImage
```

## <a name="possible-values"></a>Возможные значения

Этот атрибут является **строкой** для чтения и записи.

## <a name="remarks"></a>Комментарии

Поддерживаются форматы изображений BMP, JPG, PNG и GIF. Если изображение является 8-битным файлом BMP, его значения тона и насыщенности можно динамически изменить с помощью атрибутов **хуешифт** и **насыщенности** .

Если атрибуту **disabled** элемента **буттонелемент** присвоено значение true, то отображается соответствующий регион **дисабледимаже** для **BUTTONGROUP** . Если отключенный образ больше, чем заданный регион, отключенный образ будет обрезан.

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

[**BUTTONGROUP. насыщенность**](buttongroup-saturation.md)
</dt> </dl>

 

 





