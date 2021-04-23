---
title: Элемент управления COMBOBOX (меню и другие ресурсы)
description: Определяет сочетание элемента управления "поле" (поле со списком).
ms.assetid: 0a0fcfa8-b65c-44c1-89d8-f5020af10f0f
keywords:
- Меню элемента управления COMBOBOX и другие ресурсы
topic_type:
- apiref
api_name:
- COMBOBOX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 311cb45282b949a166add8d3aececc0698803fe5
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104412854"
---
# <a name="combobox-control"></a><span data-ttu-id="b9ce4-104">Элемент управления COMBOBOX</span><span class="sxs-lookup"><span data-stu-id="b9ce4-104">COMBOBOX control</span></span>

<span data-ttu-id="b9ce4-105">Определяет сочетание элемента управления "поле" (поле со списком).</span><span class="sxs-lookup"><span data-stu-id="b9ce4-105">Defines a combination box control (a combo box).</span></span> <span data-ttu-id="b9ce4-106">Поле со списком содержит либо статическое текстовое поле, либо поле редактирования, объединенное с полем со списком.</span><span class="sxs-lookup"><span data-stu-id="b9ce4-106">A combo box consists of either a static text box or an edit box combined with a list box.</span></span> <span data-ttu-id="b9ce4-107">Список может отображаться в любое время или быть извлечен пользователем.</span><span class="sxs-lookup"><span data-stu-id="b9ce4-107">The list box can be displayed at all times or pulled down by the user.</span></span> <span data-ttu-id="b9ce4-108">Если поле со списком содержит статическое текстовое поле, то в текстовом поле всегда будет отображаться выбор (если он есть) в области списка в поле со списком.</span><span class="sxs-lookup"><span data-stu-id="b9ce4-108">If the combo box contains a static text box, the text box always displays the selection (if any) in the list box portion of the combo box.</span></span> <span data-ttu-id="b9ce4-109">Если в нем используется поле ввода, пользователь может ввести нужный вариант. в списке выделяется первый элемент (если таковой имеется), соответствующий введенному пользователем в поле ввода.</span><span class="sxs-lookup"><span data-stu-id="b9ce4-109">If it uses an edit box, the user can type in the desired selection; the list box highlights the first item (if any) that matches what the user has entered in the edit box.</span></span> <span data-ttu-id="b9ce4-110">Затем пользователь может выбрать элемент, выделенный в списке, чтобы завершить выбор.</span><span class="sxs-lookup"><span data-stu-id="b9ce4-110">The user can then select the item highlighted in the list box to complete the choice.</span></span> <span data-ttu-id="b9ce4-111">Кроме того, поле со списком может быть выведено владельцем и имеет фиксированную или переменную высоту.</span><span class="sxs-lookup"><span data-stu-id="b9ce4-111">In addition, the combo box can be owner-drawn and of fixed or variable height.</span></span>

``` syntax
COMBOBOX id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span data-ttu-id="b9ce4-112"><span id="style"></span><span id="STYLE"></span>*стиль*</span><span class="sxs-lookup"><span data-stu-id="b9ce4-112"><span id="style"></span><span id="STYLE"></span>*style*</span></span>
</dt> <dd>

<span data-ttu-id="b9ce4-113">Стили элементов управления.</span><span class="sxs-lookup"><span data-stu-id="b9ce4-113">Control styles.</span></span> <span data-ttu-id="b9ce4-114">Это значение может быть сочетанием стилей класса COMBOBOX и любого из следующих стилей: **WS \_ TABSTOP**, **WS \_ Group**, **WS \_ VSCROLL** и **WS \_ disabled**.</span><span class="sxs-lookup"><span data-stu-id="b9ce4-114">This value can be a combination of the COMBOBOX class styles and any of the following styles: **WS\_TABSTOP**, **WS\_GROUP**, **WS\_VSCROLL**, and **WS\_DISABLED**.</span></span>

<span data-ttu-id="b9ce4-115">Если стиль не указан, используется стиль по умолчанию `CBS_SIMPLE | WS_TABSTOP` .</span><span class="sxs-lookup"><span data-stu-id="b9ce4-115">If you do not specify a style, the default style is `CBS_SIMPLE | WS_TABSTOP`.</span></span>

</dd> </dl>

<span data-ttu-id="b9ce4-116">Параметр *Height* применяется к высоте поля со списком, в котором раскрывающийся список полностью развернут.</span><span class="sxs-lookup"><span data-stu-id="b9ce4-116">The *height* parameter applies to the height of a combo box with a drop-down list fully expanded.</span></span>

<span data-ttu-id="b9ce4-117">Дополнительные сведения об общем синтаксисе инструкции Control см. в разделе [Общие параметры управления](common-control-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="b9ce4-117">For more information about the general syntax of a control statement, see [Common Control Parameters](common-control-parameters.md).</span></span>

## <a name="examples"></a><span data-ttu-id="b9ce4-118">Примеры</span><span class="sxs-lookup"><span data-stu-id="b9ce4-118">Examples</span></span>

<span data-ttu-id="b9ce4-119">В этом примере определяется элемент управления "поле со списком" с вертикальной полосой прокрутки:</span><span class="sxs-lookup"><span data-stu-id="b9ce4-119">This example defines a combo-box control with a vertical scroll bar:</span></span>

``` syntax
COMBOBOX 777, 10, 10, 50, 54, CBS_SIMPLE | WS_VSCROLL | WS_TABSTOP 
```

## <a name="see-also"></a><span data-ttu-id="b9ce4-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b9ce4-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9ce4-121">Поля со списком</span><span class="sxs-lookup"><span data-stu-id="b9ce4-121">Combo Boxes</span></span>](../controls/about-combo-boxes.md)
</dt> </dl>

 

 