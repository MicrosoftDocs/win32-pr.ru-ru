---
title: Атрибут Аверажелевел
description: Атрибут Аверажелевел представляет собой 16-битное значение амплитуды, указывающее средний уровень громкости.
ms.assetid: 04ff19f1-a9a5-4e47-86a6-50c6f08b0d7d
keywords:
- проигрыватель Windows Media атрибута аверажелевел
topic_type:
- apiref
api_name:
- AverageLevel
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e169b1e2d63e6f8215515acc852d431ff13ccd513924e4c2a237b16c17dacfc0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118582749"
---
# <a name="averagelevel-attribute"></a>Атрибут Аверажелевел

Атрибут **аверажелевел** представляет собой 16-битное значение амплитуды, указывающее средний уровень громкости.

## <a name="applies-to"></a>Применяется к

-   [Звуковые элементы](audio-item-attributes.md)
-   [часто используемые Windows файлы мультимедиа](commonly-used-windows-media-file-attributes.md)

## <a name="remarks"></a>Remarks

Этот атрибут хранится как в библиотеке, так и в файле цифрового мультимедиа.

проигрыватель Windows Media задает это значение в одном из следующих экземпляров:

-   После копирования файла на скопированный файл.
-   После воспроизведения файла (при включенном улучшении автоматического выравнивания громкости).

константа пакета SDK Windows Media Format для этого атрибута — g \_ всзаверажелевел.

Чтобы определить, можно ли изменить значение этого атрибута, используйте метод [Media. исреадонлитем](media-isreadonlyitem.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------|
| Версия<br/> | проигрыватель Windows Media 9 Series или более поздней версии<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Ссылка на атрибут**](attribute-reference.md)
</dt> </dl>

 

 





