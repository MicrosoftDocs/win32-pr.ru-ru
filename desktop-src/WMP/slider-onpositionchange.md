---
title: ПОЛЗУНок. Онпоситиончанже
description: Обработчик событий Онпоситиончанже обрабатывает событие, возникающее при изменении положения ползунка в результате нажатия или перетаскивания пользователем. | ПОЛЗУНок. Онпоситиончанже
ms.assetid: c18e9a49-9576-42ae-9f30-249c44d40f41
keywords:
- ПОЛЗУНок. Онпоситиончанже Windows Media Player
topic_type:
- apiref
api_name:
- SLIDER.onPositionChange
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd68faa9e7addd85b9b5f02b8a6c445e7ddf54e9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698833"
---
# <a name="slideronpositionchange"></a>ПОЛЗУНок. Онпоситиончанже

Обработчик событий **онпоситиончанже** обрабатывает событие, возникающее при изменении положения ползунка в результате нажатия или перетаскивания пользователем.

``` syntax
onPositionChange
```

## <a name="remarks"></a>Комментарии

Если положение ползунка изменяется в результате изменения атрибута **значения** в скрипте, это событие не срабатывает. Чтобы справиться с этой возможностью, реализуйте вместо него обработчик события **\_ onChange** .

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------|
| Версия<br/> | Проигрыватель Windows Media версии 7,0 или более поздней<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Элемент SLIDER**](slider-element.md)
</dt> </dl>

 

 





