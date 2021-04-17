---
title: TEXT. Текствидс
description: Атрибут Текствидс извлекает ширину (в пикселях) текста, содержащегося в атрибуте value.
ms.assetid: 46c34659-f441-467c-8846-45785f7a2736
keywords:
- Проигрыватель Windows Media TEXT. Текствидс
topic_type:
- apiref
api_name:
- TEXT.textWidth
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17ce93517837aecf737336137df3cf5d8bf292dd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704487"
---
# <a name="texttextwidth"></a>TEXT. Текствидс

Атрибут **текствидс** извлекает ширину (в пикселях) текста, содержащегося в атрибуте **value** .

``` syntax
        elementID.textWidth
```

## <a name="possible-values"></a>Возможные значения

Этот атрибут является **числом** только для чтения (**int**).

## <a name="remarks"></a>Комментарии

Возвращаемое значение основано на атрибутах **фонтфаце**, **fontSize** и **FontStyle** , а также на реальных символах в строке атрибута **значения** .

См. атрибут [value](text-value.md) для примера, иллюстрирующий использование атрибутов **текстового** элемента.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------|
| Версия<br/> | Проигрыватель Windows Media версии 7,0 или более поздней<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**TEXT, элемент**](text-element.md)
</dt> <dt>

[**TEXT. Фонтфаце**](text-fontface.md)
</dt> <dt>

[**TEXT. fontSize**](text-fontsize.md)
</dt> <dt>

[**TEXT. fontStyle**](text-fontstyle.md)
</dt> <dt>

[**TEXT. Value**](text-value.md)
</dt> </dl>

 

 





