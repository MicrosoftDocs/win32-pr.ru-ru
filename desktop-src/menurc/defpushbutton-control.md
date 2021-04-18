---
title: Элемент управления ДЕФПУШБУТТОН
description: Определяет элемент управления принудительной кнопки по умолчанию.
ms.assetid: 17b2ffcb-0611-4d92-9108-bf27b1c07049
keywords:
- Меню элементов управления ДЕФПУШБУТТОН и другие ресурсы
topic_type:
- apiref
api_name:
- DEFPUSHBUTTON
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49b958e60d812c3372ad6a6e6ed2a8d02d56c0f6
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "105672239"
---
# <a name="defpushbutton-control"></a>Элемент управления ДЕФПУШБУТТОН

Определяет элемент управления принудительной кнопки по умолчанию. Элемент управления является небольшим прямоугольником с полужирным контуром, представляющим ответ по умолчанию для пользователя. Заданный текст отображается внутри кнопки. Элемент управления выделяет кнопку обычным образом, когда пользователь нажимает на нее указатель мыши и отправляет сообщение родительскому окну.

``` syntax
DEFPUSHBUTTON text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span id="text"></span><span id="TEXT"></span>*полнотекстовым*
</dt> <dd>

Текст, который должен быть центрирован в прямоугольной области элемента управления.

</dd> <dt>

<span id="style"></span><span id="STYLE"></span>*стиль*
</dt> <dd>

Стили элементов управления. Это значение может быть сочетанием следующих стилей: **BS \_ дефпушбуттон**, **WS \_ TABSTOP**, **WS \_ Group** и **WS \_ disabled**.

Если стиль не указан, используется стиль по умолчанию `BS_DEFPUSHBUTTON | WS_TABSTOP` .

</dd> </dl>

Дополнительные сведения об общем синтаксисе инструкции Control см. в разделе [Общие параметры управления](common-control-parameters.md).

## <a name="examples"></a>Примеры

В этом примере определяется элемент управления принудительной кнопки по умолчанию, помеченный как Cancel:

``` syntax
DEFPUSHBUTTON "Cancel", 101, 10, 10, 24, 50
```

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Кнопки Push-уведомлений](https://www.bing.com/search?q=Push+Buttons)
</dt> <dt>

[**PUSHBUTTON**](pushbutton-control.md)
</dt> <dt>

[**RADIOBUTTON**](radiobutton-control.md)
</dt> </dl>

 

 




