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
ms.openlocfilehash: a6b220448fcaa6cbbbb6b01c605a9b5fd6e03f8dc6a60a0e409f6f275d9b74b5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119826004"
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

[**ЭЛЕМЕНТА**](control-control.md)
</dt> <dt>

[Изменить элементы управления](../controls/about-edit-controls.md)
</dt> <dt>

[**лтекст**](ltext-control.md)
</dt> <dt>

[**ртекст**](rtext-control.md)
</dt> </dl>

 

 