---
title: Элемент управления "автофлажок"
description: Определяет элемент управления автоматического флажка.
ms.assetid: 086f5dd3-267f-4ec6-be37-4e9402f7aede
keywords:
- Меню элемента управления "автофлажок" и другие ресурсы
topic_type:
- apiref
api_name:
- AUTOCHECKBOX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 842bb3ede2b1f96f3e5b343e351e047d112a8403
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "103790320"
---
# <a name="autocheckbox-control"></a><span data-ttu-id="143d2-104">Элемент управления "автофлажок"</span><span class="sxs-lookup"><span data-stu-id="143d2-104">AUTOCHECKBOX control</span></span>

<span data-ttu-id="143d2-105">Определяет элемент управления автоматического флажка.</span><span class="sxs-lookup"><span data-stu-id="143d2-105">Defines an automatic check box control.</span></span> <span data-ttu-id="143d2-106">Элемент управления является небольшим прямоугольником (флажок), для которого рядом с ним отображается указанный текст (обычно справа).</span><span class="sxs-lookup"><span data-stu-id="143d2-106">The control is a small rectangle (check box) that has the specified text displayed next to it (typically, to the right).</span></span> <span data-ttu-id="143d2-107">Когда пользователь выбирает элемент управления, элемент управления выделяет прямоугольник и отправляет сообщение родительскому окну.</span><span class="sxs-lookup"><span data-stu-id="143d2-107">When the user chooses the control, the control highlights the rectangle and sends a message to its parent window.</span></span>

<span data-ttu-id="143d2-108">Инструкцию **автоcheckbox** можно использовать только в теле [**диалогового окна**](dialog-resource.md) или инструкции [**диаложекс**](dialogex-resource.md) .</span><span class="sxs-lookup"><span data-stu-id="143d2-108">The **AUTOCHECKBOX** statement can only be used in the body of a [**DIALOG**](dialog-resource.md) or [**DIALOGEX**](dialogex-resource.md) statement.</span></span>

``` syntax
AUTOCHECKBOX text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span data-ttu-id="143d2-109"><span id="style"></span><span id="STYLE"></span>*стиль*</span><span class="sxs-lookup"><span data-stu-id="143d2-109"><span id="style"></span><span id="STYLE"></span>*style*</span></span>
</dt> <dd>

<span data-ttu-id="143d2-110">Стили элемента управления.</span><span class="sxs-lookup"><span data-stu-id="143d2-110">Styles of the control.</span></span> <span data-ttu-id="143d2-111">Это значение может быть сочетанием стиля класса кнопки **\_ автофлажок BS** и стилей **\_ группы** **WS \_ TABSTOP** и WS.</span><span class="sxs-lookup"><span data-stu-id="143d2-111">This value can be a combination of the button class style **BS\_AUTOCHECKBOX** and the **WS\_TABSTOP** and **WS\_GROUP** styles.</span></span>

<span data-ttu-id="143d2-112">Если стиль не указан, используется стиль по умолчанию `BS_AUTOCHECKBOX | WS_TABSTOP` .</span><span class="sxs-lookup"><span data-stu-id="143d2-112">If you do not specify a style, the default style is `BS_AUTOCHECKBOX | WS_TABSTOP`.</span></span>

</dd> </dl>

<span data-ttu-id="143d2-113">Дополнительные сведения об общем синтаксисе инструкции Control см. в разделе [Общие параметры управления](common-control-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="143d2-113">For more information about the general syntax of a control statement, see [Common Control Parameters](common-control-parameters.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="143d2-114">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="143d2-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="143d2-115">**AUTO3STATE**</span><span class="sxs-lookup"><span data-stu-id="143d2-115">**AUTO3STATE**</span></span>](auto3state-control.md)
</dt> <dt>

[<span data-ttu-id="143d2-116">Стили кнопок</span><span class="sxs-lookup"><span data-stu-id="143d2-116">Button Styles</span></span>](../controls/button-styles.md)
</dt> <dt>

[<span data-ttu-id="143d2-117">**Установка**</span><span class="sxs-lookup"><span data-stu-id="143d2-117">**CHECKBOX**</span></span>](checkbox-control.md)
</dt> <dt>

[<span data-ttu-id="143d2-118">**CONTROL**</span><span class="sxs-lookup"><span data-stu-id="143d2-118">**CONTROL**</span></span>](control-control.md)
</dt> <dt>

[<span data-ttu-id="143d2-119">**STATE3**</span><span class="sxs-lookup"><span data-stu-id="143d2-119">**STATE3**</span></span>](state3-control.md)
</dt> </dl>

 

 