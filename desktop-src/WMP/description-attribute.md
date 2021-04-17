---
title: Атрибут Description (пакет SDK для проигрывателя)
description: Атрибут Description является описанием содержимого.
ms.assetid: 8bf76bf5-2bba-4ceb-bc98-f8b8ab2c8b6f
keywords:
- Описание атрибут Windows Media Player
topic_type:
- apiref
api_name:
- Description
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78c4bc3562e7b807dc0e333c887aad1550d05b0b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694761"
---
# <a name="description-attribute"></a>Атрибут Description

Атрибут **Description** является описанием содержимого.

## <a name="applies-to"></a>Применение

-   [Музыкальные файлы](music-file-attributes.md)

## <a name="remarks"></a>Комментарии

Этот атрибут хранится в музыкальных файлах, а не в библиотеке.

Этот атрибут может иметь несколько значений. Чтобы получить все значения атрибута с несколькими значениями, необходимо использовать *носитель*. метод **жетитеминфобитипе** , а не метод *Media*. getItemInfo.

Константа Windows Media Format SDK для этого атрибута — g \_ всзвмдескриптион.

Чтобы определить, можно ли изменить значение этого атрибута, используйте метод [Media. исреадонлитем](media-isreadonlyitem.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------|
| Версия<br/> | Проигрыватель Windows Media 9 Series или более поздней версии<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Ссылка на атрибут**](attribute-reference.md)
</dt> </dl>

 

 





