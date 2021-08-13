---
title: Элемент управления CHECKBOX (компилятор ресурсов)
description: Определяет элемент управления "флажок".
ms.assetid: 24ee25e5-9de2-4843-a55e-96b897f6ae8e
keywords:
- Меню элементов управления CHECKBOX и другие ресурсы
topic_type:
- apiref
api_name:
- CHECKBOX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab103291a919a166d63656718629a7781bdd5f3a4b3023283f2dd114decd966e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119461334"
---
# <a name="checkbox-control"></a>Элемент управления CHECKBOX

Определяет элемент управления "флажок". Элемент управления является небольшим прямоугольником (флажок), для которого рядом с ним отображается указанный текст (обычно справа). Когда пользователь выбирает элемент управления, элемент управления выделяет прямоугольник и отправляет сообщение родительскому окну.

Оператор **CheckBox** , который может использоваться только в операторе [**диаложекс**](dialogex-resource.md) , определяет текст, идентификатор, измерения и атрибуты элемента управления.

``` syntax
CHECKBOX text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span id="text"></span><span id="TEXT"></span>*полнотекстовым*
</dt> <dd>

Текст, отображаемый справа от элемента управления.

</dd> <dt>

<span id="style"></span><span id="STYLE"></span>*стиль*
</dt> <dd>

Стили элементов управления. Это значение может быть сочетанием **\_ флажка** "класс кнопки" и стилей группы **WS \_ TABSTOP** и **WS \_** .

Если стиль не указан, используется стиль по умолчанию `BS_CHECKBOX | WS_TABSTOP` .

</dd> </dl>

Дополнительные сведения об общем синтаксисе инструкции Control см. в разделе [Общие параметры управления](common-control-parameters.md).

## <a name="examples"></a>Примеры

В этом примере определяется элемент управления "флажок", помеченный курсивом:

``` syntax
CHECKBOX "Italic", 3, 10, 10, 40, 10
```

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Автофлажок**](autocheckbox-control.md)
</dt> <dt>

[**AUTO3STATE**](auto3state-control.md)
</dt> <dt>

[Флажки](https://www.bing.com/search?q=Check+Boxes)
</dt> <dt>

[**жетдиалогбасеунитс**](/windows/win32/api/winuser/nf-winuser-getdialogbaseunits)
</dt> <dt>

[**STATE3**](state3-control.md)
</dt> </dl>

 

 