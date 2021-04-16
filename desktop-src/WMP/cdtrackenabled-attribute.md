---
title: Атрибут Кдтраккенаблед
description: Атрибут Кдтраккенаблед указывает, включена ли запись для воспроизведения.
ms.assetid: ebbc42bd-2d6c-47ae-9a3f-c6256b120d35
keywords:
- Кдтраккенаблед атрибут Windows Media Player
topic_type:
- apiref
api_name:
- CDTrackEnabled
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c81c231dbdfc432ea7aa510a19b1f85e0826c836
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699170"
---
# <a name="cdtrackenabled-attribute"></a>Атрибут Кдтраккенаблед

Атрибут **кдтраккенаблед** указывает, включена ли запись для воспроизведения.

## <a name="applies-to"></a>Применение

-   [Дорожки компакт-диска](cd-track-attributes.md)

## <a name="remarks"></a>Комментарии

Этот атрибут хранится только в кэше библиотеки.

При воспроизведении компакт-диска в проигрывателе Windows Media пользователь может выбрать запись и указать, что ее не следует воспроизводить. Это значение атрибута равно true, если запись может быть воспроизведена, или false, если пользователь указал, что трассировка не должна воспроизводиться.

Чтобы определить, можно ли изменить значение этого атрибута, используйте метод [Media. исреадонлитем](media-isreadonlyitem.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------|
| Версия<br/> | Проигрыватель Windows Media 9 Series или более поздней версии<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Ссылка на атрибут**](attribute-reference.md)
</dt> </dl>

 

 





