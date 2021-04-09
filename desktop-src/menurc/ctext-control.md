---
title: Элемент управления столбец CTEXT
description: Определяет элемент управления центра текста.
ms.assetid: 11f42d25-8fe1-4a8b-a5c5-c8cb47cc8c73
keywords:
- Меню элементов управления столбец CTEXT и другие ресурсы
topic_type:
- apiref
api_name:
- CTEXT
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41c12b6c1da5d5bd5c8ce59a01e21b05baf77503
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104133787"
---
# <a name="ctext-control"></a>Элемент управления столбец CTEXT

Определяет элемент управления центра текста. Элемент управления — это простой прямоугольник, который отображает заданный текст в центре прямоугольника. Перед отображением текст форматируется. Слова, которые будут расширяться после конца строки, автоматически упаковываются в начало следующей строки. Слова, длина которых превышает ширину элемента управления, усекаются.

Инструкция [**лтекст**](ltext-control.md) , которая может использоваться только в операторе представителя, определяет текст, идентификатор, измерения и атрибуты элемента управления.

``` syntax
CTEXT text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span id="text"></span><span id="TEXT"></span>*полнотекстовым*
</dt> <dd>

Текст, который должен быть центрирован в прямоугольной области элемента управления.

</dd> <dt>

<span id="style"></span><span id="STYLE"></span>*стиль*
</dt> <dd>

Стили элементов управления. Это значение может быть любым сочетанием следующих стилей: **SS \_ Center**, **WS \_ TABSTOP** и **WS \_**.

Если стиль не указан, используется стиль по умолчанию `SS_CENTER | WS_GROUP` .

</dd> </dl>

Дополнительные сведения об общем синтаксисе инструкции Control см. в разделе [Общие параметры управления](common-control-parameters.md).

## <a name="examples"></a>Примеры

В этом примере определяется центрированный текст элемента управления с именем filename:

``` syntax
CTEXT "Filename", 101, 10, 10, 100, 100 
```

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**CONTROL**](control-control.md)
</dt> <dt>

[Изменить элементы управления](../controls/about-edit-controls.md)
</dt> <dt>

[**лтекст**](ltext-control.md)
</dt> <dt>

[**ртекст**](rtext-control.md)
</dt> </dl>

 

 