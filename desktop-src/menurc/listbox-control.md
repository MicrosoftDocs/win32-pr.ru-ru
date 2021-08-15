---
title: Элемент управления LISTBOX (меню и другие ресурсы)
description: Определяет часто используемые элементы управления для диалогового окна или окна. Элемент управления — это прямоугольник, содержащий список строк (например, имен файлов), из которых пользователь может выбрать.
ms.assetid: 78f6d36e-5079-4f04-87e4-ca55a1161a51
keywords:
- Меню элементов управления LISTBOX и другие ресурсы
topic_type:
- apiref
api_name:
- LISTBOX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 676ea07f7d66a0d84997f0b2b22b9973c326db0fb603caedcc631caeffffaf98
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119226352"
---
# <a name="listbox-control"></a>Элемент управления LISTBOX

Определяет часто используемые элементы управления для диалогового окна или окна. Элемент управления — это прямоугольник, содержащий список строк (например, имен файлов), из которых пользователь может выбрать.

Оператор **ListBox** , который может использоваться только в инструкции [**диаложекс**](dialogex-resource.md) или **Window** , определяет идентификатор, измерения и атрибуты окна управления.

``` syntax
LISTBOX id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span id="style"></span><span id="STYLE"></span>*стиль*
</dt> <dd>

Стили элементов управления. Это значение может быть сочетанием стилей класса окна списка и любого из следующих стилей: **WS \_ border** и **WS \_ VSCROLL**.

Если стиль не указан, используется стиль по умолчанию `LBS_NOTIFY | WS_BORDER` .

</dd> </dl>

Дополнительные сведения об общем синтаксисе инструкции Control см. в разделе [Общие параметры управления](common-control-parameters.md).

## <a name="examples"></a>Примеры

В этом примере определяется элемент управления "список", идентификатор которого равен 101:

``` syntax
LISTBOX 101, 10, 10, 100, 100
```

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**COMBOBOX**](combobox-control.md)
</dt> <dt>

[Списки](../controls/about-list-boxes.md)
</dt> </dl>

 

 