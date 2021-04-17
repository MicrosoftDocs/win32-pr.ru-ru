---
title: Список воспроизведения. насыщенность
description: Атрибут насыщенности указывает или получает значение насыщенности раскрывающихся изображений.
ms.assetid: 4c5dd3d9-828a-45c9-896a-9a702d354544
keywords:
- Проигрыватель Windows Media в списке воспроизведения. насыщенность
topic_type:
- apiref
api_name:
- PLAYLIST.saturation
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82eb53afeafb0754f0e754f68fd5ff785eaade8a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704255"
---
# <a name="playlistsaturation"></a>Список воспроизведения. насыщенность

Атрибут **насыщенности** указывает или получает значение насыщенности раскрывающихся изображений.

``` syntax
        elementID.saturation
```

## <a name="possible-values"></a>Возможные значения

Этот атрибут является **числом** для чтения и записи (**float**) со значением в диапазоне от 0,0 до 2,0 со значением по умолчанию 1,0.

## <a name="remarks"></a>Комментарии

Этот атрибут изменяет значение насыщенности изображений, заданных атрибутами **дропдовнбаккграундимаже** и **дропдовнимаже** , если они заданы и ссылаются на 8-битные изображения BMP.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------|
| Версия<br/> | Проигрыватель Windows Media 9 Series или более поздней версии<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Элемент списка воспроизведения**](playlist-element.md)
</dt> <dt>

[**Список воспроизведения. Дропдовнбаккграундимаже**](playlist-dropdownbackgroundimage.md)
</dt> <dt>

[**Список воспроизведения. Дропдовнимаже**](playlist-dropdownimage.md)
</dt> <dt>

[**Список воспроизведения. Хуешифт**](playlist-hueshift.md)
</dt> </dl>

 

 





