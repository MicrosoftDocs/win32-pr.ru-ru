---
title: Атрибут WM/Composer
description: Атрибут WM/Composer — это имя композитора музыки.
ms.assetid: 48459027-ed80-46a2-ad5c-ace602144150
keywords:
- Проигрыватель Windows Media с атрибутом WM/Composer
topic_type:
- apiref
api_name:
- WM/Composer
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2f206b1a23126612f3f7c875b9a9b4badca8339
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704316"
---
# <a name="wmcomposer-attribute"></a>Атрибут WM/Composer

Атрибут **WM/Composer** — это имя композитора музыки.

## <a name="applies-to"></a>Применение

-   [Звуковые элементы](audio-item-attributes.md)
-   [Списки воспроизведения компакт-дисков](cd-playlist-attributes.md)
-   [Дорожки компакт-диска](cd-track-attributes.md)
-   [Часто используемые атрибуты файлов Windows Media](commonly-used-windows-media-file-attributes.md)

## <a name="remarks"></a>Комментарии

Этот атрибут хранится как в библиотеке (или в кэше), так и в файле цифрового носителя.

Этот атрибут может иметь несколько значений. Чтобы получить все значения атрибута с несколькими значениями, необходимо использовать метод **Media. жетитеминфобитипе** , а не метод **Media. getItemInfo** .

**Composer** — это псевдоним для этого атрибута.

Константа Windows Media Format SDK для этого атрибута — g \_ всзвмкомпосер.

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

 

 





