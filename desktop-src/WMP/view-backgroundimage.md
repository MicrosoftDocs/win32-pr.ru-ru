---
title: Просмотр. backgroundImage
description: Атрибут backgroundImage указывает или получает фоновое изображение представления или подпредставления.
ms.assetid: 60ffb257-2f43-4ae3-869d-3eb981ef4ae7
keywords:
- просмотр. backgroundImage проигрыватель Windows Media
topic_type:
- apiref
api_name:
- VIEW.backgroundImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c1de8bcbd0eb47f03aaff46b4292a8afe226ca8a221ec570537351af8e509801
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119761744"
---
# <a name="viewbackgroundimage"></a>Просмотр. backgroundImage

Атрибут **backgroundImage** указывает или получает фоновое изображение **представления** или **подпредставления**.

``` syntax
        elementID.backgroundImage
```

## <a name="possible-values"></a>Возможные значения

Этот атрибут является **строкой** для чтения и записи.

## <a name="remarks"></a>Remarks

Поддерживаются форматы BMP, JPG, GIF и PNG. Если изображение является 8-битным файлом BMP, его значения тона и насыщенности можно динамически изменить с помощью атрибутов **баккграундимажехуешифт** и **баккграундимажесатуратион** .

в пакете скачивания Windows носителя, если для элемента **представления** задан атрибут **backgroundImage** , необходимо также указать атрибут **backgroundColor** для этого элемента.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|------------------------------------------------------|
| Версия<br/> | проигрыватель Windows Media версии 7,0 или более поздней<br/> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**VIEW, элемент**](view-element.md)
</dt> <dt>

[**VIEW. Баккграундимажехуешифт**](view-backgroundimagehueshift.md)
</dt> <dt>

[**VIEW. Баккграундимажесатуратион**](view-backgroundimagesaturation.md)
</dt> </dl>

 

 





