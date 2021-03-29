---
title: Список воспроизведения. itemCount
description: Атрибут itemCount извлекает количество элементов, отображаемых в данный момент в элементе списка воспроизведения.
ms.assetid: d090d95c-e3c3-41bc-951e-ffeb0a314a0c
keywords:
- Проигрыватель Windows Media Player. itemCount
topic_type:
- apiref
api_name:
- PLAYLIST.itemCount
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cbde81ee6c2849a19c6400fee4ef7fa6514eaefe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657949"
---
# <a name="playlistitemcount"></a>Список воспроизведения. itemCount

Атрибут **ItemCount** извлекает количество элементов, отображаемых в данный момент в элементе **списка воспроизведения** .

``` syntax
        elementID.itemCount
```

## <a name="possible-values"></a>Возможные значения

Этот атрибут является **числом** только для чтения (**длинное целое**).

## <a name="remarks"></a>Комментарии

Свойство **ItemCount** будет считать общее число развернутых элементов. Например, если имеется два списка воспроизведения, каждый из которых содержит три элемента мультимедиа, **ItemCount** возвратит 2, если списки воспроизведения не развернуты. Если развернут только первый список воспроизведения, **ItemCount** возвратит 4. Если оба списка воспроизведения развернуты, **ItemCount** возвратит значение 6.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------|
| Версия<br/> | Проигрыватель Windows Media 9 Series или более поздней версии<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Элемент списка воспроизведения**](playlist-element.md)
</dt> </dl>

 

 





