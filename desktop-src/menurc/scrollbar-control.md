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
ms.openlocfilehash: 44ef4069988603c7c89ec2ed8a363d3515a0b8bb
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104133870"
---
# <a name="scrollbar-control"></a><span data-ttu-id="9861b-104">Элемент управления SCROLLBAR</span><span class="sxs-lookup"><span data-stu-id="9861b-104">SCROLLBAR control</span></span>

<span data-ttu-id="9861b-105">Определяет элемент управления "полоса прокрутки".</span><span class="sxs-lookup"><span data-stu-id="9861b-105">Defines a scroll-bar control.</span></span> <span data-ttu-id="9861b-106">Элемент управления — это прямоугольник, который содержит поле прокрутки и имеет стрелки направления на обоих концах.</span><span class="sxs-lookup"><span data-stu-id="9861b-106">The control is a rectangle that contains a scroll box and has direction arrows at both ends.</span></span> <span data-ttu-id="9861b-107">Элемент управления "полоса прокрутки" отправляет сообщение уведомления родительскому пользователю, когда пользователь щелкает мышью в элементе управления.</span><span class="sxs-lookup"><span data-stu-id="9861b-107">The scroll-bar control sends a notification message to its parent whenever the user clicks the mouse in the control.</span></span> <span data-ttu-id="9861b-108">Родительский элемент отвечает за обновление расположения прокрутки.</span><span class="sxs-lookup"><span data-stu-id="9861b-108">The parent is responsible for updating the scroll-box position.</span></span> <span data-ttu-id="9861b-109">Элементы управления "полоса прокрутки" можно располагать в любом месте окна и использовать при необходимости для ввода прокрутки.</span><span class="sxs-lookup"><span data-stu-id="9861b-109">Scroll-bar controls can be positioned anywhere in a window and used whenever needed to provide scrolling input.</span></span>

``` syntax
SCROLLBAR id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span data-ttu-id="9861b-110"><span id="style"></span><span id="STYLE"></span>*стиль*</span><span class="sxs-lookup"><span data-stu-id="9861b-110"><span id="style"></span><span id="STYLE"></span>*style*</span></span>
</dt> <dd>

<span data-ttu-id="9861b-111">Ноль или сочетание следующих стилей: **WS \_ TABSTOP**, **WS \_ Group** и **WS \_ disabled**.</span><span class="sxs-lookup"><span data-stu-id="9861b-111">Zero or a combination of the following styles: **WS\_TABSTOP**, **WS\_GROUP**, and **WS\_DISABLED**.</span></span>

<span data-ttu-id="9861b-112">В дополнение к этим стилям параметр *Style* может содержать сочетание (или ни одного) стилей класса ScrollBar.</span><span class="sxs-lookup"><span data-stu-id="9861b-112">In addition to these styles, the *style* parameter may contain a combination (or none) of the SCROLLBAR-class styles.</span></span>

<span data-ttu-id="9861b-113">Если стиль не указан, по умолчанию используется тип **SBS \_ горизонтали**.</span><span class="sxs-lookup"><span data-stu-id="9861b-113">If you do not specify a style, the default style is **SBS\_HORZ**.</span></span>

</dd> </dl>

<span data-ttu-id="9861b-114">Дополнительные сведения об общем синтаксисе инструкции Control см. в разделе [Общие параметры управления](common-control-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="9861b-114">For more information about the general syntax of a control statement, see [Common Control Parameters](common-control-parameters.md).</span></span> <span data-ttu-id="9861b-115">Обратите внимание, что нельзя указать текст для этого элемента управления.</span><span class="sxs-lookup"><span data-stu-id="9861b-115">Note that you cannot specify text for this control.</span></span>

## <a name="examples"></a><span data-ttu-id="9861b-116">Примеры</span><span class="sxs-lookup"><span data-stu-id="9861b-116">Examples</span></span>

<span data-ttu-id="9861b-117">В следующем примере демонстрируется использование оператора **ScrollBar** :</span><span class="sxs-lookup"><span data-stu-id="9861b-117">The following example demonstrates the use of the **SCROLLBAR** statement:</span></span>

``` syntax
#define IDC_SCROLLBARV                  1010

SCROLLBAR IDC_SCROLLBARV, 7, 55, 187, 44, SBS_VERT
```

## <a name="see-also"></a><span data-ttu-id="9861b-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9861b-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9861b-119">Полосы прокрутки</span><span class="sxs-lookup"><span data-stu-id="9861b-119">Scroll Bars</span></span>](../controls/about-scroll-bars.md)
</dt> </dl>

 

 