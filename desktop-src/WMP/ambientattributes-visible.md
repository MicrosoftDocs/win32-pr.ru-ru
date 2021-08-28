---
title: Амбиентаттрибутес. Visible
description: Атрибут Visible указывает или получает видимость для элемента управления.
ms.assetid: 8347d42a-4af1-4ea1-b968-a2ae58278430
keywords:
- амбиентаттрибутес. visible проигрыватель Windows Media
topic_type:
- apiref
api_name:
- AmbientAttributes.visible
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6136bbdba7fe222c16e6185bc2ddfa243c5387443122fb93eb1d6564ad01c956
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120124054"
---
# <a name="ambientattributesvisible"></a>Амбиентаттрибутес. Visible

Атрибут **Visible** указывает или получает видимость для элемента управления.

``` syntax
        elementID.visible
```

## <a name="possible-values"></a>Возможные значения

Этот атрибут является **логическим значением** для чтения и записи.



| Значение | Описание                      |
|-------|----------------------------------|
| Да  | По умолчанию. Элемент управления является видимым. |
| false | Элемент управления невидим.      |



 

## <a name="remarks"></a>Remarks

Этот атрибут полезен для скрытия элементов управления, например при переключении кнопки паузы на кнопку воспроизведения.

Если значение равно false, элемент управления не отображается, а события щелчка передаются в элемент управления, лежащий за ним. Если значение равно true, элемент управления является видимым и получает событие Click.

Значение по умолчанию для элемента **АВТОМЕНЮ** — false.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------|
| Версия<br/> | проигрыватель Windows Media версии 7,0 или более поздней<br/> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Атрибуты окружения**](ambient-attributes.md)
</dt> </dl>

 

 





