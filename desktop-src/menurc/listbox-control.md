---
title: Элемент управления LISTBOX (меню и другие ресурсы)
description: Определяет часто используемые элементы управления для диалогового окна или окна. Элемент управления — это прямоугольник, содержащий список строк (например, имен файлов), из которых пользователь может выбрать.
ms.assetid: 78f6d36e-5079-4f04-87e4-ca55a1161a51
keywords:
- Меню элементов управления LISTBOX и другие ресурсы
topic_type:
- apiref
api_name:
- LISTBOX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9f062387463917438a988c3b023ca656beef722
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104133842"
---
# <a name="listbox-control"></a><span data-ttu-id="85d4d-105">Элемент управления LISTBOX</span><span class="sxs-lookup"><span data-stu-id="85d4d-105">LISTBOX control</span></span>

<span data-ttu-id="85d4d-106">Определяет часто используемые элементы управления для диалогового окна или окна.</span><span class="sxs-lookup"><span data-stu-id="85d4d-106">Defines commonly used controls for a dialog box or window.</span></span> <span data-ttu-id="85d4d-107">Элемент управления — это прямоугольник, содержащий список строк (например, имен файлов), из которых пользователь может выбрать.</span><span class="sxs-lookup"><span data-stu-id="85d4d-107">The control is a rectangle containing a list of strings (such as filenames) from which the user can select.</span></span>

<span data-ttu-id="85d4d-108">Оператор **ListBox** , который может использоваться только в инструкции [**диаложекс**](dialogex-resource.md) или **Window** , определяет идентификатор, измерения и атрибуты окна управления.</span><span class="sxs-lookup"><span data-stu-id="85d4d-108">The **LISTBOX** statement, which can only be used in a [**DIALOGEX**](dialogex-resource.md) or **WINDOW** statement, defines the identifier, dimensions, and attributes of a control window.</span></span>

``` syntax
LISTBOX id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span data-ttu-id="85d4d-109"><span id="style"></span><span id="STYLE"></span>*стиль*</span><span class="sxs-lookup"><span data-stu-id="85d4d-109"><span id="style"></span><span id="STYLE"></span>*style*</span></span>
</dt> <dd>

<span data-ttu-id="85d4d-110">Стили элементов управления.</span><span class="sxs-lookup"><span data-stu-id="85d4d-110">Control styles.</span></span> <span data-ttu-id="85d4d-111">Это значение может быть сочетанием стилей класса окна списка и любого из следующих стилей: **WS \_ border** и **WS \_ VSCROLL**.</span><span class="sxs-lookup"><span data-stu-id="85d4d-111">This value can be a combination of the list-box class styles and any of the following styles: **WS\_BORDER** and **WS\_VSCROLL**.</span></span>

<span data-ttu-id="85d4d-112">Если стиль не указан, используется стиль по умолчанию `LBS_NOTIFY | WS_BORDER` .</span><span class="sxs-lookup"><span data-stu-id="85d4d-112">If you do not specify a style, the default style is `LBS_NOTIFY | WS_BORDER`.</span></span>

</dd> </dl>

<span data-ttu-id="85d4d-113">Дополнительные сведения об общем синтаксисе инструкции Control см. в разделе [Общие параметры управления](common-control-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="85d4d-113">For more information about the general syntax of a control statement, see [Common Control Parameters](common-control-parameters.md).</span></span>

## <a name="examples"></a><span data-ttu-id="85d4d-114">Примеры</span><span class="sxs-lookup"><span data-stu-id="85d4d-114">Examples</span></span>

<span data-ttu-id="85d4d-115">В этом примере определяется элемент управления "список", идентификатор которого равен 101:</span><span class="sxs-lookup"><span data-stu-id="85d4d-115">This example defines a list-box control whose identifier is 101:</span></span>

``` syntax
LISTBOX 101, 10, 10, 100, 100
```

## <a name="see-also"></a><span data-ttu-id="85d4d-116">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="85d4d-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85d4d-117">**COMBOBOX**</span><span class="sxs-lookup"><span data-stu-id="85d4d-117">**COMBOBOX**</span></span>](combobox-control.md)
</dt> <dt>

[<span data-ttu-id="85d4d-118">Списки</span><span class="sxs-lookup"><span data-stu-id="85d4d-118">List Boxes</span></span>](../controls/about-list-boxes.md)
</dt> </dl>

 

 