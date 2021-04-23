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
# <a name="state3-control"></a><span data-ttu-id="425c3-105">Элемент управления STATE3</span><span class="sxs-lookup"><span data-stu-id="425c3-105">STATE3 control</span></span>

<span data-ttu-id="425c3-106">Определяет элемент управления "флажок" с тремя состояниями.</span><span class="sxs-lookup"><span data-stu-id="425c3-106">Defines a three-state check box control.</span></span> <span data-ttu-id="425c3-107">Элемент управления идентичен [**CheckBox**](checkbox-control.md), за исключением того, что он имеет три состояния: установлен, снят и отключен (серый цвет).</span><span class="sxs-lookup"><span data-stu-id="425c3-107">The control is identical to a [**CHECKBOX**](checkbox-control.md), except that it has three states: checked, unchecked, and disabled (grayed).</span></span>

``` syntax
STATE3 text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span data-ttu-id="425c3-108"><span id="text"></span><span id="TEXT"></span>*полнотекстовым*</span><span class="sxs-lookup"><span data-stu-id="425c3-108"><span id="text"></span><span id="TEXT"></span>*text*</span></span>
</dt> <dd>

<span data-ttu-id="425c3-109">Текст, отображаемый справа от элемента управления.</span><span class="sxs-lookup"><span data-stu-id="425c3-109">Text that is to be displayed to the right of the control.</span></span>

</dd> <dt>

<span data-ttu-id="425c3-110"><span id="style"></span><span id="STYLE"></span>*стиль*</span><span class="sxs-lookup"><span data-stu-id="425c3-110"><span id="style"></span><span id="STYLE"></span>*style*</span></span>
</dt> <dd>

<span data-ttu-id="425c3-111">Стили элементов управления.</span><span class="sxs-lookup"><span data-stu-id="425c3-111">Control styles.</span></span> <span data-ttu-id="425c3-112">Это значение может быть сочетанием стиля класса кнопки « **BS \_ 3STATE** » и стилей « **WS \_ TABSTOP** » и « **WS \_** ».</span><span class="sxs-lookup"><span data-stu-id="425c3-112">This value can be a combination of the button class style **BS\_3STATE** and the **WS\_TABSTOP** and **WS\_GROUP** styles.</span></span>

<span data-ttu-id="425c3-113">Если стиль не указан, используется стиль по умолчанию `BS_3STATE | WS_TABSTOP` .</span><span class="sxs-lookup"><span data-stu-id="425c3-113">If you do not specify a style, the default style is `BS_3STATE | WS_TABSTOP`.</span></span>

</dd> </dl>

<span data-ttu-id="425c3-114">Дополнительные сведения об общем синтаксисе инструкции Control см. в разделе [Общие параметры управления](common-control-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="425c3-114">For more information about the general syntax of a control statement, see [Common Control Parameters](common-control-parameters.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="425c3-115">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="425c3-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="425c3-116">**Автофлажок**</span><span class="sxs-lookup"><span data-stu-id="425c3-116">**AUTOCHECKBOX**</span></span>](autocheckbox-control.md)
</dt> <dt>

[<span data-ttu-id="425c3-117">Флажки</span><span class="sxs-lookup"><span data-stu-id="425c3-117">Check Boxes</span></span>](https://www.bing.com/search?q=Check+Boxes)
</dt> <dt>

[<span data-ttu-id="425c3-118">**Установка**</span><span class="sxs-lookup"><span data-stu-id="425c3-118">**CHECKBOX**</span></span>](checkbox-control.md)
</dt> <dt>

[<span data-ttu-id="425c3-119">**CONTROL**</span><span class="sxs-lookup"><span data-stu-id="425c3-119">**CONTROL**</span></span>](control-control.md)
</dt> </dl>

 

 




