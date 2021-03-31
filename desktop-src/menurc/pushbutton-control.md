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
ms.openlocfilehash: b9a303121b7c0eee7ac57fc369164547bd3ae6b9
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104337468"
---
# <a name="pushbutton-control"></a><span data-ttu-id="e1cd0-107">Кнопка элемента управления</span><span class="sxs-lookup"><span data-stu-id="e1cd0-107">PUSHBUTTON control</span></span>

<span data-ttu-id="e1cd0-108">Определяет элемент управления "Кнопка".</span><span class="sxs-lookup"><span data-stu-id="e1cd0-108">Defines a push-button control.</span></span> <span data-ttu-id="e1cd0-109">Элемент управления является прямоугольником с закругленными углами, содержащим заданный текст.</span><span class="sxs-lookup"><span data-stu-id="e1cd0-109">The control is a round-cornered rectangle containing the given text.</span></span> <span data-ttu-id="e1cd0-110">Текст выравнивается по центру элемента управления.</span><span class="sxs-lookup"><span data-stu-id="e1cd0-110">The text is centered in the control.</span></span> <span data-ttu-id="e1cd0-111">Элемент управления отправляет сообщение своему родителю каждый раз, когда пользователь выбирает элемент управления.</span><span class="sxs-lookup"><span data-stu-id="e1cd0-111">The control sends a message to its parent whenever the user chooses the control.</span></span>

``` syntax
PUSHBUTTON text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span data-ttu-id="e1cd0-112"><span id="style"></span><span id="STYLE"></span>*стиль*</span><span class="sxs-lookup"><span data-stu-id="e1cd0-112"><span id="style"></span><span id="STYLE"></span>*style*</span></span>
</dt> <dd>

<span data-ttu-id="e1cd0-113">Стили для кнопки, которые могут быть сочетанием стиля « **\_ кнопка BS** » и следующими стилями: **WS \_ TABSTOP**, **WS \_ disabled** и **WS \_ Group**.</span><span class="sxs-lookup"><span data-stu-id="e1cd0-113">Styles for the pushbutton, which can be a combination of the **BS\_PUSHBUTTON** style and the following styles: **WS\_TABSTOP**, **WS\_DISABLED**, and **WS\_GROUP**.</span></span>

<span data-ttu-id="e1cd0-114">Если стиль не указан, используется стиль по умолчанию `BS_PUSHBUTTON | WS_TABSTOP` .</span><span class="sxs-lookup"><span data-stu-id="e1cd0-114">If you do not specify a style, the default style is `BS_PUSHBUTTON | WS_TABSTOP`.</span></span>

</dd> </dl>

<span data-ttu-id="e1cd0-115">Дополнительные сведения об общем синтаксисе инструкции Control см. в разделе [Общие параметры управления](common-control-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="e1cd0-115">For more information about the general syntax of a control statement, see [Common Control Parameters](common-control-parameters.md).</span></span>

## <a name="examples"></a><span data-ttu-id="e1cd0-116">Примеры</span><span class="sxs-lookup"><span data-stu-id="e1cd0-116">Examples</span></span>

<span data-ttu-id="e1cd0-117">В следующем примере показано использование оператора « **кнопка** »:</span><span class="sxs-lookup"><span data-stu-id="e1cd0-117">The following example demonstrates the use of the **PUSHBUTTON** statement:</span></span>

``` syntax
PUSHBUTTON "ON", 7, 10, 10, 20, 10
```

## <a name="see-also"></a><span data-ttu-id="e1cd0-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e1cd0-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1cd0-119">**жетдиалогбасеунитс**</span><span class="sxs-lookup"><span data-stu-id="e1cd0-119">**GetDialogBaseUnits**</span></span>](/windows/win32/api/winuser/nf-winuser-getdialogbaseunits)
</dt> <dt>

[<span data-ttu-id="e1cd0-120">Кнопки Push-уведомлений</span><span class="sxs-lookup"><span data-stu-id="e1cd0-120">Push Buttons</span></span>](https://www.bing.com/search?q=Push+Buttons)
</dt> </dl>

 

 