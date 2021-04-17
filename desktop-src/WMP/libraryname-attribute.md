---
title: Атрибут ИмяБиблиотеки
description: Атрибут ИмяБиблиотеки — это имя библиотеки, к которой принадлежит элемент.
ms.assetid: 70ce2de1-6c7b-427a-ba48-a9f69bacd015
keywords:
- ИмяБиблиотеки атрибут Windows Media Player
topic_type:
- apiref
api_name:
- LibraryName
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 263023c9881e109efe77ec30c1e37091200c051b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694991"
---
# <a name="libraryname-attribute"></a>Атрибут ИмяБиблиотеки

Атрибут ИмяБиблиотеки — это имя библиотеки, к которой принадлежит элемент.

## <a name="applies-to"></a>Применение

-   [**Звуковые элементы**](audio-item-attributes.md)
-   [**Элементы фото**](photo-item-attributes.md)
-   [**Элементы списка воспроизведения**](playlist-attributes-ref.md)
-   [**Элементы видео**](video-item-attributes.md)

## <a name="remarks"></a>Комментарии

Элемент мультимедиа может принадлежать к локальной библиотеке текущего пользователя или к библиотеке, которая стала доступна другим пользователям в домашней сети.

Значение этого атрибута совпадает со значением, возвращаемым методом [**ивмплибрари:: Get \_ Name**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibrary-get_name) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------|
| Версия<br/> | Проигрыватель Windows Media 12<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Ссылка на атрибут**](attribute-reference.md)
</dt> </dl>

 

 





