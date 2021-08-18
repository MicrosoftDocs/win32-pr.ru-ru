---
title: BUTTONGROUP. Дисабледимаже
description: Атрибут Дисабледимаже указывает или получает имя изображения, представляющего отключенное состояние кнопок в BUTTONGROUP.
ms.assetid: 34d4e6a9-de73-4dfa-9c23-4f17b55298f6
keywords:
- BUTTONGROUP. дисабледимаже проигрыватель Windows Media
topic_type:
- apiref
api_name:
- BUTTONGROUP.disabledImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7eeef37bbc25185a64e767f00f9ce17934e8b445327606b552ad69d282e42e4b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119764354"
---
# <a name="buttongroupdisabledimage"></a>BUTTONGROUP. Дисабледимаже

Атрибут **дисабледимаже** указывает или получает имя изображения, представляющего отключенное состояние кнопок в **BUTTONGROUP**.

``` syntax
        elementID.disabledImage
```

## <a name="possible-values"></a>Возможные значения

Этот атрибут является **строкой** для чтения и записи.

## <a name="remarks"></a>Remarks

Поддерживаются форматы изображений BMP, JPG, PNG и GIF. Если изображение является 8-битным файлом BMP, его значения тона и насыщенности можно динамически изменить с помощью атрибутов **хуешифт** и **насыщенности** .

Если атрибуту **disabled** элемента **буттонелемент** присвоено значение true, то отображается соответствующий регион **дисабледимаже** для **BUTTONGROUP** . Если отключенный образ больше, чем заданный регион, отключенный образ будет обрезан.

Если изображение не может быть получено, отображается изображение по умолчанию (изображение Красного x).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|------------------------------------------------------|
| Версия<br/> | проигрыватель Windows Media версии 7,0 или более поздней<br/> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**BUTTONGROUP, элемент**](buttongroup-element.md)
</dt> <dt>

[**BUTTONGROUP. Хуешифт**](buttongroup-hueshift.md)
</dt> <dt>

[**BUTTONGROUP. насыщенность**](buttongroup-saturation.md)
</dt> </dl>

 

 





