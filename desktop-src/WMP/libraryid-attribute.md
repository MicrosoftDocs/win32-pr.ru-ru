---
title: Атрибут Либрарид
description: Атрибут Либрарид является идентификатором библиотеки, к которой принадлежит элемент.
ms.assetid: 680d9374-8729-4258-8672-b4b93b65e20a
keywords:
- Либрарид атрибут Windows Media Player
topic_type:
- apiref
api_name:
- LibraryID Attribute
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 47ae9e5ad097bc188b8de1e76a09448c57aa9b83
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694994"
---
# <a name="libraryid-attribute"></a>Атрибут Либрарид

Атрибут **либрарид** является идентификатором библиотеки, к которой принадлежит элемент.

## <a name="applies-to"></a>Применение

-   [**Звуковые элементы**](audio-item-attributes.md)
-   [**Элементы фото**](photo-item-attributes.md)
-   [**Элементы списка воспроизведения**](playlist-attributes-ref.md)
-   [**Элементы видео**](video-item-attributes.md)

## <a name="remarks"></a>Комментарии

Элемент мультимедиа может принадлежать к локальной библиотеке текущего пользователя или к библиотеке, которая стала доступна другим пользователям в домашней сети или Интернете.

Значение этого атрибута совпадает со значением, возвращаемым методом [**IWMPLibrary2:: getItemInfo**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibrary-get_name) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------|
| Версия<br/> | Проигрыватель Windows Media 12<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Ссылка на атрибут**](attribute-reference.md)
</dt> </dl>

 

 





