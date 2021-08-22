---
title: Атрибут ИмяБиблиотеки
description: Атрибут ИмяБиблиотеки — это имя библиотеки, к которой принадлежит элемент.
ms.assetid: 70ce2de1-6c7b-427a-ba48-a9f69bacd015
keywords:
- проигрыватель Windows Media атрибута имябиблиотеки
topic_type:
- apiref
api_name:
- LibraryName
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57d2b86a1b551fab103db732dd5405187c06395f37b1ae59c030c3a75a05f275
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119054792"
---
# <a name="libraryname-attribute"></a>Атрибут ИмяБиблиотеки

Атрибут ИмяБиблиотеки — это имя библиотеки, к которой принадлежит элемент.

## <a name="applies-to"></a>Применяется к

-   [**Звуковые элементы**](audio-item-attributes.md)
-   [**Элементы фото**](photo-item-attributes.md)
-   [**Элементы списка воспроизведения**](playlist-attributes-ref.md)
-   [**Элементы видео**](video-item-attributes.md)

## <a name="remarks"></a>Remarks

Элемент мультимедиа может принадлежать к локальной библиотеке текущего пользователя или к библиотеке, которая стала доступна другим пользователям в домашней сети.

Значение этого атрибута совпадает со значением, возвращаемым методом [**ивмплибрари:: Get \_ Name**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibrary-get_name) .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|------------------------------------|
| Версия<br/> | проигрыватель Windows Media 12<br/> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Ссылка на атрибут**](attribute-reference.md)
</dt> </dl>

 

 





