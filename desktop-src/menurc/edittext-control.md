---
title: Элемент управления EDITTEXT
description: Определяет элемент управления "поле ввода", принадлежащий классу EDIT.
ms.assetid: 9dc4be90-9503-4c97-813d-db246869ba3c
keywords:
- Меню элементов управления EDITTEXT и другие ресурсы
topic_type:
- apiref
api_name:
- EDITTEXT
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 511cff6791703b30ec975625e0cd5cb044f4f492
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "103790560"
---
# <a name="edittext-control"></a>Элемент управления EDITTEXT

Определяет элемент управления "поле ввода", принадлежащий классу EDIT. Он создает прямоугольную область, в которой пользователь может вводить и редактировать текст. Элемент управления отображает курсор, когда пользователь нажимает на него указатель мыши. Пользователь может использовать клавиатуру для ввода текста или редактирования существующего текста. Ключи редактирования включают в себя клавиши BACKSPACE и DELETE. Пользователь может также использовать мышь, чтобы выбрать символы для удаления или выбрать место для вставки новых символов.

``` syntax
EDITTEXT id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span id="style"></span><span id="STYLE"></span>*стиль*
</dt> <dd>

Стили элементов управления. Это значение может быть сочетанием стилей класса изменить и следующими стилями: **WS \_ TABSTOP**, **WS \_ Group**, **WS \_ VSCROLL**, **WS \_ HSCROLL** и **WS \_ disabled**.

Если стиль не указан, используется стиль по умолчанию `ES_LEFT | WS_BORDER | WS_TABSTOP` .

</dd> </dl>

Дополнительные сведения об общем синтаксисе инструкции Control см. в разделе [Общие параметры управления](common-control-parameters.md).

## <a name="examples"></a>Примеры

В следующем примере демонстрируется использование оператора **EditText** :

``` syntax
EDITTEXT  3, 10, 10, 100, 10
```

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Изменить элементы управления](../controls/about-edit-controls.md)
</dt> </dl>

 

 