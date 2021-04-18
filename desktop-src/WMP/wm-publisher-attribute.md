---
title: Атрибут WM/Publisher
description: Атрибут WM/Publisher — это имя компании, опубликовавшего содержимое.
ms.assetid: 5f3aa5de-237e-449c-918e-8750481adc6f
keywords:
- Проигрыватель Windows Media с атрибутом WM/Publisher
topic_type:
- apiref
api_name:
- WM/Publisher
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00bd0d2ab2b6d886639cffa1df0770dfe329f7f4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718015"
---
# <a name="wmpublisher-attribute"></a>Атрибут WM/Publisher

Атрибут **WM/Publisher** — это имя компании, опубликовавшего содержимое.

## <a name="applies-to"></a>Применение

-   [Звуковые элементы](audio-item-attributes.md)
-   [Списки воспроизведения компакт-дисков](cd-playlist-attributes.md)
-   [Дорожки компакт-диска](cd-track-attributes.md)
-   [Часто используемые атрибуты файлов Windows Media](commonly-used-windows-media-file-attributes.md)
-   [DVD-диски](dvd-attributes.md)
-   [Элементы видео](video-item-attributes.md)

## <a name="remarks"></a>Комментарии

Этот атрибут хранится как в библиотеке (или в кэше), так и в файле цифрового носителя.

**Label**, **релеаседби** и **Studio** являются псевдонимами для этого атрибута.

Константа Windows Media Format SDK для этого атрибута — g \_ всзвмпублишер.

Чтобы определить, можно ли изменить значение этого атрибута, используйте метод [Media. исреадонлитем](media-isreadonlyitem.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------|
| Версия<br/> | Проигрыватель Windows Media 9 Series или более поздней версии<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Ссылка на атрибут**](attribute-reference.md)
</dt> </dl>

 

 





