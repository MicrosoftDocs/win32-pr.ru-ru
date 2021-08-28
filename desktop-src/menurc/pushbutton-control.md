---
title: Элемент управления "Кнопка" (меню и другие ресурсы)
description: Определяет элемент управления "Кнопка". Элемент управления является прямоугольником с закругленными углами, содержащим заданный текст. Текст выравнивается по центру элемента управления. Элемент управления отправляет сообщение своему родителю каждый раз, когда пользователь выбирает элемент управления.
ms.assetid: c5fbcfb7-1b7d-4199-acac-d11bfd899298
keywords:
- Управляющие меню и другие ресурсы для кнопок
topic_type:
- apiref
api_name:
- PUSHBUTTON
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24db89c986f3f6d466f1710bc18420f9da9eec3348eada10e95582a882fe25e9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119777004"
---
# <a name="pushbutton-control"></a>Кнопка элемента управления

Определяет элемент управления "Кнопка". Элемент управления является прямоугольником с закругленными углами, содержащим заданный текст. Текст выравнивается по центру элемента управления. Элемент управления отправляет сообщение своему родителю каждый раз, когда пользователь выбирает элемент управления.

``` syntax
PUSHBUTTON text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span id="style"></span><span id="STYLE"></span>*стиль*
</dt> <dd>

Стили для кнопки, которые могут быть сочетанием стиля « **\_ кнопка BS** » и следующими стилями: **WS \_ TABSTOP**, **WS \_ disabled** и **WS \_ Group**.

Если стиль не указан, используется стиль по умолчанию `BS_PUSHBUTTON | WS_TABSTOP` .

</dd> </dl>

Дополнительные сведения об общем синтаксисе инструкции Control см. в разделе [Общие параметры управления](common-control-parameters.md).

## <a name="examples"></a>Примеры

В следующем примере показано использование оператора « **кнопка** »:

``` syntax
PUSHBUTTON "ON", 7, 10, 10, 20, 10
```

## <a name="see-also"></a>См. также

<dl> <dt>

[**жетдиалогбасеунитс**](/windows/win32/api/winuser/nf-winuser-getdialogbaseunits)
</dt> <dt>

[Кнопки Push-уведомлений](https://www.bing.com/search?q=Push+Buttons)
</dt> </dl>

 

 