---
title: LISTBOX. popUp
description: Атрибут popUp задает значение, указывающее, представляет ли элемент элемент управления "всплывающее окно" или "список".
ms.assetid: b0ade23a-6164-4dd4-b599-43ea1fcd44e4
keywords:
- Проигрыватель Windows Media LISTBOX. popUp
topic_type:
- apiref
api_name:
- LISTBOX.popUp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43d197adbdf2ec27ea6ef7bf04c5c71d15ae923d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704424"
---
# <a name="listboxpopup"></a>LISTBOX. popUp

Атрибут **popUp** задает значение, указывающее, представляет ли элемент элемент управления "всплывающее окно" или "список".

``` syntax
<ELEMENT popUp="value">
```

## <a name="possible-values"></a>Возможные значения

Этот атрибут является **логическим** , заданным только во время разработки.



| Значение | Описание                                |
|-------|--------------------------------------------|
| true  | Элемент представляет элемент управления Popup.    |
| false | Элемент представляет элемент управления "список". |



 

## <a name="remarks"></a>Комментарии

Элемент **Popup** представляет элемент управления "список", который отображается только при необходимости. Он идентичен элементу **ListBox** , за исключением значения по умолчанию этого атрибута, которое изменяет поведение экрана. Для элементов **ListBox** значение по умолчанию — false. Для элементов **Popup** значение по умолчанию — true. Вместо указания этого атрибута следует использовать элемент **ListBox** или **Popup** в соответствии с желаемым поведением.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------------|
| Версия<br/> | Проигрыватель Windows Media для Windows XP или более поздней версии<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Элемент LISTBOX**](listbox-element.md)
</dt> <dt>

[**Элемент POPUP**](popup-element.md)
</dt> </dl>

 

 





