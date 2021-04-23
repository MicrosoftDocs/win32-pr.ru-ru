---
title: Элемент управления CHECKBOX (компилятор ресурсов)
description: Определяет элемент управления "флажок".
ms.assetid: 24ee25e5-9de2-4843-a55e-96b897f6ae8e
keywords:
- Меню элементов управления CHECKBOX и другие ресурсы
topic_type:
- apiref
api_name:
- CHECKBOX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57b4a86a2f08baf7d6e3af9960bd68db1eba86f1
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "105700851"
---
# <a name="checkbox-control"></a><span data-ttu-id="771c7-104">Элемент управления CHECKBOX</span><span class="sxs-lookup"><span data-stu-id="771c7-104">CHECKBOX control</span></span>

<span data-ttu-id="771c7-105">Определяет элемент управления "флажок".</span><span class="sxs-lookup"><span data-stu-id="771c7-105">Defines a check box control.</span></span> <span data-ttu-id="771c7-106">Элемент управления является небольшим прямоугольником (флажок), для которого рядом с ним отображается указанный текст (обычно справа).</span><span class="sxs-lookup"><span data-stu-id="771c7-106">The control is a small rectangle (check box) that has the specified text displayed next to it (typically, to the right).</span></span> <span data-ttu-id="771c7-107">Когда пользователь выбирает элемент управления, элемент управления выделяет прямоугольник и отправляет сообщение родительскому окну.</span><span class="sxs-lookup"><span data-stu-id="771c7-107">When the user selects the control, the control highlights the rectangle and sends a message to its parent window.</span></span>

<span data-ttu-id="771c7-108">Оператор **CheckBox** , который может использоваться только в операторе [**диаложекс**](dialogex-resource.md) , определяет текст, идентификатор, измерения и атрибуты элемента управления.</span><span class="sxs-lookup"><span data-stu-id="771c7-108">The **CHECKBOX** statement, which can only be used in a [**DIALOGEX**](dialogex-resource.md) statement, defines the text, identifier, dimensions, and attributes of the control.</span></span>

``` syntax
CHECKBOX text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span data-ttu-id="771c7-109"><span id="text"></span><span id="TEXT"></span>*полнотекстовым*</span><span class="sxs-lookup"><span data-stu-id="771c7-109"><span id="text"></span><span id="TEXT"></span>*text*</span></span>
</dt> <dd>

<span data-ttu-id="771c7-110">Текст, отображаемый справа от элемента управления.</span><span class="sxs-lookup"><span data-stu-id="771c7-110">Text that is to be displayed to the right of the control.</span></span>

</dd> <dt>

<span data-ttu-id="771c7-111"><span id="style"></span><span id="STYLE"></span>*стиль*</span><span class="sxs-lookup"><span data-stu-id="771c7-111"><span id="style"></span><span id="STYLE"></span>*style*</span></span>
</dt> <dd>

<span data-ttu-id="771c7-112">Стили элементов управления.</span><span class="sxs-lookup"><span data-stu-id="771c7-112">Control styles.</span></span> <span data-ttu-id="771c7-113">Это значение может быть сочетанием **\_ флажка** "класс кнопки" и стилей группы **WS \_ TABSTOP** и **WS \_** .</span><span class="sxs-lookup"><span data-stu-id="771c7-113">This value can be a combination of the button class style **BS\_CHECKBOX** and the **WS\_TABSTOP** and **WS\_GROUP** styles.</span></span>

<span data-ttu-id="771c7-114">Если стиль не указан, используется стиль по умолчанию `BS_CHECKBOX | WS_TABSTOP` .</span><span class="sxs-lookup"><span data-stu-id="771c7-114">If you do not specify a style, the default style is `BS_CHECKBOX | WS_TABSTOP`.</span></span>

</dd> </dl>

<span data-ttu-id="771c7-115">Дополнительные сведения об общем синтаксисе инструкции Control см. в разделе [Общие параметры управления](common-control-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="771c7-115">For more information about the general syntax of a control statement, see [Common Control Parameters](common-control-parameters.md).</span></span>

## <a name="examples"></a><span data-ttu-id="771c7-116">Примеры</span><span class="sxs-lookup"><span data-stu-id="771c7-116">Examples</span></span>

<span data-ttu-id="771c7-117">В этом примере определяется элемент управления "флажок", помеченный курсивом:</span><span class="sxs-lookup"><span data-stu-id="771c7-117">This example defines a check-box control that is labeled Italic:</span></span>

``` syntax
CHECKBOX "Italic", 3, 10, 10, 40, 10
```

## <a name="see-also"></a><span data-ttu-id="771c7-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="771c7-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="771c7-119">**Автофлажок**</span><span class="sxs-lookup"><span data-stu-id="771c7-119">**AUTOCHECKBOX**</span></span>](autocheckbox-control.md)
</dt> <dt>

[<span data-ttu-id="771c7-120">**AUTO3STATE**</span><span class="sxs-lookup"><span data-stu-id="771c7-120">**AUTO3STATE**</span></span>](auto3state-control.md)
</dt> <dt>

[<span data-ttu-id="771c7-121">Флажки</span><span class="sxs-lookup"><span data-stu-id="771c7-121">Check Boxes</span></span>](https://www.bing.com/search?q=Check+Boxes)
</dt> <dt>

[<span data-ttu-id="771c7-122">**жетдиалогбасеунитс**</span><span class="sxs-lookup"><span data-stu-id="771c7-122">**GetDialogBaseUnits**</span></span>](/windows/win32/api/winuser/nf-winuser-getdialogbaseunits)
</dt> <dt>

[<span data-ttu-id="771c7-123">**STATE3**</span><span class="sxs-lookup"><span data-stu-id="771c7-123">**STATE3**</span></span>](state3-control.md)
</dt> </dl>

 

 