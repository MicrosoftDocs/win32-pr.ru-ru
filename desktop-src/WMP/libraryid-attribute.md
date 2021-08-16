---
title: Атрибут Либрарид
description: Атрибут Либрарид является идентификатором библиотеки, к которой принадлежит элемент.
ms.assetid: 680d9374-8729-4258-8672-b4b93b65e20a
keywords:
- проигрыватель Windows Media атрибута либрарид
topic_type:
- apiref
api_name:
- LibraryID Attribute
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a011db4e18509761c232bcf5439e33445128ef77c50945f84662a7b7956f607f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119468224"
---
# <a name="libraryid-attribute"></a>Атрибут Либрарид

Атрибут **либрарид** является идентификатором библиотеки, к которой принадлежит элемент.

## <a name="applies-to"></a>Применяется к

-   [**Звуковые элементы**](audio-item-attributes.md)
-   [**Элементы фото**](photo-item-attributes.md)
-   [**Элементы списка воспроизведения**](playlist-attributes-ref.md)
-   [**Элементы видео**](video-item-attributes.md)

## <a name="remarks"></a>Remarks

Элемент мультимедиа может принадлежать к локальной библиотеке текущего пользователя или к библиотеке, которая стала доступна другим пользователям в домашней сети или Интернете.

Значение этого атрибута совпадает со значением, возвращаемым методом [**IWMPLibrary2:: getItemInfo**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibrary-get_name) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------|
| Версия<br/> | проигрыватель Windows Media 12<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Ссылка на атрибут**](attribute-reference.md)
</dt> </dl>

 

 





