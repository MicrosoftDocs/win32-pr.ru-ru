---
title: Атрибут Author
description: Атрибут Author — это имя исполнителя или субъекта мультимедиа, связанного с содержимым.
ms.assetid: 6621a955-dd6b-4725-9690-0cc96e73d94f
keywords:
- Атрибут автора Windows Media Player
topic_type:
- apiref
api_name:
- Author
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e94ef73679aa3869a9a3d87b926b7f38464b1001
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698752"
---
# <a name="author-attribute"></a>Атрибут Author

Атрибут **Author** — это имя исполнителя или субъекта мультимедиа, связанного с содержимым.

## <a name="applies-to"></a>Применение

-   [Звуковые элементы](audio-item-attributes.md)
-   [Списки воспроизведения компакт-дисков](cd-playlist-attributes.md)
-   [Дорожки компакт-диска](cd-track-attributes.md)
-   [Часто используемые файлы Windows Media](commonly-used-windows-media-file-attributes.md)
-   [DVD-диски](dvd-attributes.md)
-   [Media. Жетитеминфобитипе](media-getiteminfobytype.md)
-   [Элементы фото](photo-item-attributes.md)
-   [Списки воспроизведения](playlist-attributes-ref.md)
-   [Элементы Радио](radio-item-attributes.md)
-   [Элементы видео](video-item-attributes.md)

## <a name="remarks"></a>Комментарии

Этот атрибут хранится как в библиотеке (или в кэше), так и в файле мультимедиа.

Этот атрибут может иметь несколько значений. Чтобы получить все значения атрибута с несколькими значениями, необходимо использовать *носитель*. метод **жетитеминфобитипе** , а не *носитель*. метод **getItemInfo** .

Константа Windows Media Format SDK для этого атрибута — g \_ всзвмаусор.

**Субъект** и **исполнитель** — это псевдонимы для этого атрибута.

Чтобы определить, можно ли изменить значение этого атрибута, используйте метод [Media. исреадонлитем](media-isreadonlyitem.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------|
| Версия<br/> | Проигрыватель Windows Media 9 Series или более поздней версии<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Ссылка на атрибут**](attribute-reference.md)
</dt> </dl>

 

 





