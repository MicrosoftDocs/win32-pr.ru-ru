---
title: Список воспроизведения. backgroundImage
description: Атрибут backgroundImage указывает или получает фоновое изображение.
ms.assetid: d4efa774-d42e-4415-a487-1e858d984075
keywords:
- Проигрыватель Windows Media. backgroundImage
topic_type:
- apiref
api_name:
- PLAYLIST.backgroundImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7eca04f47f6e157d5ede529c47fb6ae65b4333cf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708331"
---
# <a name="playlistbackgroundimage"></a>Список воспроизведения. backgroundImage

Атрибут **backgroundImage** указывает или получает фоновое изображение.

``` syntax
        elementID.backgroundImage
```

## <a name="possible-values"></a>Возможные значения

Этот атрибут является **строкой** для чтения и записи, содержащей имя файла изображения. У него нет значения по умолчанию.

## <a name="remarks"></a>Комментарии

Если высота и ширина изображения меньше, чем высота и ширина элемента **списка воспроизведения** , изображение будет мозаичным. Поддерживаются форматы BMP, JPG, GIF и PNG.

Указание значения "градиент" для фонового изображения приводит к тому, что фон списка воспроизведения отображается как цветовой градиент. Это означает, что цвет фона постепенно переходит между [списком воспроизведения. backgroundColor](playlist-backgroundcolor.md) (в верхней части фона) и значениями [списка воспроизведения. статусколор](playlist-statuscolor.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------|
| Версия<br/> | Проигрыватель Windows Media версии 7,0 или более поздней, проигрыватель Windows Media 10 для функции градиента<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Элемент списка воспроизведения**](playlist-element.md)
</dt> </dl>

 

 





