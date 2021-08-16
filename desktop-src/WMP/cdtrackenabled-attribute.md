---
title: Атрибут Кдтраккенаблед
description: Атрибут Кдтраккенаблед указывает, включена ли запись для воспроизведения.
ms.assetid: ebbc42bd-2d6c-47ae-9a3f-c6256b120d35
keywords:
- проигрыватель Windows Media атрибута кдтраккенаблед
topic_type:
- apiref
api_name:
- CDTrackEnabled
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a86c94c2c1b44327cdbfb35544c3e0b5b34d25885215d78dbec0ec084d056e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118342687"
---
# <a name="cdtrackenabled-attribute"></a>Атрибут Кдтраккенаблед

Атрибут **кдтраккенаблед** указывает, включена ли запись для воспроизведения.

## <a name="applies-to"></a>Применяется к

-   [Дорожки компакт-диска](cd-track-attributes.md)

## <a name="remarks"></a>Remarks

Этот атрибут хранится только в кэше библиотеки.

при воспроизведении компакт-диска в проигрыватель Windows Media пользователь может выбрать запись и указать, что ее не следует воспроизводить. Это значение атрибута равно true, если запись может быть воспроизведена, или false, если пользователь указал, что трассировка не должна воспроизводиться.

Чтобы определить, можно ли изменить значение этого атрибута, используйте метод [Media. исреадонлитем](media-isreadonlyitem.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------|
| Версия<br/> | проигрыватель Windows Media 9 Series или более поздней версии<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Ссылка на атрибут**](attribute-reference.md)
</dt> </dl>

 

 





