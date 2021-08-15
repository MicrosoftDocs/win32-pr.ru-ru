---
title: Элемент управления SCROLLBAR
description: Определяет элемент управления "полоса прокрутки".
ms.assetid: 9b0b60b1-4b4b-494e-90d0-aaa67e7ea88c
keywords:
- Меню элемента управления SCROLLBAR и другие ресурсы
topic_type:
- apiref
api_name:
- SCROLLBAR
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b03865f66a06198cc1b1b78f8bb0b0213d998b7e5407506e4b8ed64ed9efaf9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118733442"
---
# <a name="scrollbar-control"></a>Элемент управления SCROLLBAR

Определяет элемент управления "полоса прокрутки". Элемент управления — это прямоугольник, который содержит поле прокрутки и имеет стрелки направления на обоих концах. Элемент управления "полоса прокрутки" отправляет сообщение уведомления родительскому пользователю, когда пользователь щелкает мышью в элементе управления. Родительский элемент отвечает за обновление расположения прокрутки. Элементы управления "полоса прокрутки" можно располагать в любом месте окна и использовать при необходимости для ввода прокрутки.

``` syntax
SCROLLBAR id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span id="style"></span><span id="STYLE"></span>*стиль*
</dt> <dd>

Ноль или сочетание следующих стилей: **WS \_ TABSTOP**, **WS \_ Group** и **WS \_ disabled**.

В дополнение к этим стилям параметр *Style* может содержать сочетание (или ни одного) стилей класса ScrollBar.

Если стиль не указан, по умолчанию используется тип **SBS \_ горизонтали**.

</dd> </dl>

Дополнительные сведения об общем синтаксисе инструкции Control см. в разделе [Общие параметры управления](common-control-parameters.md). Обратите внимание, что нельзя указать текст для этого элемента управления.

## <a name="examples"></a>Примеры

В следующем примере демонстрируется использование оператора **ScrollBar** :

``` syntax
#define IDC_SCROLLBARV                  1010

SCROLLBAR IDC_SCROLLBARV, 7, 55, 187, 44, SBS_VERT
```

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Полосы прокрутки](../controls/about-scroll-bars.md)
</dt> </dl>

 

 