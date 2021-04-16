---
title: Атрибут Албумид
description: Атрибут Албумид является уникальным идентификатором для альбома.
ms.assetid: 0412d91a-11a7-434c-8717-a71d85655679
keywords:
- Албумид атрибут Windows Media Player
topic_type:
- apiref
api_name:
- AlbumID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 339253c82554579fa549371e2ebe4cb2f1926cc5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699257"
---
# <a name="albumid-attribute"></a>Атрибут Албумид

Атрибут **албумид** является уникальным идентификатором для альбома.

## <a name="applies-to"></a>Применение

-   [Звуковые элементы](audio-item-attributes.md)

## <a name="remarks"></a>Комментарии

Этот атрибут хранится только в библиотеке.

Уникальный идентификатор представляет собой сочетание названия альбома и имени исполнителя альбома. В этом атрибуте сначала появляется заголовок альбома. При использовании метода [медиаколлектион. жетаттрибутестрингколлектион](mediacollection-getattributestringcollection.md) для получения объекта **StringCollection** с помощью этого атрибута значения сортируются по названию альбома.

Чтобы определить, можно ли изменить значение этого атрибута, используйте метод [Media. исреадонлитем](media-isreadonlyitem.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------|
| Версия<br/> | Проигрыватель Windows Media 9 Series или более поздней версии<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Атрибут Албумидалбумартист**](albumidalbumartist-attribute.md)
</dt> <dt>

[**Ссылка на атрибут**](attribute-reference.md)
</dt> </dl>

 

 





