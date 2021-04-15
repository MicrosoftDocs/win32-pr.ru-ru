---
title: VIEW. backgroundColor
description: Атрибут backgroundColor указывает или получает цвет фона для представления или подпредставления.
ms.assetid: 02804e03-3518-4825-8ad0-bf91f74b5f74
keywords:
- Просмотреть. backgroundColor проигрыватель Windows Media
topic_type:
- apiref
api_name:
- VIEW.backgroundColor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73bbee10c6f442c9c03f46baa26251a7f6f85c22
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648055"
---
# <a name="viewbackgroundcolor"></a>VIEW. backgroundColor

Атрибут **backgroundColor** указывает или получает цвет фона для **представления** или **подпредставления**.

``` syntax
        elementID.backgroundColor
```

## <a name="possible-values"></a>Возможные значения

Этот атрибут является **строкой** для чтения и записи, содержащей любое значение цвета Microsoft Internet Explorer, или значение None. Он имеет значение по умолчанию "белый" для элементов **представления** или "нет" для элементов вложенного **представления** .

Если в пакете загрузки Windows Media задан атрибут backgroundImage для элемента **View** , необходимо также указать атрибут **backgroundColor** для этого элемента.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------|
| Версия<br/> | Проигрыватель Windows Media версии 7,0 или более поздней<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Ссылка на цвет**](color-reference.md)
</dt> <dt>

[**VIEW, элемент**](view-element.md)
</dt> </dl>

 

 





