---
title: Список воспроизведения. Хуешифт
description: Атрибут Хуешифт указывает или получает величину, на которую смещается оттенок раскрывающихся изображений.
ms.assetid: 9d4d8b73-527e-43f3-a921-0576b8897918
keywords:
- проигрыватель Windows Media списка воспроизведения. хуешифт
topic_type:
- apiref
api_name:
- PLAYLIST.hueShift
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a615549c25b57ed9693843a09433200f73c8e4ffad131c2a4e4057932c5e92b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117747082"
---
# <a name="playlisthueshift"></a>Список воспроизведения. Хуешифт

Атрибут **хуешифт** указывает или получает величину, на которую смещается оттенок раскрывающихся изображений.

``` syntax
        elementID.hueShift
```

## <a name="possible-values"></a>Возможные значения

Этот атрибут является **числом** для чтения и записи (**float**) со значением в диапазоне от 0,0 до 360,0 со значением по умолчанию 0,0.

## <a name="remarks"></a>Remarks

Этот атрибут изменяет значение оттенка изображений, заданных атрибутами **дропдовнбаккграундимаже** и **дропдовнимаже** , если они заданы и ссылаются на 8-битные изображения BMP.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------|
| Версия<br/> | проигрыватель Windows Media 9 Series или более поздней версии<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Элемент списка воспроизведения**](playlist-element.md)
</dt> <dt>

[**Список воспроизведения. Дропдовнбаккграундимаже**](playlist-dropdownbackgroundimage.md)
</dt> <dt>

[**Список воспроизведения. Дропдовнимаже**](playlist-dropdownimage.md)
</dt> <dt>

[**Список воспроизведения. насыщенность**](playlist-saturation.md)
</dt> </dl>

 

 





