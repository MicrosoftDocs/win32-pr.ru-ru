---
title: Элемент управления RADIOBUTTON
description: Определяет элемент управления "переключатель".
ms.assetid: c427080f-0408-42b4-8888-7333f3eb985d
keywords:
- Меню элементов управления RADIOBUTTON и другие ресурсы
topic_type:
- apiref
api_name:
- RADIOBUTTON
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67dd559c2d61ca8b2735d393170c177a65735b4b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104070003"
---
# <a name="radiobutton-control"></a>Элемент управления RADIOBUTTON

Определяет элемент управления "переключатель". Элемент управления представляет собой небольшой круг с текстом, который отображается рядом с ним, как правило, справа. Элемент управления выделяет окружность и отправляет сообщение родительскому окну, когда пользователь нажимает кнопку. Элемент управления удаляет выделение и отправляет сообщение при следующем выборе кнопки.

``` syntax
RADIOBUTTON text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span id="style"></span><span id="STYLE"></span>*стиль*
</dt> <dd>

Стили для переключателя, которые могут быть сочетанием стилей классов кнопок и следующих стилей: **WS \_ TABSTOP**, **WS \_ disabled** и **WS \_ Group**.

Если стиль не указан, используется стиль по умолчанию `BS_RADIOBUTTON | WS_TABSTOP` .

</dd> </dl>

Дополнительные сведения об общем синтаксисе инструкции Control см. в разделе [Общие параметры управления](common-control-parameters.md).

## <a name="examples"></a>Примеры

В следующем примере демонстрируется использование оператора **RADIOBUTTON** :

``` syntax
RADIOBUTTON "Italic", 100, 10, 10, 40, 10
```

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**жетдиалогбасеунитс**](/windows/win32/api/winuser/nf-winuser-getdialogbaseunits)
</dt> <dt>

[Переключатели](https://www.bing.com/search?q=Radio+Buttons)
</dt> </dl>

 

 