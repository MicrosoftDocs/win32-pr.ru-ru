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
# <a name="auto3state-control"></a><span data-ttu-id="5f074-104">Элемент управления AUTO3STATE</span><span class="sxs-lookup"><span data-stu-id="5f074-104">AUTO3STATE control</span></span>

<span data-ttu-id="5f074-105">Определяет автоматически установленный флажок с тремя состояниями.</span><span class="sxs-lookup"><span data-stu-id="5f074-105">Defines an automatic three-state check box.</span></span> <span data-ttu-id="5f074-106">Элемент управления является открытым полем с заданным текстом, расположенным справа от поля.</span><span class="sxs-lookup"><span data-stu-id="5f074-106">The control is an open box with the given text positioned to the right of the box.</span></span> <span data-ttu-id="5f074-107">При выборе этого поля автоматически перемещается между тремя состояниями: установлен, снят и отключен (серым цветом).</span><span class="sxs-lookup"><span data-stu-id="5f074-107">When chosen, the box automatically advances between three states: checked, unchecked, and disabled (grayed).</span></span> <span data-ttu-id="5f074-108">Элемент управления отправляет сообщение своему родителю каждый раз, когда пользователь выбирает элемент управления.</span><span class="sxs-lookup"><span data-stu-id="5f074-108">The control sends a message to its parent whenever the user chooses the control.</span></span>

``` syntax
AUTO3STATE text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span data-ttu-id="5f074-109"><span id="style"></span><span id="STYLE"></span>*стиль*</span><span class="sxs-lookup"><span data-stu-id="5f074-109"><span id="style"></span><span id="STYLE"></span>*style*</span></span>
</dt> <dd>

<span data-ttu-id="5f074-110">Стили для элемента управления, которые могут быть сочетанием стиля **BS \_ AUTO3STATE** и следующих стилей: **WS \_ TABSTOP**, **WS \_ disabled** и **WS \_ Group**.</span><span class="sxs-lookup"><span data-stu-id="5f074-110">Styles for the control, which can be a combination of the **BS\_AUTO3STATE** style and the following styles: **WS\_TABSTOP**, **WS\_DISABLED**, and **WS\_GROUP**.</span></span>

<span data-ttu-id="5f074-111">Если стиль не указан, используется стиль по умолчанию `BS_AUTO3STATE | WS_TABSTOP` .</span><span class="sxs-lookup"><span data-stu-id="5f074-111">If you do not specify a style, the default style is `BS_AUTO3STATE | WS_TABSTOP`.</span></span>

</dd> </dl>

<span data-ttu-id="5f074-112">Дополнительные сведения об общем синтаксисе инструкции Control см. в разделе [Общие параметры управления](common-control-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="5f074-112">For more information about the general syntax of a control statement, see [Common Control Parameters](common-control-parameters.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="5f074-113">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5f074-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f074-114">**Автофлажок**</span><span class="sxs-lookup"><span data-stu-id="5f074-114">**AUTOCHECKBOX**</span></span>](autocheckbox-control.md)
</dt> <dt>

[<span data-ttu-id="5f074-115">Флажки</span><span class="sxs-lookup"><span data-stu-id="5f074-115">Check Boxes</span></span>](https://www.bing.com/search?q=Check+Boxes)
</dt> <dt>

[<span data-ttu-id="5f074-116">**Установка**</span><span class="sxs-lookup"><span data-stu-id="5f074-116">**CHECKBOX**</span></span>](checkbox-control.md)
</dt> <dt>

[<span data-ttu-id="5f074-117">**CONTROL**</span><span class="sxs-lookup"><span data-stu-id="5f074-117">**CONTROL**</span></span>](control-control.md)
</dt> <dt>

[<span data-ttu-id="5f074-118">**STATE3**</span><span class="sxs-lookup"><span data-stu-id="5f074-118">**STATE3**</span></span>](state3-control.md)
</dt> <dt>

[<span data-ttu-id="5f074-119">Стили окна</span><span class="sxs-lookup"><span data-stu-id="5f074-119">Window Styles</span></span>](/windows/desktop/winmsg/window-styles)
</dt> </dl>

 

 