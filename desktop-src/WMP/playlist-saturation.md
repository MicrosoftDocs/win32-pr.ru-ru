---
title: Список воспроизведения. насыщенность
description: Атрибут насыщенности указывает или получает значение насыщенности раскрывающихся изображений.
ms.assetid: 4c5dd3d9-828a-45c9-896a-9a702d354544
keywords:
- список воспроизведения. насыщенность проигрыватель Windows Media
topic_type:
- apiref
api_name:
- PLAYLIST.saturation
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f5ce3c576fd923dae5c7a6cb4b7227b67dbebd87c6a497fc6c48e6e453b53f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118336540"
---
# <a name="playlistsaturation"></a>Список воспроизведения. насыщенность

Атрибут **насыщенности** указывает или получает значение насыщенности раскрывающихся изображений.

``` syntax
        elementID.saturation
```

## <a name="possible-values"></a>Возможные значения

Этот атрибут является **числом** для чтения и записи (**float**) со значением в диапазоне от 0,0 до 2,0 со значением по умолчанию 1,0.

## <a name="remarks"></a>Remarks

Этот атрибут изменяет значение насыщенности изображений, заданных атрибутами **дропдовнбаккграундимаже** и **дропдовнимаже** , если они заданы и ссылаются на 8-битные изображения BMP.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|---------------------------------------------------|
| Версия<br/> | проигрыватель Windows Media 9 Series или более поздней версии<br/> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Элемент списка воспроизведения**](playlist-element.md)
</dt> <dt>

[**Список воспроизведения. Дропдовнбаккграундимаже**](playlist-dropdownbackgroundimage.md)
</dt> <dt>

[**Список воспроизведения. Дропдовнимаже**](playlist-dropdownimage.md)
</dt> <dt>

[**Список воспроизведения. Хуешифт**](playlist-hueshift.md)
</dt> </dl>

 

 





