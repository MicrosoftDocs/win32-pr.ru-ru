---
title: Список воспроизведения. backgroundImage
description: Атрибут backgroundImage указывает или получает фоновое изображение.
ms.assetid: d4efa774-d42e-4415-a487-1e858d984075
keywords:
- проигрыватель Windows Media списка воспроизведения. backgroundImage
topic_type:
- apiref
api_name:
- PLAYLIST.backgroundImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b56ddcb42f118a5a672b6678079825b6cb3d6aba5fbdc54953fb566e4222f583
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119054252"
---
# <a name="playlistbackgroundimage"></a>Список воспроизведения. backgroundImage

Атрибут **backgroundImage** указывает или получает фоновое изображение.

``` syntax
        elementID.backgroundImage
```

## <a name="possible-values"></a>Возможные значения

Этот атрибут является **строкой** для чтения и записи, содержащей имя файла изображения. У него нет значения по умолчанию.

## <a name="remarks"></a>Remarks

Если высота и ширина изображения меньше, чем высота и ширина элемента **списка воспроизведения** , изображение будет мозаичным. Поддерживаются форматы BMP, JPG, GIF и PNG.

Указание значения "градиент" для фонового изображения приводит к тому, что фон списка воспроизведения отображается как цветовой градиент. Это означает, что цвет фона постепенно переходит между [списком воспроизведения. backgroundColor](playlist-backgroundcolor.md) (в верхней части фона) и значениями [списка воспроизведения. статусколор](playlist-statuscolor.md) .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------|
| Версия<br/> | проигрыватель Windows Media версии 7,0 или более поздней, проигрыватель Windows Media 10 для функции градиента<br/> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Элемент списка воспроизведения**](playlist-element.md)
</dt> </dl>

 

 





