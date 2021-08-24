---
title: ПОЛЗУНок. Онпоситиончанже
description: Обработчик событий Онпоситиончанже обрабатывает событие, возникающее при изменении положения ползунка в результате нажатия или перетаскивания пользователем. | ПОЛЗУНок. Онпоситиончанже
ms.assetid: c18e9a49-9576-42ae-9f30-249c44d40f41
keywords:
- проигрыватель Windows Media SLIDER. онпоситиончанже
topic_type:
- apiref
api_name:
- SLIDER.onPositionChange
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e45fbb87c8b48b008c3f7d60d9bc83685fd24d8160e7eaf075dcd0b1b94b9141
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119507774"
---
# <a name="slideronpositionchange"></a>ПОЛЗУНок. Онпоситиончанже

Обработчик событий **онпоситиончанже** обрабатывает событие, возникающее при изменении положения ползунка в результате нажатия или перетаскивания пользователем.

``` syntax
onPositionChange
```

## <a name="remarks"></a>Remarks

Если положение ползунка изменяется в результате изменения атрибута **значения** в скрипте, это событие не срабатывает. Чтобы справиться с этой возможностью, реализуйте вместо него обработчик события **\_ onChange** .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|------------------------------------------------------|
| Версия<br/> | проигрыватель Windows Media версии 7,0 или более поздней<br/> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Элемент SLIDER**](slider-element.md)
</dt> </dl>

 

 





