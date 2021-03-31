---
title: Элемент управления GROUPBOX (меню и другие ресурсы)
description: Определяет элемент управления "Группа". Элемент управления — это прямоугольник, который объединяет другие элементы управления. Элементы управления группируются путем рисования границы вокруг них и отображения заданного текста в левом верхнем углу.
ms.assetid: ffca7b68-0326-4fbe-8330-7d1151abb14a
keywords:
- Меню элементов управления GROUPBOX и другие ресурсы
topic_type:
- apiref
api_name:
- GROUPBOX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4f77461099362e4f100924f82d95dffa09a94fa
ms.sourcegitcommit: 40a1246849dba8ececf54c716b2794b99c96ad50
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/12/2019
ms.locfileid: "104069313"
---
# <a name="groupbox-control"></a><span data-ttu-id="14669-106">Элемент управления GROUPBOX</span><span class="sxs-lookup"><span data-stu-id="14669-106">GROUPBOX control</span></span>

<span data-ttu-id="14669-107">Определяет элемент управления "Группа".</span><span class="sxs-lookup"><span data-stu-id="14669-107">Defines a group box control.</span></span> <span data-ttu-id="14669-108">Элемент управления — это прямоугольник, который объединяет другие элементы управления.</span><span class="sxs-lookup"><span data-stu-id="14669-108">The control is a rectangle that groups other controls together.</span></span> <span data-ttu-id="14669-109">Элементы управления группируются путем рисования границы вокруг них и отображения заданного текста в левом верхнем углу.</span><span class="sxs-lookup"><span data-stu-id="14669-109">The controls are grouped by drawing a border around them and displaying the given text in the upper-left corner.</span></span>

<span data-ttu-id="14669-110">Оператор **GROUPBOX** , который можно использовать только в инструкции [**диаложекс**](dialogex-resource.md) , определяет текст, идентификатор, измерения и атрибуты окна элемента управления.</span><span class="sxs-lookup"><span data-stu-id="14669-110">The **GROUPBOX** statement, which you can use only in a [**DIALOGEX**](dialogex-resource.md) statement, defines the text, identifier, dimensions, and attributes of a control window.</span></span>

``` syntax
GROUPBOX text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span data-ttu-id="14669-111"><span id="style"></span><span id="STYLE"></span>*стиль*</span><span class="sxs-lookup"><span data-stu-id="14669-111"><span id="style"></span><span id="STYLE"></span>*style*</span></span>
</dt> <dd>

<span data-ttu-id="14669-112">Стили элементов управления.</span><span class="sxs-lookup"><span data-stu-id="14669-112">Control styles.</span></span> <span data-ttu-id="14669-113">Это значение может представлять собой сочетание стиля класса кнопки "BS" и стилей **WS \_ TABSTOP** и **WS \_ disabled** . **\_**</span><span class="sxs-lookup"><span data-stu-id="14669-113">This value can be a combination of the button class style **BS\_GROUPBOX** and the **WS\_TABSTOP** and **WS\_DISABLED** styles.</span></span>

<span data-ttu-id="14669-114">Если стиль не указан, то по умолчанию используется стиль **BS \_ GROUPBOX**.</span><span class="sxs-lookup"><span data-stu-id="14669-114">If you do not specify a style, the default style is **BS\_GROUPBOX**.</span></span>

</dd> </dl>

<span data-ttu-id="14669-115">Дополнительные сведения об общем синтаксисе инструкции Control см. в разделе [Общие параметры управления](common-control-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="14669-115">For more information about the general syntax of a control statement, see [Common Control Parameters](common-control-parameters.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="14669-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="14669-116">Remarks</span></span>

<span data-ttu-id="14669-117">Если в стиле содержится элемент **WS \_ TABSTOP** или в тексте задан ускоритель, то фокус перемещается на первый элемент управления в группе.</span><span class="sxs-lookup"><span data-stu-id="14669-117">When the style contains **WS\_TABSTOP** or the text specifies an accelerator, tabbing or pressing the accelerator key moves the focus to the first control within the group.</span></span>

## <a name="examples"></a><span data-ttu-id="14669-118">Примеры</span><span class="sxs-lookup"><span data-stu-id="14669-118">Examples</span></span>

<span data-ttu-id="14669-119">В этом примере определяется элемент управления "Группа" с метками "Параметры":</span><span class="sxs-lookup"><span data-stu-id="14669-119">This example defines a group-box control that is labeled Options:</span></span>

``` syntax
GROUPBOX "Options", 101, 10, 10, 100, 100
```

## <a name="see-also"></a><span data-ttu-id="14669-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="14669-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14669-121">Поля группы</span><span class="sxs-lookup"><span data-stu-id="14669-121">Group Boxes</span></span>](https://www.bing.com/search?q=Group+Boxes)
</dt> </dl>

 

 




