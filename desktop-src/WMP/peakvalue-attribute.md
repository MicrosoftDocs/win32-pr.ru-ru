---
title: Атрибут Пеаквалуе
description: Атрибут Пеаквалуе представляет собой 16-битное значение амплитуды, указывающее пиковый уровень громкости.
ms.assetid: 5d80a1f3-015c-4740-bd1c-f3bbf88a9df2
keywords:
- Пеаквалуе атрибут Windows Media Player
topic_type:
- apiref
api_name:
- PeakValue
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74fde522e043adb8b11c25bede763bed6b252f2f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699118"
---
# <a name="peakvalue-attribute"></a>Атрибут Пеаквалуе

Атрибут **пеаквалуе** представляет собой 16-битное значение амплитуды, указывающее пиковый уровень громкости.

## <a name="applies-to"></a>Применение

-   [Звуковые элементы](audio-item-attributes.md)
-   [Часто используемые файлы Windows Media](commonly-used-windows-media-file-attributes.md)

## <a name="remarks"></a>Комментарии

Этот атрибут хранится как в библиотеке, так и в файле цифрового мультимедиа.

Проигрыватель Windows Media задает это значение в одном из следующих экземпляров:

-   После копирования файла на скопированный файл.
-   После воспроизведения файла (при включенном улучшении автоматического выравнивания громкости).

Константа Windows Media Format SDK для этого атрибута — g \_ всзпеаквалуе.

Чтобы определить, можно ли изменить значение этого атрибута, используйте метод [Media. исреадонлитем](media-isreadonlyitem.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------|
| Версия<br/> | Проигрыватель Windows Media 9 Series или более поздней версии<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Ссылка на атрибут**](attribute-reference.md)
</dt> </dl>

 

 





