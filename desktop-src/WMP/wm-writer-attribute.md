---
title: Атрибут WM/Writer
description: Атрибут WM/Writer — это имя средства записи, которое написало слова содержимого.
ms.assetid: e2035cf7-29f4-4642-9388-4cd7cb08149e
keywords:
- Проигрыватель Windows Media с атрибутом WM/Writer
topic_type:
- apiref
api_name:
- WM/Writer
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29aabf353fc742370ac5d01f084544be8143d3ec
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648841"
---
# <a name="wmwriter-attribute"></a>Атрибут WM/Writer

Атрибут **WM/Writer** — это имя средства записи, которое написало слова содержимого.

## <a name="applies-to"></a>Применение

-   [Звуковые элементы](audio-item-attributes.md)
-   [Часто используемые атрибуты файлов Windows Media](commonly-used-windows-media-file-attributes.md)
-   [Элементы видео](video-item-attributes.md)

## <a name="remarks"></a>Комментарии

Этот атрибут хранится как в библиотеке, так и в файле цифрового мультимедиа.

Этот атрибут может иметь несколько значений. Чтобы получить все значения атрибута с несколькими значениями, необходимо использовать метод **Media. жетитеминфобитипе** , а не метод **Media. getItemInfo** .

**Модуль записи** является псевдонимом для этого атрибута.

Константа Windows Media Format SDK для этого атрибута — g \_ всзвмвритер.

Чтобы определить, можно ли изменить значение этого атрибута, используйте метод [Media. исреадонлитем](media-isreadonlyitem.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------|
| Версия<br/> | Проигрыватель Windows Media 9 Series или более поздней версии<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Ссылка на атрибут**](attribute-reference.md)
</dt> <dt>

[**Media. Жетитеминфобитипе**](media-getiteminfobytype.md)
</dt> </dl>

 

 





