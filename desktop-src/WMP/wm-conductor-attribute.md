---
title: Атрибут WM/проводника
description: Атрибут WM/проводника — это имя проводника музыки.
ms.assetid: 31c7d310-da6a-4c30-86b0-15defaee1743
keywords:
- Проигрыватель Windows Media с атрибутом WM/проводника
topic_type:
- apiref
api_name:
- WM/Conductor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d1ae08dfee807d130f04dd258c6af81a8d68057
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704315"
---
# <a name="wmconductor-attribute"></a>Атрибут WM/проводника

Атрибут **WM/проводника** — это имя проводника музыки.

## <a name="applies-to"></a>Применение

-   [Звуковые элементы](audio-item-attributes.md)
-   [Дорожки компакт-диска](cd-track-attributes.md)
-   [Часто используемые атрибуты файлов Windows Media](commonly-used-windows-media-file-attributes.md)

## <a name="remarks"></a>Комментарии

Этот атрибут хранится как в библиотеке (или в кэше), так и в файле цифрового носителя.

Этот атрибут может иметь несколько значений. Чтобы получить все значения атрибута с несколькими значениями, необходимо использовать метод **Media. жетитеминфобитипе** , а не метод **Media. getItemInfo** .

**Проводник** является псевдонимом для этого атрибута.

Константа Windows Media Format SDK для этого атрибута — g \_ всзвмкондуктор.

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

 

 





