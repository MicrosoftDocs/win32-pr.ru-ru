---
title: Элемент управления STATE3
description: 'Определяет элемент управления "флажок" с тремя состояниями. Элемент управления идентичен CHECKBOX, за исключением того, что он имеет три состояния: установлен, снят и отключен (серый цвет).'
ms.assetid: 74659827-ce46-4d36-a5e2-3a97e8fd1c04
keywords:
- Меню элементов управления STATE3 и другие ресурсы
topic_type:
- apiref
api_name:
- STATE3
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24333fa9567db5613896f26429b72ff68e029335
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "103783666"
---
# <a name="state3-control"></a>Элемент управления STATE3

Определяет элемент управления "флажок" с тремя состояниями. Элемент управления идентичен [**CheckBox**](checkbox-control.md), за исключением того, что он имеет три состояния: установлен, снят и отключен (серый цвет).

``` syntax
STATE3 text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span id="text"></span><span id="TEXT"></span>*полнотекстовым*
</dt> <dd>

Текст, отображаемый справа от элемента управления.

</dd> <dt>

<span id="style"></span><span id="STYLE"></span>*стиль*
</dt> <dd>

Стили элементов управления. Это значение может быть сочетанием стиля класса кнопки « **BS \_ 3STATE** » и стилей « **WS \_ TABSTOP** » и « **WS \_** ».

Если стиль не указан, используется стиль по умолчанию `BS_3STATE | WS_TABSTOP` .

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
</dt> </dl>

 

 




