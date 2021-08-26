---
title: атрибут WM/Composer
description: атрибут WM/Composer — это имя композитора музыки.
ms.assetid: 48459027-ed80-46a2-ad5c-ace602144150
keywords:
- проигрыватель Windows Media атрибута WM/Composer
topic_type:
- apiref
api_name:
- WM/Composer
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f41e92e1f343ecbd532769560a6d2d555c275e147ab2386ae574c2dea8bc411c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120001174"
---
# <a name="wmcomposer-attribute"></a>атрибут WM/Composer

атрибут **WM/Composer** — это имя композитора музыки.

## <a name="applies-to"></a>Применяется к

-   [Звуковые элементы](audio-item-attributes.md)
-   [Списки воспроизведения компакт-дисков](cd-playlist-attributes.md)
-   [Дорожки компакт-диска](cd-track-attributes.md)
-   [часто используемые Windows атрибуты файла мультимедиа](commonly-used-windows-media-file-attributes.md)

## <a name="remarks"></a>Remarks

Этот атрибут хранится как в библиотеке (или в кэше), так и в файле цифрового носителя.

Этот атрибут может иметь несколько значений. Чтобы получить все значения атрибута с несколькими значениями, необходимо использовать метод **Media. жетитеминфобитипе** , а не метод **Media. getItemInfo** .

**Composer** является псевдонимом для этого атрибута.

константа пакета SDK Windows Media Format для этого атрибута — g \_ всзвмкомпосер.

Чтобы определить, можно ли изменить значение этого атрибута, используйте метод [Media. исреадонлитем](media-isreadonlyitem.md) .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|---------------------------------------------------|
| Версия<br/> | проигрыватель Windows Media 9 Series или более поздней версии<br/> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Ссылка на атрибут**](attribute-reference.md)
</dt> <dt>

[**Media. Жетитеминфобитипе**](media-getiteminfobytype.md)
</dt> </dl>

 

 





