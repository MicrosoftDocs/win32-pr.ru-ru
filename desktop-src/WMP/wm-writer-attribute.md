---
title: Атрибут WM/Writer
description: Атрибут WM/Writer — это имя средства записи, которое написало слова содержимого.
ms.assetid: e2035cf7-29f4-4642-9388-4cd7cb08149e
keywords:
- проигрыватель Windows Media атрибута WM/Writer
topic_type:
- apiref
api_name:
- WM/Writer
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a239fd83c936a0712459307fbf08b01c4bfcc4f6fd4c6d32cddc12d8092f2b2c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118332060"
---
# <a name="wmwriter-attribute"></a>Атрибут WM/Writer

Атрибут **WM/Writer** — это имя средства записи, которое написало слова содержимого.

## <a name="applies-to"></a>Применяется к

-   [Звуковые элементы](audio-item-attributes.md)
-   [часто используемые Windows атрибуты файла мультимедиа](commonly-used-windows-media-file-attributes.md)
-   [Элементы видео](video-item-attributes.md)

## <a name="remarks"></a>Remarks

Этот атрибут хранится как в библиотеке, так и в файле цифрового мультимедиа.

Этот атрибут может иметь несколько значений. Чтобы получить все значения атрибута с несколькими значениями, необходимо использовать метод **Media. жетитеминфобитипе** , а не метод **Media. getItemInfo** .

**Модуль записи** является псевдонимом для этого атрибута.

константа пакета SDK Windows Media Format для этого атрибута — g \_ всзвмвритер.

Чтобы определить, можно ли изменить значение этого атрибута, используйте метод [Media. исреадонлитем](media-isreadonlyitem.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------|
| Версия<br/> | проигрыватель Windows Media 9 Series или более поздней версии<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Ссылка на атрибут**](attribute-reference.md)
</dt> <dt>

[**Media. Жетитеминфобитипе**](media-getiteminfobytype.md)
</dt> </dl>

 

 





