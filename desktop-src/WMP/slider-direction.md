---
title: ПОЛЗУНок. Direction
description: Атрибут Direction указывает или получает направление, в котором размещаются изображения ползунков.
ms.assetid: a6add56b-3fc6-4c78-90e4-6daafd701eda
keywords:
- ПОЛЗУНок. Направление проигрывателя Windows Media
topic_type:
- apiref
api_name:
- SLIDER.direction
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dfc49f2963747508c56573a7ff699f28e93113d9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657114"
---
# <a name="sliderdirection"></a>ПОЛЗУНок. Direction

Атрибут **Direction** указывает или получает направление, в котором размещаются изображения ползунков.

``` syntax
        elementID.direction
```

## <a name="possible-values"></a>Возможные значения

Этот атрибут является **строкой** для чтения и записи.



| Значение      | Описание                                                                             |
|------------|-----------------------------------------------------------------------------------------|
| horizontal | По умолчанию. Минимальная позиции — слева, а максимальная — справа. |
| Вертикаль   | Минимальная позиции находится в нижней части, а максимальная — вверху.          |



 

## <a name="remarks"></a>Комментарии

Заливка или перемещение **foregroundColor** или **фореграундимаже** находится вдоль вертикальной или горизонтальной оси в соответствии с указанным значением.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------|
| Версия<br/> | Проигрыватель Windows Media версии 7,0 или более поздней<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Элемент SLIDER**](slider-element.md)
</dt> <dt>

[**ПОЛЗУНок. foregroundColor**](slider-foregroundcolor.md)
</dt> <dt>

[**ПОЛЗУНок. Фореграундимаже**](slider-foregroundimage.md)
</dt> </dl>

 

 





