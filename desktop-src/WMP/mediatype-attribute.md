---
title: Атрибут MediaType
description: Атрибут MediaType — это тип содержимого элемента.
ms.assetid: 0d8a6937-32d8-4a4a-87e5-0002f077fefe
keywords:
- Проигрыватель Windows Media, атрибут MediaType
topic_type:
- apiref
api_name:
- MediaType
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5779552f62007aa3dd3da0e2f4253fcf5499a6be
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651817"
---
# <a name="mediatype-attribute"></a>Атрибут MediaType

Атрибут **mediaType** — это тип содержимого элемента.

## <a name="applies-to"></a>Применение

-   [Звуковые элементы](audio-item-attributes.md)
-   [Другие элементы](other-item-attributes.md)
-   [Элементы фото](photo-item-attributes.md)
-   [Списки воспроизведения](playlist-attributes-ref.md)
-   [Элементы Радио](radio-item-attributes.md)
-   [Элементы видео](video-item-attributes.md)

## <a name="remarks"></a>Комментарии

Этот атрибут хранится только в библиотеке.

Этот атрибут имеет одно из следующих значений: "звук", "другое", "Фото", "список воспроизведения", "Радио" или "видео". Используйте этот атрибут с параметром *медиаколлектион*. метод **жетбяттрибуте** для получения списка воспроизведения, содержащего все элементы определенного типа.

Чтобы определить, можно ли изменить значение этого атрибута, используйте метод [Media. исреадонлитем](media-isreadonlyitem.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------|
| Версия<br/> | Проигрыватель Windows Media 9 Series или более поздней версии<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Ссылка на атрибут**](attribute-reference.md)
</dt> <dt>

[**Медиаколлектион. Жетбяттрибуте**](mediacollection-getbyattribute.md)
</dt> </dl>

 

 





