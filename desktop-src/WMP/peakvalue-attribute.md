---
title: Атрибут Пеаквалуе
description: Атрибут Пеаквалуе представляет собой 16-битное значение амплитуды, указывающее пиковый уровень громкости.
ms.assetid: 5d80a1f3-015c-4740-bd1c-f3bbf88a9df2
keywords:
- проигрыватель Windows Media атрибута пеаквалуе
topic_type:
- apiref
api_name:
- PeakValue
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5aa2a661342b305155717f4f11336f540e1ae53524ff2d303a2ab790e2c73af7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118573588"
---
# <a name="peakvalue-attribute"></a>Атрибут Пеаквалуе

Атрибут **пеаквалуе** представляет собой 16-битное значение амплитуды, указывающее пиковый уровень громкости.

## <a name="applies-to"></a>Применяется к

-   [Звуковые элементы](audio-item-attributes.md)
-   [часто используемые Windows файлы мультимедиа](commonly-used-windows-media-file-attributes.md)

## <a name="remarks"></a>Remarks

Этот атрибут хранится как в библиотеке, так и в файле цифрового мультимедиа.

проигрыватель Windows Media задает это значение в одном из следующих экземпляров:

-   После копирования файла на скопированный файл.
-   После воспроизведения файла (при включенном улучшении автоматического выравнивания громкости).

константа пакета SDK Windows Media Format для этого атрибута — g \_ всзпеаквалуе.

Чтобы определить, можно ли изменить значение этого атрибута, используйте метод [Media. исреадонлитем](media-isreadonlyitem.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------|
| Версия<br/> | проигрыватель Windows Media 9 Series или более поздней версии<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Ссылка на атрибут**](attribute-reference.md)
</dt> </dl>

 

 





