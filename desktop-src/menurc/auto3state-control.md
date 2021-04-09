---
title: Элемент управления AUTO3STATE
description: Определяет автоматически установленный флажок с тремя состояниями.
ms.assetid: 8b27367c-30d0-4591-93d0-756c65255b26
keywords:
- Меню элементов управления AUTO3STATE и другие ресурсы
topic_type:
- apiref
api_name:
- AUTO3STATE
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de184a639de7beee7ac05bdf63609ae29a0f034b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104133791"
---
# <a name="auto3state-control"></a>Элемент управления AUTO3STATE

Определяет автоматически установленный флажок с тремя состояниями. Элемент управления является открытым полем с заданным текстом, расположенным справа от поля. При выборе этого поля автоматически перемещается между тремя состояниями: установлен, снят и отключен (серым цветом). Элемент управления отправляет сообщение своему родителю каждый раз, когда пользователь выбирает элемент управления.

``` syntax
AUTO3STATE text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span id="style"></span><span id="STYLE"></span>*стиль*
</dt> <dd>

Стили для элемента управления, которые могут быть сочетанием стиля **BS \_ AUTO3STATE** и следующих стилей: **WS \_ TABSTOP**, **WS \_ disabled** и **WS \_ Group**.

Если стиль не указан, используется стиль по умолчанию `BS_AUTO3STATE | WS_TABSTOP` .

</dd> </dl>

Дополнительные сведения об общем синтаксисе инструкции Control см. в разделе [Общие параметры управления](common-control-parameters.md).

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Автофлажок**](autocheckbox-control.md)
</dt> <dt>

[Флажки](https://www.bing.com/search?q=Check+Boxes)
</dt> <dt>

[**Установка**](checkbox-control.md)
</dt> <dt>

[**CONTROL**](control-control.md)
</dt> <dt>

[**STATE3**](state3-control.md)
</dt> <dt>

[Стили окна](/windows/desktop/winmsg/window-styles)
</dt> </dl>

 

 