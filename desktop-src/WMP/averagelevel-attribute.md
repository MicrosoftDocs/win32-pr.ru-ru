---
title: Атрибут Аверажелевел
description: Атрибут Аверажелевел представляет собой 16-битное значение амплитуды, указывающее средний уровень громкости.
ms.assetid: 04ff19f1-a9a5-4e47-86a6-50c6f08b0d7d
keywords:
- Аверажелевел атрибут Windows Media Player
topic_type:
- apiref
api_name:
- AverageLevel
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 594612f3675d818f94270b1952d2a9ca7bed15d7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694762"
---
# <a name="averagelevel-attribute"></a>Атрибут Аверажелевел

Атрибут **аверажелевел** представляет собой 16-битное значение амплитуды, указывающее средний уровень громкости.

## <a name="applies-to"></a>Применение

-   [Звуковые элементы](audio-item-attributes.md)
-   [Часто используемые файлы Windows Media](commonly-used-windows-media-file-attributes.md)

## <a name="remarks"></a>Комментарии

Этот атрибут хранится как в библиотеке, так и в файле цифрового мультимедиа.

Проигрыватель Windows Media задает это значение в одном из следующих экземпляров:

-   После копирования файла на скопированный файл.
-   После воспроизведения файла (при включенном улучшении автоматического выравнивания громкости).

Константа Windows Media Format SDK для этого атрибута — g \_ всзаверажелевел.

Чтобы определить, можно ли изменить значение этого атрибута, используйте метод [Media. исреадонлитем](media-isreadonlyitem.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------|
| Версия<br/> | Проигрыватель Windows Media 9 Series или более поздней версии<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Ссылка на атрибут**](attribute-reference.md)
</dt> </dl>

 

 





